---
title: FxCopCmd hataları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: devlang-csharp
ms.topic: conceptual
helpviewer_keywords:
- FxCopCmd errors
ms.assetid: bb614ed0-1b7c-4b56-99ae-da50ef6cfef9
caps.latest.revision: 12
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: b5c7b62ce9e117b348daaa54da3d397346b6eab0
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54767538"
---
# <a name="fxcopcmd-errors"></a>FxCopCmd Hataları
FxCopCmd önemli olması için tüm hataları dikkate almaz. FxCopCmd kısmi analiz gerçekleştirmek için yeterli bilgi varsa, oluşan analiz ve raporları hatalar gerçekleştirir. Bir 32 bitlik tamsayıdır, hata kodu karşılaştırmaya hataları karşılık gelen sayısal değerleri içerir.  
  
 Aşağıdaki tabloda FxCopCmd tarafından döndürülen hata kodları açıklanmaktadır:  
  
|Hata|Sayısal değer|  
|-----------|-------------------|  
|Hata yok|0x0|  
|Analiz hatası|0x1|  
|Kuralın özel durumları|0x2|  
|Proje yükleme hatası|0x4|  
|Derleme yükleme hatası|0x8|  
|Kural kitaplık yükleme hatası|0x10|  
|İçeri aktarma rapor yükleme hatası|0x20|  
|Çıkış hatası|0x40|  
|Komut satırı geçiş hatası|0x80|  
|Başlatma hatası|0x100|  
|Derleme başvuruları hatası|0x200|  
|BuildBreakingMessage|0x400|  
|Bilinmeyen hata|0x1000000|  
  
 Çözümleme hatası için önemli hatalar döndürülür. Analiz tamamlanamadı gösterir. Uygun olduğunda hata kodu önemli hata temel nedenini de içerir. Aşağıdaki koşullar önemli hatalar oluşturur:  
  
-   Analiz tarafından yetersiz girişi nedeniyle gerçekleştirilemedi.  
  
-   Analiz FxCopCmd tarafından işlenmemiş özel durum oluşturdu.  
  
-   Belirtilen proje dosyası bulunamadı veya bozuk olabilir.  
  
-   Output seçeneği belirtilmedi veya dosya yazılmadı.  
  
    > [!NOTE]
    >  FxCopCmd dönüş kodu "Derleme hatası başvuruları" 0x200 tek başına bir hata yerine bir uyarı olduğunu. Bu dönüş kodu eksik dolaylı başvuru bulundu, ancak FxCopCmd bunları işleyebilmesi olduğunu gösterir. Bu, bazı analiz sonuçları gizliliği bozulmuş olabilecek, olasılığı olan bir uyarıdır. Diğer dönüş kodu ile birleştirildiğinde, "Derleme hatası başvuruları" dönüş kodu hata olarak göz önünde bulundurun.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kod Çözümleme Uygulama Hataları](../code-quality/code-analysis-application-errors.md)