---
title: 'Test alanı 4: İade | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control [Visual Studio SDK], checking items in
- source control plug-ins, checking items in
ms.assetid: d0329fa8-7a8d-4d30-b67b-6f2a97b75a30
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 80b3603480964daf618040a983b181a9a82f7407
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53853300"
---
# <a name="test-area-4-check-in"></a>Test alanı 4: İade Et
Bu kaynak denetimi eklentisi test alanını kapsayan güncelleştirilmiş öğeleri sürüm deposu gönderme **iade** komutu.  
  
## <a name="command-menu-access"></a>Komut menü erişimi  
 Aşağıdaki [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı menüsü yolları test durumlarında kullanılır.  
  
##### <a name="check-in"></a>Teslim etme:  
 **Dosya**, **kaynak denetimi**, **iade**.  
  
 **Dosya**, **iade**.  
  
 Kısayol menüsünde, **iade**.  
  
## <a name="common-expected-behavior"></a>Ortak beklenen davranışı  
  
-   Projeleri ve dosyaları bir çözüm veya proje kaynak denetimi altında eklenen görünür **iade** iletişim kutusu ve **Bekleyen İadeler** penceresi.  
  
-   Sonra iade eklenen öğeler kaynak denetiminde görünür.  
  
-   İade etme sonra güncelleştirilmiş öğeleri deposunda düzgün bir şekilde tutulur.  
  
## <a name="test-cases"></a>Test çalışmaları  
 Belirli test çalışmaları için iade etme test alanı aşağıda verilmiştir.  
  
### <a name="case-4a-modified-items"></a>Büyük/küçük harf 4a: Değiştirilen öğeler  
 Onay değiştirildi kaynak denetimi altındaki bir dosyayı güncelleştirmek için eylemde kullanmayı açıklar.  
  
|Eylem|Test adımları|Beklenen sonuçları doğrulamak için|  
|------------|----------------|--------------------------------|  
|Kullanıma alınmış bir metin dosyasını değiştirme, dosyayı iade edin (**iade** iletişim kutusu)|1.  Yeni bir proje içeren bir metin dosyası oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Kullanıma alma ve metin dosyasını değiştirin.<br />4.  İade Et iletişim kutusu kontrol edin (**dosya**, **kaynak denetimi**, **iade**).|Ortak beklenen bir davranış.|  
|Kullanıma alınmış bir metin dosyasını değiştirme, dosyayı iade edin (**Bekleyen İadeler** pencere)|1.  Yeni bir proje içeren bir metin dosyası oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Kullanıma alma ve metin dosyasını değiştirin.<br />4.  Aracılığıyla iade **Bekleyen İadeler** penceresi.|Ortak beklenen bir davranış.|  
  
### <a name="case-4b-adding-files"></a>Büyük/küçük harf 4b: Dosya ekleme  
 Bir dosya bir proje ya da bir çözüme bir öğe eklerken, proje veya çözümü de değiştirmeniz gerekir. Bu nedenle üst dosya ayrıca kullanıma ve ayrıca tamamlamak için iade edilmesi gerekir.  
  
|Eylem|Test adımları|Beklenen sonuçları doğrulamak için|  
|------------|----------------|--------------------------------|  
|Bir metin dosyası ekleyin ve her şeyi denetleyin (**iade** iletişim kutusu)|1.  Yeni bir proje oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Bir metin dosyası projeye ekleyin.<br />4.  Projenin kullanıma istenirse kabul edin.<br />5.  Çözümde seçin **Çözüm Gezgini**.<br />6.  İade etme **iade** iletişim kutusu.|Ortak beklenen bir davranış.|  
|Bir metin dosyası ekleyin ve her şeyi denetleyin (**Bekleyen İadeler** pencere)|1.  Yeni bir proje oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Bir metin dosyası projeye ekleyin.<br />4.  Projenin kullanıma istenirse kabul edin.<br />5.  Çözümden iade **Bekleyen İadeler** penceresi.|Ortak beklenen davranışı|  
  
### <a name="case-4c-adding-projects"></a>4c. durum: Ekleme projeleri  
 Bir çözüme bir proje eklediğinizde, çözüm de değiştirmeniz gerekir. Bu nedenle çözüm dosyasını da kullanıma ve ayrıca tamamlamak için iade edilmesi gerekir.  
  
|Eylem|Test adımları|Beklenen sonuçları doğrulamak için|  
|------------|----------------|--------------------------------|  
|Kaynak denetimi altında boş bir çözüme proje ekleme (**iade** iletişim kutusu)|1.  Boş bir çözüm oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Yeni bir proje ekleyin.<br />4.  Çözüm kullanıma istenirse kabul edin.<br />5.  İade etme **iade** iletişim kutusu.|Ortak beklenen bir davranış.|  
|Kaynak denetimi altında boş bir çözüme proje ekleme (**Bekleyen İadeler** pencere)|1.  Boş bir çözüm oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Yeni bir proje ekleyin.<br />4.  Çözüm kullanıma istenirse kabul edin.<br />5.  Çözümden iade **Bekleyen İadeler** penceresi.|Ortak beklenen bir davranış.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentileri için Test Kılavuzu](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)