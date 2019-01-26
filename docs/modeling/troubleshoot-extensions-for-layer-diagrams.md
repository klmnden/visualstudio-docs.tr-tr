---
title: Bağımlılık diyagramları için uzantı sorunlarını giderme
ms.date: 11/04/2016
ms.topic: troubleshooting
helpviewer_keywords:
- dependency diagrams, extension errors
- dependency diagrams, troubleshooting extensions
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: 01b8486c9ca0ffc62d338b9d9a46e50248182581
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55028601"
---
# <a name="troubleshoot-extensions-for-dependency-diagrams"></a>Bağımlılık diyagramları için uzantı sorunlarını giderme

Bu konuda, katman model uzantıları oluştururken karşılaşabileceğiniz bazı sorunlar ele alınmaktadır.

## <a name="when-i-press-f5-to-debug-my-extension-my-commands-gesture-handlers-validation-extensions-or-custom-properties-do-not-appear-on-dependency-diagrams-in-the-experimental-instance-of-visual-studio"></a>Uzantımı ayıklamak için F5 tuşuna bastığımda, komutları, hareket işleyicileri, doğrulama uzantıları veya özel özellikler Visual Studio'nun deneysel örneğinde bağımlılık diyagramlarında görünmez.

1. Uzantı çözümünüzü üzerinde ve Visual Studio'nun deneysel örneğinde açın **derleme** menüsünde tıklatın **çözümü yeniden derle**.

2. Tuşuna **F5** veya **CTRL + F5** Visual Studio'nun deneysel örneği başlatmak için. Bir bağımlılık diyagramı açın ve uzantınızı sınayın.

   Gerekirse, sonraki yordama geçin.

## <a name="an-old-version-of-my-extension-runs"></a>Uzantım eski bir sürümünü çalıştırır.

1. Hiçbir Visual Studio'nun Deneysel örneğinin çalıştığından emin olun.

2. Aşağıdaki klasörü silin: %LocalAppData%\Microsoft\VisualStudio\\[sürüm] \ComponentModelCache

   > [!NOTE]
   > % LocalAppData %, genellikle *DriveName*: \Users\\*kullanıcıadı*\AppData\Local.

   Gerekirse, sonraki yordama geçin.

## <a name="an-old-version-of-my-validation-results-appears-or-my-validation-method-is-not-called"></a>Doğrulama sonuçlarımın eski bir sürümü görünüyor veya doğrulama Yöntemim çağrılmıyor.

1.  Visual Studio'nun Deneysel örneğinin üzerinde **derleme** menüsünde tıklatın **çözümü Temizle**. Bu, önceki doğrulama analizinin önbelleğe alınan sonuçlarını temizler.

2.  Modelinizdeki katmanların kod öğeleriyle ilişkili olduğundan ve modelde en az bir bağımlılık bağlantısı olduğundan emin olun. Doğrulanacak bir şey yoksa, doğrulama çağrılmaz.

3.  Ayrı bir işlemde çalıştığından, bir doğrulama yönteminde normal kesme noktaları çalışmayabilir. Bir çağrı eklemeniz gerekir `System.Diagnostics.Debugger.Launch()` yönteminizde ilerlemek istiyorsanız.

4.  İçinde **source.extension.vsixmanifest** katman doğrulama projenizdeki her ikisi de eklediğinizden emin olun bir **MEF Bileşeni** öğesi ve bir **özel uzantı türü** altında öğesi **İçerik**.

## <a name="see-also"></a>Ayrıca Bkz.

- [Bağımlılık diyagramlarını genişletme](../modeling/extend-layer-diagrams.md)
