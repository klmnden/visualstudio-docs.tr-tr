---
title: Kullanıcı ayarları Store için yazma | Microsoft Docs
ms.date: 05/23/2019
ms.topic: conceptual
ms.assetid: efd27f00-7fe5-45f8-9b97-371af732be97
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fe8187fe11f4818433aed847a7bc67d4a889ad3a
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66206877"
---
# <a name="writing-to-the-user-settings-store"></a>Kullanıcı Ayarları Deposuna Yazma
Kullanıcı ayarları benzeyen yazılabilir ayarlarıdır **Araçlar / Seçenekler** iletişim ve özellikleri windows belirli bir iletişim kutusu. Visual Studio uzantıları bunlar küçük miktarlarda veri depolamak için kullanabilirsiniz. Bu izlenecek yolda not defteri için Visual Studio dış bir araç olarak okuma ve kullanıcı ayarları deposuna yazma tarafından nasıl ekleneceğini gösterir.

## <a name="writing-to-the-user-settings-store"></a>Kullanıcı Ayarları Deposuna Yazma

1. UserSettingsStoreExtension adlı bir VSIX projesi oluşturun ve ardından UserSettingsStoreCommand adlı özel bir komut ekleyin. Özel komut oluşturma hakkında daha fazla bilgi için bkz. [bir menü komutuyla uzantı oluşturma](../extensibility/creating-an-extension-with-a-menu-command.md)

2. UserSettingsStoreCommand.cs içinde aşağıdaki ekleme using deyimlerini:

    ```csharp
    using System.Collections.Generic;
    using Microsoft.VisualStudio.Settings;
    using Microsoft.VisualStudio.Shell.Settings;
    ```

3. MenuItemCallback, yöntem gövdesi silme ve kullanıcı ayarlarını depolamak, aşağıdaki gibi alır:

    ```csharp
    private void MenuItemCallback(object sender, EventArgs e)
    {
        SettingsManager settingsManager = new ShellSettingsManager(ServiceProvider);
        WritableSettingsStore userSettingsStore = settingsManager.GetWritableSettingsStore(SettingsScope.UserSettings);
    }
    ```

4. Artık, Not Defteri zaten dış bir araç olarak ayarlanmasına bulun. İle tüm dış araçları ToolCmd ayarı "Not", şu şekilde olup olmadığını belirlemek için yineleme yapmanız gerekir:

    ```csharp
    private void MenuItemCallback(object sender, EventArgs e)
    {
        SettingsManager settingsManager = new ShellSettingsManager(ServiceProvider);
        WritableSettingsStore userSettingsStore = settingsManager.GetWritableSettingsStore(SettingsScope.UserSettings);

        // Find out whether Notepad is already an External Tool.
        int toolCount = userSettingsStore.GetInt32("External Tools", "ToolNumKeys");
        bool hasNotepad = false;
        CompareInfo Compare = CultureInfo.InvariantCulture.CompareInfo;
        for (int i = 0; i < toolCount; i++)
        {
            if (Compare.IndexOf(userSettingsStore.GetString("External Tools", "ToolCmd" + i), "Notepad", CompareOptions.IgnoreCase) >= 0)
            {
                hasNotepad = true;
                break;
            }
        }
    }

    ```

5. Not Defteri'ni dış bir araç olarak ayarlanmamışsa, aşağıdaki gibi ayarlayın:

    ```vb
    private void MenuItemCallback(object sender, EventArgs e)
    {
        SettingsManager settingsManager = new ShellSettingsManager(ServiceProvider);
        WritableSettingsStore userSettingsStore = settingsManager.GetWritableSettingsStore(SettingsScope.UserSettings);

        // Find out whether Notepad is already installed.
        int toolCount = userSettingsStore.GetInt32("External Tools", "ToolNumKeys");
        bool hasNotepad = false;
        CompareInfo Compare = CultureInfo.InvariantCulture.CompareInfo;
        for (int i = 0; i < toolCount; i++)
        {
            if (Compare.IndexOf(userSettingsStore.GetString("External Tools", "ToolCmd" + i), "Notepad", CompareOptions.IgnoreCase) >= 0)
            {
                hasNotepad = true;
                break;
            }
        }

        string message = (hasNotepad) ? "Notepad already installed" : "Installing Notepad";
         if (!hasNotepad)
        {
            userSettingsStore.SetString("External Tools", "ToolTitle" + toolCount, "&Notepad");
            userSettingsStore.SetString("External Tools", "ToolCmd" + toolCount, "C:\\Windows\\notepad.exe");
            userSettingsStore.SetString("External Tools", "ToolArg" + toolCount, "");
            userSettingsStore.SetString("External Tools", "ToolDir" + toolCount, "$(ProjectDir)");
            userSettingsStore.SetString("External Tools", "ToolSourceKey" + toolCount, "");
            userSettingsStore.SetUInt32("External Tools", "ToolOpt" + toolCount, 0x00000011);

            userSettingsStore.SetInt32("External Tools", "ToolNumKeys", toolCount + 1);
        }
    }
    ```

6. Kodu test edin. İkinci kez çalıştırmadan önce kayıt defterini geri alma işlemleri gerekir böylece onu dış bir araç olarak not defteri ekler unutmayın.

7. Kodu derlemek ve hata ayıklamaya başlayın.

8. Üzerinde **Araçları** menüsünde tıklatın **çağırma UserSettingsStoreCommand**. Bu Not Defteri'ne ekler **Araçları** menüsü.

9. Not Defteri'ni araçları görürsünüz / Seçenekler menüsü ve tıklayarak **not defteri** bir not defteri örneği ayarlama duruma getirmeniz gerekir.