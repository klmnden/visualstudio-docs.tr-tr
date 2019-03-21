---
title: Visual Studio şablon bulma sorunlarını giderme | Microsoft Docs
ms.date: 01/02/2018
ms.topic: conceptual
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c98c13528facb08f475614a6cbca9cee3c426ef9
ms.sourcegitcommit: 3d37c2460584f6c61769be70ef29c1a67397cf14
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2019
ms.locfileid: "58323113"
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

4. Visual Studio'yu açın ve her iki şablon ağaçları başlatmak için yeni proje ve yeni öğe iletişim kutularında başlatın.

   Şablon günlük görüntülenir **%LOCALAPPDATA%\Microsoft\VisualStudio\15.0_[instanceid]\VsTemplateDiagnosticsList.csv** (InstanceId örneğinizin Visual Studio yükleme Kimliğine karşılık gelir). Her şablon ağaç başlatma için bu günlük girdileri ekler.

::: moniker-end

::: moniker range=">=vs-2019"

4. Visual Studio'yu açın ve her iki şablon ağaçları başlatmak için yeni proje ve yeni öğe iletişim kutularında başlatın.

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