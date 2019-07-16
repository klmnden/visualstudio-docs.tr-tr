---
title: 'Nasıl yapılır: Performans veri dosyası adlandırma seçeneklerini ayarlama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: d7a8d6b9-ab23-46fb-98ed-774781157860
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: faaa78d34c71d1f0b436b861ccb1ac4892267e9b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68205793"
---
# <a name="how-to-set-performance-data-file-name-options"></a>Nasıl yapılır: Performans Veri Dosyası Adlandırma Seçeneklerini Ayarlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Varsayılan olarak, aşağıdaki söz dizimini kullanarak bir profil oluşturma veri (.vsp) dosyasını kaydedin:  
  
 *Path\VSP-File\YYMMDD(N)* **.vsp**  
  
 Performans oturumu için herhangi bir adlandırma parametre Özellikleri iletişim kutusu, genel sayfasında değiştirebilirsiniz.  
  
 **Gereksinimler**  
  
- [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
|||  
|-|-|  
|*Yolu*|Rapor içeren dizin. Varsayılan konumu, kullanıcının projeler ve çözümler için varsayılan konum ya da Çözüm klasörü ' dir.|  
|*VSP-File*|Profil oluşturma veri dosyasının adı. Yürütülebilir, profil oluşturulan ya da çözüm adı varsayılan addır.|  
|*YYAAGG*|Yıl, ay ve profil oluşturma verilerinin toplandığı günü gösteren tarih damgası.|  
|*(N)*|Birden fazla profil oluşturma veri dosyası varsa, dosya adı parantezler arasında artan bir sayı eklenir.|  
  
### <a name="to-change-the-naming-syntax-of-the-profiling-data-files-of-a-performance-session"></a>Adlandırma söz dizimi profil oluşturma veri dosyaları bir performans oturumunun değiştirmek için  
  
1. İçinde **performans Gezgini**performans oturumu adına sağ tıklayın ve ardından **özellikleri**.  
  
2. Tıklayın **genel**.  
  
3. Altında **rapor**, aşağıdaki ayarlardan birini değiştirin:  
  
    |||  
    |-|-|  
    |**Rapor konumu**|Profil oluşturma veri dosyaları depolamak için bir dizin belirtin.|  
    |**Rapor adı**|Dosyalar için temel bir ad belirtin.|  
    |**Yeni raporlar oturuma otomatik olarak Ekle**|Veri dosyası için performans oturumu otomatik olarak eklemek için onay kutusunu işaretleyin.|  
    |**Oluşturulan raporlar için artan bir sayı Ekle**|Aynı ada sahip birden fazla dosya varsa, artan bir sayı için dosya adı eklemek için onay kutusunu işaretleyin. Varolan dosyanın üzerine yazmak için bu onay kutusunu temizleyin.|  
    |**Numara için zaman damgasını kullanın**|Dosya adına bir tarih damgası eklemek için onay kutusunu işaretleyin.|
