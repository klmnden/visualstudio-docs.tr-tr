---
title: Test kaynak denetimi eklentileri için Kılavuzu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- plug-ins, source control
- source control [Visual Studio SDK], testing plug-ins
- tests, source control plug-ins
- testing, source control plug-ins
- source control plug-ins, test guide
ms.assetid: 13b74765-0b7c-418e-8cd9-5f2e8db51ae5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c7a1313a5d74f973e439d6177234eb11a202b344
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54949694"
---
# <a name="test-guide-for-source-control-plug-ins"></a>Kaynak Denetimi Eklentileri için Test Kılavuzu
Bu bölümde, kaynak denetimi eklentisi ile test etmek için yönergeler sağlanmaktadır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Test en yaygın alanlara ek olarak bazı sorunlu olabilecek daha karmaşık alanları kapsamlı bir bakış sağlanır. Bu genel bakış, test çalışmalarının kapsamlı bir liste olarak tasarlanmamıştır.  
  
> [!NOTE]
>  Bazı hata düzeltmeleri ve geliştirmeleri en son [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE, var olan kaynak denetimi daha önce önceki sürümlerini kullanırken karşılaşılan değil eklentileri ile ilgili sorunlar ortaya [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Hiçbir eklenti için önceki sürümden itibaren yapılan değişiklikler olsa bile, var olan kaynak denetimi eklentisi Bu bölümde, numaralandırılan alanlarda test önemle tavsiye edilir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].  
  
## <a name="common-preparation"></a>Ortak hazırlama  
 Bir makine [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ve yüklü, hedef kaynak denetimi eklentisi gereklidir. Benzer şekilde yapılandırılmış bir ikinci makine, açık kaynak denetimi testlerden bazıları için kullanılabilir.  
  
## <a name="definition-of-terms"></a>Koşulları tanımı  
 Bu test Kılavuzu amacıyla aşağıdaki terim tanımları kullanın:  
  
 İstemci projesi  
 Herhangi bir proje türü kullanılabilir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] kaynak denetimi tümleştirmesini destekleyen (örneğin, [!INCLUDE[vbprvb](../../code-quality/includes/vbprvb_md.md)], [!INCLUDE[csprcs](../../data-tools/includes/csprcs_md.md)], veya [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)]).  
  
 Web projesi  
 Web projeleri dört tür vardır: Dosya sistemi, yerel IIS, uzak sitelerin ve FTP.  
  
- Dosya sistemi projeleri bir yerel yolda oluşturulur, ancak dahili olarak bir UNC yolu erişilen ve istemci projeleri gibi IDE içinde kaynak denetimi altında yerleştirilmiş olarak yüklenmesi için Internet Information Services (IIS) gerektirmez.  
  
- Yerel IIS projeleri aynı makineye yüklenir ve erişilen IIS yerel makineye işaret eden bir URL ile çalışın.  
  
- Uzak siteleri projeleri aynı zamanda bir IIS hizmetleri altında oluşturulan, ancak IIS sunucu makinesinde ve değil, kaynak denetimi altında yerleştirilmiş içinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE.  
  
- FTP projeleri uzak bir FTP sunucusu üzerinden erişilen ancak kaynak denetimi altında yerleştirilemez.  
  
  Liste  
  Çözüm veya projeyi kaynak denetimi altında için başka bir terim.  
  
  Sürüm Store  
  Kaynak Denetimi Eklentisi API aracılığıyla erişilen kaynak denetimi veritabanı.  
  
## <a name="test-areas-covered-in-this-section"></a>Bu bölümde yer alan test alanlarını  
  
-   [Test alanı 1: / Açık kaynak denetiminden Ekle](../../extensibility/internals/test-area-1-add-to-open-from-source-control.md)  
  
    -   Büyük/küçük harf 1a: Kaynak Denetimine Çözüm Ekle  
  
    -   Büyük/küçük harf 1b: Açık çözüm kaynak denetimi  
  
    -   Durum 1c: Kaynak denetiminden çözüm ekleyin  
  
-   [Test alanı 2: Kaynak denetiminden alma](../../extensibility/internals/test-area-2-get-from-source-control.md)  
  
-   [Test alanı 3: Kullanıma almayı geri al / gözden geçirin](../../extensibility/internals/test-area-3-check-out-undo-checkout.md)  
  
    -   3. durum: Kullanıma almayı geri al / gözden geçirin  
  
    -   Büyük/küçük harf 3a: Kullanıma Al  
  
    -   Büyük/küçük harf 3b: Bağlantısı kesilen kullanıma alma  
  
    -   Durum 3c: Sorgu düzenleme/sorgu kaydetme (QEQS)  
  
    -   Case 3d: Sessiz kullanıma alma  
  
    -   Büyük/küçük harf 3e: Kullanıma almayı geri al  
  
-   [Test alanı 4: Teslim etme](../../extensibility/internals/test-area-4-check-in.md)  
  
    -   Büyük/küçük harf 4a: Değiştirilen öğeler  
  
    -   Büyük/küçük harf 4b: Dosya ekleme  
  
    -   4c. durum: Ekleme projeleri  
  
-   [Test alanı 5: Kaynak denetimini Değiştir](../../extensibility/internals/test-area-5-change-source-control.md)  
  
    -   Büyük/küçük harf 5a: bağlama  
  
    -   Büyük/küçük harf 5b: Bağlamayı Kaldır  
  
    -   Durum 5c: yeniden bağlayın  
  
-   [Test alanı 6: DELETE](../../extensibility/internals/test-area-6-delete.md)  
  
-   [Test alanı 7: Paylaş](../../extensibility/internals/test-area-7-share.md)  
  
-   [Test alanı 8: Eklenti değiştirme](../../extensibility/internals/test-area-8-plug-in-switching.md)  
  
    -   Büyük/küçük harf 8a: Otomatik değiştirme  
  
    -   Büyük/küçük harf 8b: Çözüm tabanlı Değiştir  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentileri](../../extensibility/source-control-plug-ins.md)