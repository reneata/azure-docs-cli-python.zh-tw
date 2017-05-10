---
title: "安裝 Azure CLI 2.0"
description: "Azure CLI 2.0 的參考文件"
keywords: "Azure CLI 2.0、Azure CLI 2.0 參考、安裝 Azure CLI 2.0、Azure Python CLI、解除安裝 Azure CLI 2.0"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/06/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: b7c0b7c50794333b28c034de9b41f1e506053e25
ms.sourcegitcommit: 663d4188ccc4be425d3d551fe32613fafd05a764
ms.translationtype: HT
ms.contentlocale: zh-TW
---
# <a name="install-azure-cli-20"></a>安裝 Azure CLI 2.0

立即安裝新版 Azure CLI！
我們已改進並更新此版本，以提供絕佳的原生命令列，讓您管理 Azure 資源。
它可以用於 macOS、Linux 和 Windows。
如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azure-cli.md)。

> [!NOTE]
> 如果您需要舊版 Azure CLI，此處提供 [安裝 Azure 1.0](/azure/cli-install-nodejs) 的方法。

## <a name="macos"></a>macOS

1. 使用 `curl` 命令來安裝 Azure CLI 2.0。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. 您可能必須重新啟動命令殼層，某些變更才會生效。

   ```bash
   exec -l $SHELL
   ```
   
3. 從具有 `az` 命令的命令提示字元中執行 Azure CLI 2.0。

> [!Note]
> 當您使用 InstallAzureCli 安裝時，`az component update` 不受支援。
> 若要更新為最新的 CLI，請再次執行 `curl -L https://aka.ms/InstallAzureCli | bash`。
> 
> 若要解除安裝，請參閱 [手動解除安裝說明](#uninstall)。

## <a name="windows"></a>Windows

Azure CLI 2.0 支援 Bash 命令語法，讓 Windows 上的 Ubuntu 上的 Bash 成為使用 CLI 的好方法。
如果您不是使用 Bash，可以使用 Windows 命令列安裝並使用 CLI。

### <a name="bash-on-ubuntu-on-windows"></a>在 Windows 上 Ubuntu 上的 Bash

1. 如果在 Windows 上沒有 Bash，請[安裝它](https://msdn.microsoft.com/commandline/wsl/install_guide)。

2. 開啟 Bash 殼層。

3. 如果沒有 Python，請加以安裝。

   ```bash
   sudo apt-get install python3
   ```

   > [!NOTE]
   > 若要查看是否有安裝 python，請執行 `python --version`。

4. 修改來源清單。

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

5. 執行下列 sudo 命令：

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> 當您使用 apt-get 進行安裝時，`az component` 不受支援。
> 若要更新 CLI，請再次執行 `sudo apt-get update && sudo apt-get install azure-cli`。
> 
> 若要解除安裝，請執行 `sudo apt-get remove azure-cli`。

### <a name="windows-command-line"></a>Windows 命令列 

1. 請瀏覽 Python 網站和 [下載適用於 Windows 的 Python](https://www.python.org/downloads/)。
   安裝 Python 時，請務必安裝 Pip 元件。
   安裝完成後，將 Python 新增至 PATH 環境變數 (安裝程式會提示您)。

2. 透過命令提示字元檢查 Python 安裝。

   ```bash
   python --version
   ```

3. 使用 `pip` 安裝 Azure CLI 2.0。

   ```bash
   pip install --user azure-cli
   ```

4. 將含 az.bat 的資料夾加入至您的路徑。
   CLI `az.bat` 可能安裝在 `%USERPROFILE%\AppData\Roaming\Python\Scripts` 或 `%USERPROFILE%\AppData\Roaming\Python\PythonXY\Scripts`，其中 `XY` 是 Python 版本 (例如，`%USERPROFILE%\AppData\Roaming\Python\Python27\Scripts`)。
   將含 `az.bat` 的資料夾加入至您的路徑。
   
4. 從具有 `az` 命令的命令提示字元中執行 Azure CLI 2.0。

> [!NOTE]
> 如果您已安裝 Azure CLI 2.0，且想要查看您是否擁有最新版本，使用 `az --version` 來查看您擁有的版本。
> 請將其與 [https://pypi.python.org/pypi/azure-cli](https://pypi.python.org/pypi/azure-cli)中可用的最新版本相比較。
> 
> 若要更新為最新的 CLI，請執行 `az component update`。
> 
> 若要解除安裝 CLI 時，請執行`pip uninstall azure-cli`。

## <a name="linux"></a>Linux

1. 在 Linux 上，您可能需要安裝特定的 [必要條件](#linux-prerequisites)。

2. 使用 `curl` 命令來安裝 Azure CLI 2.0。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. 您可能必須重新啟動命令殼層，某些變更才會生效。

   ```bash
   exec -l $SHELL
   ```

4. 從具有 `az` 命令的命令提示字元中執行 Azure CLI 2.0。

> [!Note]
> 當您使用 InstallAzureCli 安裝時，`az component update` 不受支援。
> 若要更新為最新的 CLI，請再次執行 `curl -L https://aka.ms/InstallAzureCli | bash`。
> 
> 若要解除安裝，請參閱 [手動解除安裝說明](#uninstall)。

## <a name="docker"></a>Docker

我們會維護使用 Azure CLI 預先設定的 Docker 映像。

使用 `docker run` 安裝 Azure CLI。

```bash
docker run azuresdk/azure-cli-python:<version>
```

請參閱我們的 [Docker 標籤](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)，以取得可用的版本。

> [!NOTE]
> 如果您想要從使用者環境挑選 SSH 金鑰，可以使用 `-v ${HOME}:/root` 來裝載 $HOME 作為 `/root`。
>
> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

> [!NOTE]
> Docker 映像不支援 [`component`功能](/cli/azure/component)。
> 若要更新 Azure CLI 2.0，請使用 `docker run` 來安裝最新的映像或您想要的特定映像。

## <a name="apt-get"></a>apt-get

以 Debian/Ubuntu 為基礎的系統，您可以透過 `apt-get` 安裝 Azure CLI 2.0。

1. 修改來源清單。

   - 32 位元系統

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - 64 位元系統

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. 執行下列 sudo 命令：

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> 當您使用 apt-get 進行安裝時，`az component` 不受支援。
> 若要更新 CLI，請再次執行 `sudo apt-get update && sudo apt-get install azure-cli`。
> 
> 若要解除安裝，請執行 `sudo apt-get remove azure-cli`。

## <a name="linux-prerequisites"></a>Linux 必要條件

1. 如果沒有 Python，請[安裝](https://www.python.org/downloads)。

2. 根據您的 Linux 散發套件，安裝必要條件。

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install gcc libffi-devel python-devel openssl-devel
   ```

## <a name="troubleshooting"></a>疑難排解
-------------------------------

### <a name="errors-with-curl-redirection"></a>使用 curl 重新導向時發生的錯誤

如果您收到與 `-L` 參數有關，來自 `curl` 命令的錯誤，或者是某錯誤指出「物件已移動」，請嘗試使用完整的 url，而非 aka.ms url：

```
# If you see this:
curl -L https://aka.ms/InstallAzureCli | bash
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   175  100   175    0     0    562      0 --:--:-- --:--:-- --:--:--   560
bash: line 1: syntax error near unexpected token `<'
'ash: line 1: `<html><head><title>Object moved</title></head><body>

#### Try this instead:
curl https://azurecliprod.blob.core.windows.net/install | bash
```


### <a name="errors-on-install-with-cffi-or-cryptography"></a>使用 `cffi` 安裝或加密時發生錯誤

如果您在 OS X 上安裝時發生錯誤，請升級 `pip`。

```bash
pip install --upgrade --force-reinstall pip
```

如果如同這些範例，在 **Debian** 或 **Ubuntu** 上安裝時發生錯誤，請安裝 `libssl-dev` 和 `libffi-dev`。

```bash
sudo apt-get update
sudo apt-get install -y libssl-dev libffi-dev
```

同時安裝適用於您 Python 版本的 Python Dev。

Python 2：

```bash
sudo apt-get install -y python-dev
```

Python 3：

```bash
sudo apt-get install -y python3-dev
```

Ubuntu 15 也可能需要 `build-essential`︰

```bash
sudo apt-get install -y build-essential
```

### <a name="example-errors"></a>範例錯誤

```
Downloading cffi-1.5.2.tar.gz (388kB)
    100% |################################| 389kB 3.9MB/s
    Complete output from command python setup.py egg_info:

        No working compiler found, or bogus compiler options
        passed to the compiler from Python's distutils module.
        See the error messages above.
        (If they are about -mno-fused-madd and you are on OS/X 10.8,
        see http://stackoverflow.com/questions/22313407/ .)

    ----------------------------------------
Command "python setup.py egg_info" failed with error code 1 in /tmp/pip-build-77i2fido/cffi/
```

```
#include <openssl/e_os2.h>
                            ^
compilation terminated.
error: command 'x86_64-linux-gnu-gcc' failed with exit status 1

Failed building wheel for cryptography
```

請參閱 Stack Overflow 的問題 - [無法使用 PIP 和 setup.py 安裝 Python 加密套件](http://stackoverflow.com/questions/22073516/failed-to-install-python-cryptography-package-with-pip-and-setup-py)

## <a name="uninstall"></a>解除安裝

如果您使用在 https://aka.ms/InstallAzureCli 的指令碼安裝 CLI，您可以利用下列步驟進行解除安裝。

1. 移除已安裝的檔案。

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. 將 `<install location>/lib/azure-cli/az.completion` 行從 `<install location>/.bash_profile` 刪除。

> [!Note]
> 預設安裝位置是 `/Users/<username>`。

如果您使用 pip、apt-get 或 Docker 安裝 CLI 時，請使用相同的工具進行解除安裝。

## <a name="reporting-issues-and-feedback"></a>報告問題和意見反應

如果您遇到任何與工具有關的錯誤，請在 GitHub 存放庫的[問題](https://github.com/Azure/azure-cli/issues)一節中提出問題。
若要透過命令行提供意見反應，請嘗試 `az feedback` 命令。
