---
title: Yardım İçerik Yöneticisi geçersiz kılmaları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-help-viewer
ms.topic: conceptual
ms.assetid: 95fe6396-276b-4ee5-b03d-faacec42765f
caps.latest.revision: 11
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 9dfd7f7d75a44cb28e2829e38c27b63a329eacaa
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62584559"
---
# <a name="help-content-manager-overrides"></a>Yardım İçerik Yöneticisi Geçersiz Kılmaları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yardım Görüntüleyici ve Visual Studio IDE Yardım ilgili özellikleri varsayılan davranışını değiştirmek için kayıt defterini değiştirebilirsiniz.  
  
|Görev|Kayıt Defteri Anahtarı|Değer ve tanımı|  
|----------|------------------|--------------------------|  
|Benzersiz bir hizmet uç noktası tanımlama|HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VSWinExpress\14.0\Help|NewContentAndUpdateService--*HTTPValueForTheServiceEndpoint*.|  
|Çevrimiçi/çevrimdışı varsayılan tanımlayın|HKEY_LOCAL_MACHINE\Software\Microsoft\VSWinExpress\14.0\help|UseOnlineHelp--girin `0` yerel Yardım belirtin ve girin `1` çevrimiçi Yardım belirtmek için.|  
|Benzersiz F1 uç noktası tanımlama|HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VSWinExpress\14.0\Help|OnlineBaseUrl--*HTTPValueForTheServiceEndpoint*|  
|BITS iş önceliği geçersiz kıl|(Bulunan bir 64-bit machine)\Microsoft\Help\v2.2 HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node|BITSPriority--aşağıdaki değerlerden birini kullanın: **ön plan**, **yüksek**, **normal**, veya **düşük**.|  
|Devre dışı bırakma, çevrimiçi (ve IDE çevrimiçi seçeneği)|(Bulunan bir 64-bit machine)\Microsoft\VisualStudio\14.0\Help HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node|OnlineHelpPreferenceDisabled--çevrimiçi Yardım içeriğine erişimini devre dışı bırakmak için 1 olarak ayarlayın.|  
|Devre dışı bırakma içeriği yönetme|(Bulunan bir 64-bit machine)\Microsoft\VisualStudio\14.0\Help HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node|ContentManagementDisabled--devre dışı bırakmak için 1 olarak ayarlayın **içeriği Yönet** Yardım Görüntüleyicisi sekmesinde.|  
|Yerel içerik deposuna ağ paylaşımına işaret|HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Help\v2.2\Catalogs\VisualStudio11|LocationPath=”*ContentStoreNetworkShare*”|  
|Visual Studio özelliği ilk kez başlatıldığında içerik yüklenmesini devre dışı bırakın.|(Bulunan bir 64-bit machine)\Microsoft\VisualStudio\14.0\Help HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node|DisableFirstRunHelpSelection--Visual Studio başlayan ilk kez yapılandırılan Yardım özellikleri devre dışı bırakmak için 1 olarak ayarlayın.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yardım Görüntüleyicisi Yönetici Kılavuzu](../ide/help-viewer-administrator-guide.md)
