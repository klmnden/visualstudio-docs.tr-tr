---
title: 'Test alanı 8: Eklenti değiştirme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control [Visual Studio SDK], switching plug-ins
- source control plug-ins, switching
ms.assetid: 01370792-b5da-4e46-9ce2-7dd326587141
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 460d3afc18c19b7e7e3ed97725d69b5a8b04a382
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54998670"
---
# <a name="test-area-8-plug-in-switching"></a>Test alanı 8: Eklenti değiştirme
[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Tümleşik geliştirme ortamı (IDE), geçerli kaynak denetimi eklentisi değiştirmek için kullanıcı arabirimi (UI) sahiptir. Bu test alanı kullanmak için çözüm kaynak denetimi eklentisi, çekme işlemini test çalışmalarını sağlar.  

## <a name="command-menu-access"></a>Komut menü erişimi  
 Aşağıdaki [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı menüsü yolları test durumlarında kullanılır.  

-   Geçerli kaynak denetimi Eklentisi: **Araçlar** -> **seçenekleri** -> **kaynak denetimi** -> **Eklenti Seçimi**.  

-   Değişiklik kaynak denetim bağlantısı: **Dosya** -> **kaynak denetimi** -> **değiştirmek kaynak denetimi**...  

## <a name="common-expected-behavior"></a>Ortak beklenen davranışı  
 Visual Studio çıkmadan veya çözümü yeniden kaynak denetimi için bir çözüm eklentisi değiştirmek mümkündür. Ayrıca, geçerli kaynak denetimi eklentisi Bu çözüm yüklendiğinde bir çözüm tarafından kullanılan bir otomatik olarak değiştirir.  

## <a name="test-cases"></a>Test çalışmaları  
 Belirli test çalışmaları için eklenti geçiş test alanı aşağıda verilmiştir.  

### <a name="case-8a-automatic-change"></a>Büyük/küçük harf 8a: Otomatik değiştirme  

#### <a name="expected-behavior"></a>Beklenen davranış  
 Bir kullanıcı, kaynak denetimi altında bir çözüm yüklediğinde, çözüm otomatik olarak yüklenir ve ilgili kaynak denetimi eklentisi geçerli olarak seçilir.  


| Eylem | Test adımları | Beklenen sonuçları doğrulamak için |
| - | - | - |
| Otomatik kaynak denetimi eklentisini Değiştir | 1.  Geçerli olarak test altındaki eklenti seçin (**Araçları** -> **seçenekleri** -> **kaynak denetimi** -> **eklentisi Seçimi**.)<br />2.  Yeni bir proje oluşturun.<br />3.  Çözüm kaynak denetimine ekleyin.<br />4.  Başka bir eklentiyi seçin (örneğin, [!INCLUDE[vsvss](../../extensibility/includes/vsvss_md.md)]).<br />5.  Kaldırılırken çözüm istemi kabul edin.<br />6.  Diskten çözümü yeniden açın. | Çözüm açılır.<br /><br /> Geçerli kaynak denetimi eklentisi altında test eklentisidir. |

### <a name="case-8b-solution-based-change"></a>Büyük/küçük harf 8b: Çözüm tabanlı Değiştir  

#### <a name="expected-behavior"></a>Beklenen davranış  
 Çözüm değiştirilmesi, ilişkili kaynak denetimi eklentisi olabilir.  


| Eylem | Test adımları | Beklenen sonuçları doğrulamak için |
|----------------------------------| - | - |
| Değişikliği bir çözüm eklentisi | 1.  Geçerli olarak test altındaki eklenti seçin (**Araçları** -> **seçenekleri** -> **kaynak denetimi** -> **eklentisi Seçimi**).<br />2.  Yeni proje ve çözüm oluşturun.<br />3.  Çözüm kaynak denetimine ekleyin.<br />4.  Çözümün kaynak denetimi bağlantısını (kullanarak **kaynak denetimini Değiştir** iletişim kutusunda).<br />5.  Başka bir eklentiyi seçin (örneğin, [!INCLUDE[vsvss](../../extensibility/includes/vsvss_md.md)]).<br />6.  Çözümü diskten kaldırıldığında, yeniden yükleyin.<br />7.  Çözüm kaynak denetimine ekleyin.<br />8.  Çözümün kaynak denetimi bağlantısını (kullanarak **kaynak denetimini Değiştir** iletişim kutusunda).<br />9. Yeniden test eklenti'ı seçin.<br />10. Çözümü diskten, kaldırıldığında, yeniden yükleyin.<br />11. Çözüm özgün konuma bağlamak (kullanarak **kaynak denetimini Değiştir** iletişim kutusunda). | Seçili kullanarak çözüm kaynak denetimine eklendiğinde eklenti. |

## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentileri için Test Kılavuzu](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)