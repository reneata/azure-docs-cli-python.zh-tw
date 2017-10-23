---
title: "使用 Azure CLI 2.0 來建立 Azure 服務主體"
description: "了解如何使用 Azure CLI 2.0 來為應用程式或服務建立服務主體。"
keywords: Azure CLI 2.0, Azure Active Directory, Azure Active directory, AD, RBAC
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 10/12/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: fab89cb8-dac1-4e21-9d34-5eadd5213c05
ms.openlocfilehash: 5ae8af014b821fe5297ea44056ef33c4570d1d47
ms.sourcegitcommit: 5cfbea569fef193044da712708bc6957d3fb557c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2017
---
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a>使用 Azure CLI 2.0 來建立 Azure 服務主體

如果您打算使用 Azure CLI 2.0 來管理應用程式或服務，請根據 Azure Active Directory (AAD) 服務主體 (而非您自己的認證) 來執行它。
本主題會逐步引導您使用 Azure CLI 2.0 來建立安全性主體。

> [!NOTE]
> 您也可以透過 Azure 入口網站來建立服務主體。
> 如需詳細資訊，請閱讀[使用入口網站來建立可存取資源的 Active Directory 應用程式和服務主體](/azure/azure-resource-manager/resource-group-create-service-principal-portal)。

## <a name="what-is-a-service-principal"></a>何謂「服務主體」？

Azure 服務主體是一項安全性識別，可供使用者所建立的應用程式、服務和自動化工具用來存取特定 Azure 資源。 您可以把它想成是具有特定角色的「使用者識別」(登入和密碼或憑證)，並具有受到嚴格控制的資源存取權限。 不同於一般的使用者識別，服務主體只需要能夠執行特定動作。 如果您只對服務主體授與它為了執行管理工作所需要的最低權限等級，它就能提高安全性。 

Azure CLI 2.0 支援建立以密碼為基礎的驗證認證，以及以憑證認證。 在本主題中，我們將討論這兩種認證。

## <a name="verify-your-own-permission-level"></a>確認您自己的權限等級

首先，您在 Azure Active Directory 和 Azure 訂用帳戶中都必須有足夠的權限。 具體來說，您必須能夠在 Active Directory 中建立應用程式，並將角色指派給服務主體。 

檢查您的帳戶是否具有足夠的權限，最簡單的方式是透過入口網站。 請參閱[在入口網站中檢查必要的權限](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)。

## <a name="create-a-service-principal-for-your-application"></a>建立應用程式的服務主體

如需識別您想要建立服務主體的應用程式，您必須具有下列其中一項︰

  * 已部署之應用程式的唯一名稱或 URI (例如範例中的 "MyDemoWebApp")，或是
  * 應用程式識別碼；與您已部署的應用程式、服務或物件相關聯的唯一 GUID

建立服務主體時，這些值會識別您的應用程式。

### <a name="get-information-about-your-application"></a>取得應用程式的相關資訊

使用 `az ad app list` 來取得您應用程式的身分識別資訊。

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

`--display-name` 選項會篩選傳回的應用程式清單，來顯示以 MyDemoWebApp 為開頭且具有 `displayName` 的項目。

### <a name="create-a-service-principal-with-a-password"></a>使用密碼建立服務主體

使用 [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) 和 `--password` 參數，透過密碼建立服務主題。 若未提供角色或範圍，則目前的訂用帳戶會預設為**參與者**角色。 若您使用 `--password` 或 `--cert` 參數建立服務主體，則會使用密碼驗證，則系統會產生一組密碼給您。

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
 > 請勿建立不安全的密碼。  請依照 [Azure AD 密碼規則和限制](/azure/active-directory/active-directory-passwords-policy)指引。

### <a name="create-a-service-principal-with-a-self-signed-certificate"></a>使用自我簽署憑證建立服務主體

使用 [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) 和 `--create-cert` 參數建立自我簽署憑證。

```azurecli-interactive
az ad sp create-for-rbac --name {appId} --create-cert
```

```json
{
  "appId": "c495db57-82e0-4e2e-9369-069dff176858",
  "displayName": "azure-cli-2017-10-12-22-15-38",
  "fileWithCertAndPrivateKey": "<path>/<file-name>.pem",
  "name": "http://MyDemoWebApp",
  "password": null,
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

複製 `fileWithCertAndPrivateKey` 回應的值。 這是驗證會使用的憑證檔案。

如需使用憑證的更多選項，請參閱 [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac)。

### <a name="get-information-about-the-service-principal"></a>取得服務主體的相關資訊

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

### <a name="sign-in-using-the-service-principal"></a>使用服務主體來登入

您現在可以使用 `az ad sp show` 的 *appId*，或*密碼*或已建立憑證的路徑，以新服務主體登入您的應用程式。  提供 `az ad sp create-for-rbac` 結果中的租用戶值。

```azurecli-interactive
az login --service-principal -u a487e0c1-82af-47d9-9a0b-af184eb87646d --password {password-or-path-to-cert} --tenant {tenant}
``` 

成功登入之後，您會看到此輸出︰

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

使用 `id`、`password` 和 `tenant` 值，作為執行您應用程式的認證。 

## <a name="managing-roles"></a>管理角色 

> [!NOTE]
> Azure 角色型存取控制 (RBAC) 是一種可定義及管理使用者和服務主體角色的模型。
> 角色會有一組相關聯的權限，以決定主體可以讀取、存取、寫入或管理的資源。
> 如需 RBAC 和角色的詳細資訊，請參閱 [RBAC：內建角色](/azure/active-directory/role-based-access-built-in-roles)。

Azure CLI 2.0 提供下列命令以供您管理角色指派︰

* [az 角色指派清單](/cli/azure/role/assignment#list)
* [az 角色指派建立](/cli/azure/role/assignment#create)
* [az 角色指派刪除](/cli/azure/role/assignment#delete)

服務主體的預設角色是**參與者**。 應用程式與 Azure 服務的互動可能並非最佳選擇，因為它所提供的權限很廣泛。 **讀取者**角色的權限較為侷限，因此很適合唯讀存取使用。 您可以透過 Azure 入口網站來檢視角色專屬權限的詳細資料，或建立自訂角色。

在此範例中，對先前的範例新增**讀取者**角色，並刪除**參與者**角色︰

```azurecli-interactive
az role assignment create --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Reader
az role assignment delete --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Contributor
```

列出目前指派的角色來確認變更︰

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
> 如果您的帳戶沒有足夠的權限可指派角色，您會看到一則錯誤訊息。
> 此訊息說明您的帳戶「沒有權限來對 '/subscriptions/{guid}' 範圍執行 'Microsoft.Authorization/roleAssignments/write' 動作」。
   
## <a name="change-the-credentials-of-a-security-principal"></a>變更安全性主體的認證

定期檢閱權限並更新密碼是很好的安全性作法。 您也可以在應用程式變更時，管理及修改您的安全性認證。

### <a name="reset-a-service-principal-password"></a>重設服務主體密碼

使用 `az ad sp reset-credentials` 將目前的服務主體密碼進行重設。

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

如果您省略 `--password` 選項，CLI 就會產生安全的密碼。
