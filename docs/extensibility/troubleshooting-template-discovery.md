---
title: Visual Studio şablon bulma sorunlarını giderme | Microsoft Docs
ms.date: 01/02/2018
ms.topic: conceptual
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d9ae6220ac38de7bf2edc7b5c305ecb377a46f18
ms.sourcegitcommit: 11337745c1aaef450fd33e150664656d45fe5bc5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57324006"
---
# <a name="troubleshooting-template-installation"></a>Şablon yükleme sorunlarını giderme

Proje veya öğe şablonlarınızın dağıtımı sorunlarla karşılaşırsanız, tanılama günlük kaydını etkinleştirebilirsiniz.

::: moniker range="vs-2017"

1. Pkgdef dosyasını içinde oluşturmak *Common7\IDE\CommonExtensions* yüklemenizin klasör. Örneğin, *C:\Program Files (x86) \Microsoft Visual Studio\2017\Enterprise\Common7\IDE\CommonExtensions\EnablePkgDefLogging.pkgdef*.

::: moniker-end

::: moniker range=">=vs-2019"

1. Pkgdef dosyasını içinde oluşturmak *Common7\IDE\CommonExtensions* yüklemenizin klasör. Örneğin, *C:\Program Files (x86) \Microsoft Visual Studio\2019\Enterprise\Common7\IDE\CommonExtensions\EnablePkgDefLogging.pkgdef*.

::: moniker-end

2. Pkgdef dosyasına aşağıdakileri ekleyin:

    ```
    [$RootKey$\VsTemplate]
    "EnableTemplateDiscoveryLog"=dword:00000001
    ```

3. Açık bir [Geliştirici komut istemi](/dotnet/framework/tools/developer-command-prompt-for-vs) yükleme ve çalıştırma `devenv /updateConfiguration`.

::: moniker range="vs-2017"

4. Visual Studio'yu başlatın ve her iki şablon ağaçları başlatmak için yeni proje ve yeni öğe iletişim kutularında başlatın.

   Şablon günlük görüntülenir **%LOCALAPPDATA%\Microsoft\VisualStudio\15.0_[instanceid]\VsTemplateDiagnosticsList.csv** (InstanceId örneğinizin Visual Studio yükleme Kimliğine karşılık gelir). Her şablon ağaç başlatma için bu günlük girdileri ekler.

::: moniker-end

::: moniker range=">=vs-2019"

4. Visual Studio'yu başlatın ve her iki şablon ağaçları başlatmak için yeni proje ve yeni öğe iletişim kutularında başlatın.

   Şablon günlük görüntülenir **%LOCALAPPDATA%\Microsoft\VisualStudio\16.0_[instanceid]\VsTemplateDiagnosticsList.csv** (InstanceId örneğinizin Visual Studio yükleme Kimliğine karşılık gelir). Her şablon ağaç başlatma için bu günlük girdileri ekler.

::: moniker-end

Günlük dosyası şu sütunları içerir:

- **FullPathToTemplate**, aşağıdaki değerleri vardır:

    - bildirim tabanlı bir dağıtım için 1

    - disk tabanlı bir dağıtım için 0

- **TemplateFileName**

- Diğer şablonu özellikleri

> [!NOTE]
> Günlüğü devre dışı bırakmak pkgdef dosyayı kaldırın veya değiştirin `EnableTemplateDiscoveryLog` için `dword:00000000`ve ardından çalıştırın `devenv /updateConfiguration` yeniden.

## <a name="see-also"></a>Ayrıca bkz.

- [Özel proje ve öğe şablonları oluşturma](creating-custom-project-and-item-templates.md)