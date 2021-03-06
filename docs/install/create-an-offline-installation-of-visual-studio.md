---
title: "Create an Offline Installation of Visual Studio"
description: "Learn how to install Visual Studio offline when you have an unreliable internet connection or low bandwidth."
ms.custom: ""
ms.date: 08/28/2018
ms.technology: vs-acquisition
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
  - "offline installation [Visual Studio]"
  - "offline install [Visual Studio]"
  - "layout [Visual Studio]"
ms.assetid: f8625d5e-f6ea-4db0-83c0-619b77fab3cf
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
  - "multiple"
---
# Create an offline installation of Visual Studio 2017

We designed Visual Studio 2017 to work well in a variety of network and computer configurations. While we recommend that you try the [Visual Studio web installer](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)&mdash;which is a small file and allows you to stay current with all the latest fixes and features&mdash;we understand that you might not be able to.

For example, you might have an unreliable internet connection or one that has low bandwidth. If so, you have a few options: You can use the new "Download all, then install" feature to download the files before you install, or you can use the command line to create a local cache of the files.

> [!NOTE]
> If you are an enterprise administrator who wants to perform a deployment of Visual Studio 2017 to a network of client workstations that are firewalled from the internet, see our [Create a network installation of Visual Studio 2017](../install/create-a-network-installation-of-visual-studio.md) and [Install certificates required for Visual Studio offline installation](../install/install-certificates-for-visual-studio-offline.md) pages.

## Use the "Download all, then install" feature

[**New in 15.8**](/visualstudio/releasenotes/vs2017-relnotes?context=visualstudio/default&view=vs-2017#install
): After you download the web installer, select the new **Download all, then install** option from the Visual Studio Installer. Then, continue with your installation.

   ![The "Download all, then install" option](media/download-all-then-install.png)

## Use the command line to create a local cache

After you download a small bootstrapper, use the command line to create a local cache. Then, use the local cache to install Visual Studio. (This process replaces the ISO files that were available for previous versions.)

Here's how.

### Step 1 - Download the Visual Studio bootstrapper

You must have an internet connection to complete this step.

Start by downloading the Visual Studio bootstrapper for your chosen edition of Visual Studio. Your setup file&mdash;or bootstrapper&mdash;will match or be similar to one of the following.

| Edition                    | File                                                                    |
|----------------------------|-------------------------------------------------------------------------|
| Visual Studio Community    | [vs_community.exe](https://aka.ms/vs/15/release/vs_community.exe)       |
| Visual Studio Professional | [vs_professional.exe](https://aka.ms/vs/15/release/vs_professional.exe) |
| Visual Studio Enterprise   | [vs_enterprise.exe](https://aka.ms/vs/15/release/vs_enterprise.exe)     |

### Step 2 - Create a local install cache

You must have an internet connection to complete this step.

Open a command prompt and use one of the commands from the following examples. The examples that are listed here assume that you're using the Community edition of Visual Studio; adjust the command as appropriate for your edition.

- For .NET web and .NET desktop development, run:

   ```vs_community.exe --layout c:\vs2017layout --add Microsoft.VisualStudio.Workload.ManagedDesktop --add Microsoft.VisualStudio.Workload.NetWeb --add Component.GitHub.VisualStudio --includeOptional --lang en-US```

- For .NET desktop and Office development, run:

   ```vs_community.exe --layout c:\vs2017layout --add Microsoft.VisualStudio.Workload.ManagedDesktop --add Microsoft.VisualStudio.Workload.Office --includeOptional --lang en-US```

- For C++ desktop development, run:

   ```vs_community.exe --layout c:\vs2017layout --add Microsoft.VisualStudio.Workload.NativeDesktop --includeRecommended --lang en-US```

- To create a complete local layout with all features (this will take a long time&mdash;we have _lots_ of features!), run:

   ```vs_community.exe --layout c:\vs2017layout --lang en-US```

If you want to install a language other than English, change `en-US` to a locale from the [List of language locales](#list-of-language-locales). Then, use the [list of the components and workloads available](workload-and-component-ids.md) to further customize your installation cache.

> [!IMPORTANT]
> A complete Visual Studio 2017 layout requires at least 35 GB of disk space and can take some time to download. See [Use command-line parameters to install Visual Studio 2017](use-command-line-parameters-to-install-visual-studio.md) for information on how to create a layout with only the components you want to install.

### Step 3 - Install Visual Studio from the local cache

> [!TIP]
> When you run from a local install cache, setup uses the local versions of each of these files. But if you select components during installation that aren't in the cache, setup attempts to download them from the internet.

To make sure that you install only the files that you've previously downloaded, use the same command-line options that you used to create the layout cache. For example, if you created a layout cache with the following command:

```vs_community.exe --layout c:\vs2017layout --add Microsoft.VisualStudio.Workload.ManagedDesktop --add Microsoft.VisualStudio.Workload.NetWeb --add Component.GitHub.VisualStudio --includeOptional --lang en-US```

Then use this command to run the installation:

```c:\vs2017layout\vs_community.exe --add Microsoft.VisualStudio.Workload.ManagedDesktop --add Microsoft.VisualStudio.Workload.NetWeb --add Component.GitHub.VisualStudio --includeOptional```

> [!NOTE]
> If you get an error that a signature is invalid, you must install updated certificates. Open the Certificates folder in your offline cache. Double-click each of the certificate files, and then click through the Certificate Manager wizard. If you're asked for a password, leave it blank.

### List of language locales

| **Language-locale** | **Language** |
| ----------------------- | --------------- |
| cs-CZ | Czech |
| de-DE | German |
| en-US | English |
| es-ES | Spanish |
| fr-FR | French |
| it-IT | Italian |
| ja-JP | Japanese |
| ko-KR | Korean |
| pl-PL | Polish |
| pt-BR | Portuguese - Brazil |
| ru-RU | Russian |
| tr-TR | Turkish |
| zh-CN | Chinese - Simplified |
| zh-TW | Chinese - Traditional |

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## See also

- [Create a network installation of Visual Studio 2017](../install/create-a-network-installation-of-visual-studio.md)
- [Install certificates required for Visual Studio offline installation](../install/install-certificates-for-visual-studio-offline.md)
- [Use command-line parameters to install Visual Studio](use-command-line-parameters-to-install-visual-studio.md)
- [Visual Studio 2017 workload and component IDs](workload-and-component-ids.md)
