---
title: 'Test alanı 6: Silme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- source control [Visual Studio SDK], deleting items
- source control plug-ins, deleting items
ms.assetid: 6f2e872c-5ba2-4303-9f50-a90cef9a6225
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 206835d92a2fca27bed2cbb8a96b99e6b7c8a082
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54764060"
---
# <a name="test-area-6-delete"></a>Test alanı 6: Sil
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bu kaynak denetimi eklentisi test alanı silme eylemleri kapsar.  
  
 Kaynak denetimi yanıt eylemleri silmek **Çözüm Gezgini**.  
  
 Silinebilir öğe listesi aşağıda verilmiştir:  
  
- Dosyalar  
  
- Klasörleri  
  
- Proje  
  
  Seçeneğini projenin türüne bağlı olarak olabilir **kaldırmak** (dosyaları diskte kalır) proje veya **Sil** (kaldırır, diskteki dosyaları) projesi. Her iki işlem proje veya öğe kaldırır **Çözüm Gezgini**.  
  
## <a name="expected-behavior"></a>Beklenen davranış  
 Test çalışmalarının silme test alanındaki beklenen davranıştır:  
  
-   Silinmiş Öğe içinde görünür artık **Çözüm Gezgini**.  
  
-   Silinen bir proje veya öğe üst (büyük olasılıkla bir istemiyle.) gerektiği şekilde kullanıma  
  
-   Çıkış kullanıma alınmış silin veya öğe eklendikten sonra bunu görünmez **Bekleyen İadeler** penceresi.  
  
-   Öğe hala silindikten sonra bile kaynak denetim deposunda mevcut ve el ile temizlenmesi gerekir.  
  
|Eylem|Test adımları|Beklenen sonuçları doğrulamak için|  
|------------|----------------|--------------------------------|  
|Bir istemci projesi silme|1.  Bir istemci projesi oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Tüm projeyi çözümden Kaldır|Ortak beklenen bir davranış.|  
|Boş bir dosya Sil|1.  Bir istemci projesi oluşturun.<br />2.  Sıfır bayt boyutunda bir dosya projeye ekleyin.<br />3.  Çözüm kaynak denetimine ekleyin.<br />4.  Dosyayı seçip silin.|Ortak beklenen bir davranış.|  
|Tek bir klasör silme|1.  Çoklu proje çözümü oluşturun.<br />2.  Bir klasör ekleyin.<br />3.  Klasörüne bir dosya ekleyin.<br />4.  Çözüm kaynak denetimine ekleyin.<br />5.  Kaçınmak için projeyi kullanıma ister.<br />6.  Klasörü silin.|Ortak beklenen bir davranış.|  
|Bir dosya sistemi Web projesini silme|1.  Bir dosya sistemi Web projesi (bir UNC yolu belirtmek için Gözat düğmesini kullanın) oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Tüm projeyi çözümden kaldırmak.<br />4.  Yerel bir Web projesi için 1 ile 3 arasındaki adımları yineleyin (kod farklı yollarını sınayan ancak davranışı ve aynı dış arayüze sahiptir).|Ortak beklenen bir davranış.|  
|Bir dosya sistemi Web projeden bir dosyayı silme|1.  Bir dosya sistemi Web projesi oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Bir dosyayı projeden silin.<br />4.  Yerel bir Web projesi için 1 ile 3 arasındaki adımları yineleyin (kod farklı yollarını sınayan ancak davranışı ve aynı dış arayüze sahiptir).|Ortak beklenen bir davranış.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentileri için Test Kılavuzu](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)
