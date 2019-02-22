---
title: 'Nasıl yapılır: Performans veri dosyası adlandırma seçeneklerini ayarlama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: d7a8d6b9-ab23-46fb-98ed-774781157860
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2b83b0aa083ca115797c9dc1cd8345d397307177
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56626966"
---
# <a name="how-to-set-performance-data-file-name-options"></a>Nasıl yapılır: Performans veri dosyası adlandırma seçeneklerini ayarlama

Varsayılan olarak, profil oluşturma verilerini kaydedin (. *Vsp*) aşağıdaki söz dizimini kullanarak dosya:

*Path\VSP-File\YYMMDD(N)* **.vsp**

Herhangi bir adlandırma parametre değiştirebileceğiniz **genel** için performans oturumu Özellikleri iletişim kutusu sayfası.

|||
|-|-|
|*Yolu*|Rapor içeren dizin. Varsayılan konumu, kullanıcının projeler ve çözümler için varsayılan konum ya da Çözüm klasörü ' dir.|
|*VSP-File*|Profil oluşturma veri dosyasının adı. Yürütülebilir, profil oluşturulan ya da çözüm adı varsayılan addır.|
|*YYAAGG*|Yıl, ay ve profil oluşturma verilerinin toplandığı günü gösteren tarih damgası.|
|*(N)*|Birden fazla profil oluşturma veri dosyası varsa, dosya adı parantezler arasında artan bir sayı eklenir.|

## <a name="to-change-the-naming-syntax-of-the-profiling-data-files-of-a-performance-session"></a>Adlandırma söz dizimi profil oluşturma veri dosyaları bir performans oturumunun değiştirmek için

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