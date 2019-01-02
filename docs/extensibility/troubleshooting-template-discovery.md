---
title: Visual Studio şablon bulma sorunlarını giderme | Microsoft Docs
ms.date: 01/02/2018
ms.topic: conceptual
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 39ebb7c49e5a8482ab0b2ef5c3a5257d0237b39c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53836159"
---
# <a name="troubleshooting-template-installation"></a>Şablon yükleme sorunlarını giderme

Proje veya öğe şablonlarınızın dağıtımı sorunlarla karşılaşırsanız, tanılama günlük kaydını etkinleştirebilirsiniz.

1. Aşağıdaki içeriklerle Common7\IDE\CommonExtensions klasöründeki pkgdef dosyasını yüklemenizin (örneğin C:\Program Files (x86) \Microsoft Visual Studio\2017\Enterprise\Common7\IDE\CommonExtensions\EnablePkgDefLogging.pkgdef) oluşturun:

    ```
    [$RootKey$\VsTemplate]
    "EnableTemplateDiscoveryLog"=dword:00000001
    ```

1. Windows Search'te arayarak yüklemenizde "Geliştirici komut istemi" açın ve çalıştırın `devenv /updateConfiguration`.

1. Visual Studio'yu başlatın ve her iki şablon ağaçları başlatmak için yeni proje ve yeni öğe iletişim kutularında başlatın. Şablon günlük görüntülenir **%LOCALAPPDATA%\Microsoft\VisualStudio\15.0_[instanceid]\VsTemplateDiagnosticsList.csv** (InstanceId örneğinizin Visual Studio yükleme Kimliğine karşılık gelir). Her şablon ağaç başlatma için bu günlük girdileri ekler.

Günlük dosyası şu sütunları içerir:

- **FullPathToTemplate**, aşağıdaki değerleri vardır:

    - bildirim tabanlı bir dağıtım için 1

    - disk tabanlı bir dağıtım için 0

- **TemplateFileName**

- Diğer şablonu özellikleri

> [!NOTE]
> Günlüğü devre dışı bırakmak pkgdef dosyayı kaldırın veya değiştirin `EnableTemplateDiscoveryLog` için `dword:00000000`ve ardından çalıştırın `devenv /updateConfiguration` yeniden.

## <a name="see-also"></a>Ayrıca bkz.

[Özel proje ve öğe şablonları oluşturma](creating-custom-project-and-item-templates.md)