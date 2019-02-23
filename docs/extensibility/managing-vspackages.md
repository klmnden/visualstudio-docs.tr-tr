---
title: VSPackage'ları yönetme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSPackages, autoloading
- VSPackages, delayed loading
- delay loading
- VSPackages, loading
ms.assetid: 386e0ce5-4107-4164-b0cd-1cf43eb5e7cf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a316d2af6ecb76c573cfb43e1334df1933a2989b
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56694718"
---
# <a name="manage-vspackages"></a>VSPackage'ları yönetme
Çoğu durumda VSPackages, proje ve öğe şablonlarını kaydetme ve paket otomatik olarak yük yönetilmesi konusunda endişelenmesine gerek yoktur. Ancak, bazı durumlarda, paket yönetmek için biraz daha fazla bilgi edinmek gerekebilir.

## <a name="use-the-experimental-instance"></a>Deneysel örneğini kullan
 Deneysel örnek hakkında daha fazla bilgi için bkz. [deneysel örneğinde](../extensibility/the-experimental-instance.md).

## <a name="register-and-unregister-vspackages"></a>Kaydolun ve VSPackage kaydı
 Kaydolun ve VSPackages ve diğer tür uzantılarla kaydı konusunda bilgi edinmek için bkz: [kaydedin ve VSPackage kaydı](../extensibility/registering-and-unregistering-vspackages.md).

## <a name="load-a-vspackage"></a>VSPackage yükleme
 VSPackage sorsorgu CMDUICONTEXT GUID açık belirli bir zaman için ayarlanabilir. Daha fazla bilgi için [yük VSPackages](../extensibility/loading-vspackages.md).

## <a name="use-asyncpackage-to-load-vspackages-in-the-background"></a>Arka planda VSPackage yükleme için AsyncPackage kullanın
 `AsyncPackage` Paketi yükleme için Visual Studio kullanıcı Arabirimi yanıt sürelerinde arka plan iş parçacığında sınıfı sağlar. Daha fazla bilgi için [nasıl yapılır: Arka planda VSPackage AsyncPackage sayfanızdaki](../extensibility/how-to-use-asyncpackage-to-load-vspackages-in-the-background.md).

## <a name="rule-based-ui-context-for-extensions"></a>Uzantıları için kural tabanlı UI bağlamı
 Uzantı yazarları, altında çalışacağı bir UI bağlamı etkinleştirildi ve ilişkili VSPackages yüklenen kesin koşulları tanımlamak kural tabanlı UI bağlamı sağlar. Daha fazla bilgi için [nasıl yapılır: Visual Studio uzantıları için kural tabanlı UI bağlamı kullanma](../extensibility/how-to-use-rule-based-ui-context-for-visual-studio-extensions.md).

## <a name="diagnose-extension-performance"></a>Uzantı performansını tanılama
Uzantılar, başlangıç ve çözüm yükleme performansını etkileyebilir. Visual Studio uzantısı etkisi nasıl hesaplandığını ve nasıl yerel olarak bir uzantı uzantısı etkileyen bir performans gösterilebilir, test etmek için analiz edilmeden öğrenin. Daha fazla bilgi için [nasıl yapılır: Uzantı performansını tanılama](how-to-diagnose-extension-performance.md).

## <a name="troubleshoot-vspackages"></a>VSPackage sorunlarını giderme
 Yükleme veya sorun yaşadığınızda VSPackage sorunlarını giderme teknikleri öğrenin: [VSPackage sorunlarını giderme](../extensibility/troubleshooting-vspackages.md)

## <a name="see-also"></a>Ayrıca bkz.
- [VSPackage’lar](../extensibility/internals/vspackages.md)