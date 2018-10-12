---
title: VSPackage'ları yönetme | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- VSPackages, autoloading
- VSPackages, delayed loading
- delay loading
- VSPackages, loading
ms.assetid: 386e0ce5-4107-4164-b0cd-1cf43eb5e7cf
caps.latest.revision: 36
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5b68ad8fb8ce32c2a4a1210d38fb458518d28435
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49296354"
---
# <a name="managing-vspackages"></a>VSPackage’ları Yönetme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Çoğu durumda VSPackages, proje ve öğe şablonlarını kaydetme ve paket otomatik olarak yük yönetilmesi konusunda endişelenmesine gerek yoktur. Ancak, bazı durumlarda, paket yönetmek için biraz daha fazla bilgi edinmek gerekebilir.  
  
## <a name="using-the-experimental-instance"></a>Deneysel örneği kullanma  
 Deneysel örnek hakkında daha fazla bilgi için bkz. [deneysel örneğinde](../extensibility/the-experimental-instance.md).  
  
## <a name="registering-and-unregistering-vspackages"></a>VSPackage Kaydetme ve Kaydını Kaldırma  
 Kaydolun ve VSPackages ve diğer tür uzantılarla kaydı konusunda bilgi edinmek için bkz: [kaydetme ve kaydını kaldırma VSPackages](../extensibility/registering-and-unregistering-vspackages.md).  
  
## <a name="loading-a-vspackage"></a>VSPackage yükleme  
 VSPackage sorsorgu CMDUICONTEXT GUID açık belirli bir zaman için ayarlanabilir. Daha fazla bilgi için [VSPackage yükleme](../extensibility/loading-vspackages.md).  
  
## <a name="using-asyncpackage-to-load-vspackages-in-the-background"></a>AsyncPackage kullanarak arka planda VSPackage'ı yükleme  
 Visual Studio kullanıcı Arabirimi yanıt sürelerinde için arka plan iş parçacığında yükleme paketi AsyncPackage sınıfı sağlar. Daha fazla bilgi için [nasıl yapılır: arka planda VSPackage yükleme için kullanım AsyncPackage](../extensibility/how-to-use-asyncpackage-to-load-vspackages-in-the-background.md).  
  
## <a name="rule-based-ui-context-for-extensions"></a>Uzantıları için kural tabanlı UI bağlamı  
 Uzantı yazarları, altında çalışacağı bir UI bağlamı etkinleştirildi ve ilişkili VSPackages yüklenen kesin koşulları tanımlamak kural tabanlı UI bağlamı sağlar. Daha fazla bilgi için [nasıl yapılır: Visual Studio uzantıları kullanım kural tabanlı UI bağlamı](../extensibility/how-to-use-rule-based-ui-context-for-visual-studio-extensions.md).  
  
## <a name="troubleshooting-vspackages"></a>VSPackage Sorunlarını Giderme  
 Yükleme veya sorun yaşadığınızda VSPackage sorunlarını giderme teknikleri öğrenin: [VSPackage sorunlarını giderme](../extensibility/troubleshooting-vspackages.md)  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPackage’lar](../extensibility/internals/vspackages.md)

