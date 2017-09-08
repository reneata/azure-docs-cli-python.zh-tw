---
title: "使用 Azure CLI 2.0 來建立 Azure 服務主體"
description: "了解如何使用 Azure CLI 2.0 來為應用程式或服務建立服務主體。"
keywords: Azure CLI 2.0, Azure Active Directory, Azure Active directory, AD, RBAC
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: fab89cb8-dac1-4e21-9d34-5eadd5213c05
ms.openlocfilehash: f37df762a9a605ea649b215f38f2e9866614f4ac
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/04/2017
---
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a><span data-ttu-id="f3fad-104">使用 Azure CLI 2.0 來建立 Azure 服務主體</span><span class="sxs-lookup"><span data-stu-id="f3fad-104">Create an Azure service principal with Azure CLI 2.0</span></span>

<span data-ttu-id="f3fad-105">如果您打算使用 Azure CLI 2.0 來管理應用程式或服務，請根據 Azure Active Directory (AAD) 服務主體 (而非您自己的認證) 來執行它。</span><span class="sxs-lookup"><span data-stu-id="f3fad-105">If you plan to manage your app or service with Azure CLI 2.0, you should run it under an Azure Active Directory (AAD) service principal rather than your own credentials.</span></span>
<span data-ttu-id="f3fad-106">本主題會逐步引導您使用 Azure CLI 2.0 來建立安全性主體。</span><span class="sxs-lookup"><span data-stu-id="f3fad-106">This topic steps you through creating a security principal with Azure CLI 2.0.</span></span>

> [!NOTE]
> <span data-ttu-id="f3fad-107">您也可以透過 Azure 入口網站來建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="f3fad-107">You can also create a service principal through the Azure portal.</span></span>
> <span data-ttu-id="f3fad-108">如需詳細資訊，請閱讀[使用入口網站來建立可存取資源的 Active Directory 應用程式和服務主體](/azure/azure-resource-manager/resource-group-create-service-principal-portal)。</span><span class="sxs-lookup"><span data-stu-id="f3fad-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="f3fad-109">何謂「服務主體」？</span><span class="sxs-lookup"><span data-stu-id="f3fad-109">What is a 'service principal'?</span></span>

<span data-ttu-id="f3fad-110">Azure 服務主體是一項安全性識別，可供使用者所建立的應用程式、服務和自動化工具用來存取特定 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="f3fad-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="f3fad-111">您可以把它想成是具有特定角色的「使用者識別」(登入和密碼或憑證)，並具有受到嚴格控制的資源存取權限。</span><span class="sxs-lookup"><span data-stu-id="f3fad-111">Think of it as a 'user identity' (login and password or certificate) with a specific role, and tightly controlled permissions to access your resources.</span></span> <span data-ttu-id="f3fad-112">不同於一般的使用者識別，服務主體只需要能夠執行特定動作。</span><span class="sxs-lookup"><span data-stu-id="f3fad-112">It only needs to be able to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="f3fad-113">如果您只將執行管理工作所需要的最低權限等級授與給服務主體，它就能提高安全性。</span><span class="sxs-lookup"><span data-stu-id="f3fad-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span> 

<span data-ttu-id="f3fad-114">目前，Azure CLI 2.0 只支援建立以密碼為基礎的驗證認證。</span><span class="sxs-lookup"><span data-stu-id="f3fad-114">Right now, Azure CLI 2.0 only supports the creation of password-based authentication credentials.</span></span> <span data-ttu-id="f3fad-115">在本主題中，我們將討論使用特定的密碼來建立服務主體，以及選擇性地將特定的角色指派給它。</span><span class="sxs-lookup"><span data-stu-id="f3fad-115">In this topic, we cover creating a service principal with a specific password, and optionally assigning specific roles to it.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="f3fad-116">確認您自己的權限等級</span><span class="sxs-lookup"><span data-stu-id="f3fad-116">Verify your own permission level</span></span>

<span data-ttu-id="f3fad-117">首先，您在 Azure Active Directory 和 Azure 訂用帳戶中都必須有足夠的權限。</span><span class="sxs-lookup"><span data-stu-id="f3fad-117">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="f3fad-118">具體來說，您必須能夠在 Active Directory 中建立應用程式，並將角色指派給服務主體。</span><span class="sxs-lookup"><span data-stu-id="f3fad-118">Specifically, you must be able to create an app in the Active Directory, and assign a role to the service principal.</span></span> 

<span data-ttu-id="f3fad-119">檢查您的帳戶是否具有足夠的權限，最簡單的方式是透過入口網站。</span><span class="sxs-lookup"><span data-stu-id="f3fad-119">The easiest way to check whether your account has adequate permissions is through the portal.</span></span> <span data-ttu-id="f3fad-120">請參閱[在入口網站中檢查必要的權限](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)。</span><span class="sxs-lookup"><span data-stu-id="f3fad-120">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="f3fad-121">建立應用程式的服務主體</span><span class="sxs-lookup"><span data-stu-id="f3fad-121">Create a service principal for your application</span></span>

<span data-ttu-id="f3fad-122">如需識別您想要建立服務主體的應用程式，您必須具有下列其中一項︰</span><span class="sxs-lookup"><span data-stu-id="f3fad-122">You must have one of the following to identify the app you want to create a service principal for:</span></span>

  * <span data-ttu-id="f3fad-123">已部署之應用程式的唯一名稱或 URI (例如範例中的 "MyDemoWebApp")，或是</span><span class="sxs-lookup"><span data-stu-id="f3fad-123">The unique name or URI of your deployed app (such as "MyDemoWebApp" in the examples), or</span></span>
  * <span data-ttu-id="f3fad-124">應用程式識別碼；與您已部署的應用程式、服務或物件相關聯的唯一 GUID</span><span class="sxs-lookup"><span data-stu-id="f3fad-124">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

<span data-ttu-id="f3fad-125">建立服務主體時，這些值會識別您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f3fad-125">These values identify your application when creating a service principal.</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="f3fad-126">取得應用程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="f3fad-126">Get information about your application</span></span>

<span data-ttu-id="f3fad-127">使用 `az ad app list` 來取得您應用程式的身分識別資訊。</span><span class="sxs-lookup"><span data-stu-id="f3fad-127">Get identity information about your application with the `az ad app list`.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

```azurecli-interactive
az ad app list --display-name MyDemoWebApp
```

```json
{
    "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
    "appPermissions": null,
    "availableToOtherTenants": false,
    "displayName": "MyDemoWebApp",
    "homepage": "http://MyDemoWebApp.azurewebsites.net",
    "identifierUris": [
      "http://MyDemoWebApp"
    ],
    "objectId": "bd07205b-629f-4a2e-945e-1ee5dadf610b9",
    "objectType": "Application",
    "replyUrls": []
  }
```

<span data-ttu-id="f3fad-128">`--display-name` 選項會篩選傳回的應用程式清單，來顯示以 MyDemoWebApp 為開頭且具有 `displayName` 的項目。</span><span class="sxs-lookup"><span data-stu-id="f3fad-128">The `--display-name` option filters the returned list of apps to show those with `displayName` starting with MyDemoWebApp.</span></span>

### <a name="create-the-service-principal"></a><span data-ttu-id="f3fad-129">建立服務主體</span><span class="sxs-lookup"><span data-stu-id="f3fad-129">Create the service principal</span></span>

<span data-ttu-id="f3fad-130">使用 [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) 來建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="f3fad-130">Use [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) to create the service principal.</span></span> 

```azurecli-interactive
az ad sp create-for-rbac --name {appId} --password "{strong password}" 
``` 

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "displayName": "MyDemoWebApp",
  "name": "http://MyDemoWebApp",
  "password": {strong password},
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

 > [!WARNING] 
 > <span data-ttu-id="f3fad-131">請勿建立不安全的密碼。</span><span class="sxs-lookup"><span data-stu-id="f3fad-131">Don't create an insecure password.</span></span>  <span data-ttu-id="f3fad-132">請依照 [Azure AD 密碼規則和限制](/azure/active-directory/active-directory-passwords-policy)指引。</span><span class="sxs-lookup"><span data-stu-id="f3fad-132">Follow the [Azure AD password rules and restrictions](/azure/active-directory/active-directory-passwords-policy) guidance.</span></span>

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="f3fad-133">取得服務主體的相關資訊</span><span class="sxs-lookup"><span data-stu-id="f3fad-133">Get information about the service principal</span></span>

```azurecli-interactive
az ad sp show --id a487e0c1-82af-47d9-9a0b-af184eb87646d
```

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "displayName": "MyDemoWebApp",
  "objectId": "0ceae62e-1a1a-446f-aa56-2300d176659bde",
  "objectType": "ServicePrincipal",
  "servicePrincipalNames": [
    "http://MyDemoWebApp",
    "a487e0c1-82af-47d9-9a0b-af184eb87646d"
  ]
}
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="f3fad-134">使用服務主體來登入</span><span class="sxs-lookup"><span data-stu-id="f3fad-134">Sign in using the service principal</span></span>

<span data-ttu-id="f3fad-135">您現在可以使用來自 `az ad sp show`的「應用程式識別碼」和「密碼」，來登入成為應用程式的新服務主體。</span><span class="sxs-lookup"><span data-stu-id="f3fad-135">You can now log in as the new service principal for your app using the *appId* and *password* from `az ad sp show`.</span></span>  <span data-ttu-id="f3fad-136">提供 `az ad sp create-for-rbac` 結果中的租用戶值。</span><span class="sxs-lookup"><span data-stu-id="f3fad-136">Supply the *tenant* value from the results of `az ad sp create-for-rbac`.</span></span>

```azurecli-interactive
az login --service-principal -u a487e0c1-82af-47d9-9a0b-af184eb87646d --password {password} --tenant {tenant}
``` 

<span data-ttu-id="f3fad-137">成功登入之後，您會看到此輸出︰</span><span class="sxs-lookup"><span data-stu-id="f3fad-137">You will see this output after a successful sign-on:</span></span>

```json
[
  {
    "cloudName": "AzureCloud",
    "id": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
    "isDefault": true,
    "state": "Enabled",
    "tenantId": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
    "user": {
      "name": "https://MyDemoWebApp",
      "type": "servicePrincipal"
    }
  }
]
```

<span data-ttu-id="f3fad-138">使用 `id`、`password` 和 `tenant` 值，作為執行您應用程式的認證。</span><span class="sxs-lookup"><span data-stu-id="f3fad-138">Use the `id`, `password`, and `tenant` values as the credentials for running your app.</span></span> 

## <a name="managing-roles"></a><span data-ttu-id="f3fad-139">管理角色</span><span class="sxs-lookup"><span data-stu-id="f3fad-139">Managing roles</span></span> 

> [!NOTE]
> <span data-ttu-id="f3fad-140">Azure 角色型存取控制 (RBAC) 是一種可定義及管理使用者和服務主體角色的模型。</span><span class="sxs-lookup"><span data-stu-id="f3fad-140">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span>
> <span data-ttu-id="f3fad-141">角色會有一組相關聯的權限，以決定主體可以讀取、存取、寫入或管理的資源。</span><span class="sxs-lookup"><span data-stu-id="f3fad-141">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span>
> <span data-ttu-id="f3fad-142">如需 RBAC 和角色的詳細資訊，請參閱 [RBAC：內建角色](/azure/active-directory/role-based-access-built-in-roles)。</span><span class="sxs-lookup"><span data-stu-id="f3fad-142">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="f3fad-143">Azure CLI 2.0 提供下列命令以供您管理角色指派︰</span><span class="sxs-lookup"><span data-stu-id="f3fad-143">The Azure CLI 2.0 provides the following commands to manage role assignments:</span></span>

* [<span data-ttu-id="f3fad-144">az 角色指派清單</span><span class="sxs-lookup"><span data-stu-id="f3fad-144">az role assignment list</span></span>](/cli/azure/role/assignment#list)
* [<span data-ttu-id="f3fad-145">az 角色指派建立</span><span class="sxs-lookup"><span data-stu-id="f3fad-145">az role assignment create</span></span>](/cli/azure/role/assignment#create)
* [<span data-ttu-id="f3fad-146">az 角色指派刪除</span><span class="sxs-lookup"><span data-stu-id="f3fad-146">az role assignment delete</span></span>](/cli/azure/role/assignment#delete)

<span data-ttu-id="f3fad-147">服務主體的預設角色是**參與者**。</span><span class="sxs-lookup"><span data-stu-id="f3fad-147">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="f3fad-148">應用程式與 Azure 服務的互動可能並非最佳選擇，因為它所提供的權限很廣泛。</span><span class="sxs-lookup"><span data-stu-id="f3fad-148">It may not be the best choice for an app's interactions with Azure services, given its broad permissions.</span></span> <span data-ttu-id="f3fad-149">**讀取者**角色的權限較為侷限，因此很適合唯讀存取使用。</span><span class="sxs-lookup"><span data-stu-id="f3fad-149">The **Reader** role is more restrictive and is a good choice for read-only access.</span></span> <span data-ttu-id="f3fad-150">您可以透過 Azure 入口網站來檢視角色專屬權限的詳細資料，或建立自訂角色。</span><span class="sxs-lookup"><span data-stu-id="f3fad-150">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="f3fad-151">在此範例中，對先前的範例新增**讀取者**角色，並刪除**參與者**角色︰</span><span class="sxs-lookup"><span data-stu-id="f3fad-151">In this example, add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurecli-interactive
az role assignment create --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Reader
az role assignment delete --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Contributor
```

<span data-ttu-id="f3fad-152">列出目前指派的角色來確認變更︰</span><span class="sxs-lookup"><span data-stu-id="f3fad-152">Verify the changes by listing the currently assigned roles:</span></span>

```azurecli-interactive
az role assignment list --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d
```

```json
{
    "id": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac/providers/Microsoft.Authorization/roleAssignments/c27f78a7-9d3b-404b-ab59-47818f9af9ac",
    "name": "c27f78a7-9d3b-404b-ab59-47818f9af9ac",
    "properties": {
      "principalId": "790525226-46f9-4051-b439-7079e41dfa31",
      "principalName": "http://MyDemoWebApp",
      "roleDefinitionId": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac/providers/Microsoft.Authorization/roleDefinitions/acdd72a7-3385-48ef-bd42-f606fba81ae7",
      "roleDefinitionName": "Reader",
      "scope": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac"
    },
    "type": "Microsoft.Authorization/roleAssignments"
}
```

> [!NOTE] 
> <span data-ttu-id="f3fad-153">如果您的帳戶沒有足夠的權限可指派角色，您會看到一則錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="f3fad-153">If your account does not have sufficient permissions to assign a role, you see an error message.</span></span>
> <span data-ttu-id="f3fad-154">此訊息說明您的帳戶「沒有權限來對 '/subscriptions/{guid}' 範圍執行 'Microsoft.Authorization/roleAssignments/write' 動作」。</span><span class="sxs-lookup"><span data-stu-id="f3fad-154">The message states your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}'."</span></span>
   
## <a name="change-the-credentials-of-a-security-principal"></a><span data-ttu-id="f3fad-155">變更安全性主體的認證</span><span class="sxs-lookup"><span data-stu-id="f3fad-155">Change the credentials of a security principal</span></span>

<span data-ttu-id="f3fad-156">定期檢閱權限並更新密碼是很好的安全性作法。</span><span class="sxs-lookup"><span data-stu-id="f3fad-156">It's a good security practice to review permissions and update passwords regularly.</span></span> <span data-ttu-id="f3fad-157">您也可以在應用程式變更時，管理及修改您的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="f3fad-157">You may also want to manage and modify the security credentials as your app changes.</span></span>

### <a name="reset-a-service-principal-password"></a><span data-ttu-id="f3fad-158">重設服務主體密碼</span><span class="sxs-lookup"><span data-stu-id="f3fad-158">Reset a service principal password</span></span>

<span data-ttu-id="f3fad-159">使用 `az ad sp reset-credentials` 將目前的服務主體密碼進行重設。</span><span class="sxs-lookup"><span data-stu-id="f3fad-159">Use `az ad sp reset-credentials` to reset the current password for the service principal.</span></span>

```azurecli-interactive
az ad sp reset-credentials --name 20bce7de-3cd7-49f4-ab64-bb5b443838c3 --password {new-password}
```

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "name": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "password": {new-password},
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

<span data-ttu-id="f3fad-160">如果您省略 `--password` 選項，CLI 就會產生安全的密碼。</span><span class="sxs-lookup"><span data-stu-id="f3fad-160">The CLI generates a secure password if you leave out the `--password` option.</span></span>
