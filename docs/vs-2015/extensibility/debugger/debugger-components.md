---
title: Hata ayıklayıcı bileşenleri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Visual Studio], components
- components [Visual Studio SDK], debugging
- debugging [Debugging SDK], components
ms.assetid: 8b8ab77f-a134-495c-be42-3bc51aa62dfb
caps.latest.revision: 31
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 12f865e7d4c44cfa4002b330ed85ec95f95a8ef9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68200679"
---
# <a name="debugger-components"></a>Hata Ayıklayıcı Bileşenleri
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

[!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] Hata ayıklayıcı bir VSPackage uygulanır ve tüm hata ayıklama oturumu yönetir. Hata ayıklama oturumu şu öğelerden oluşur:  
  
- **Paket hata ayıklama:** [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] Hata ayıklayıcı ayıklanmakta olan ne olursa olsun aynı kullanıcı arayüzü sağlar.  
  
- **Oturum hata ayıklama Yöneticisi (SDM):** İçin tutarlı bir programlama arabirimi sağlayan [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] hata ayıklayıcı hata ayıklama altyapısı çeşitli yönetimi için. Tarafından uygulanan [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
- **İşlem Hata Ayıklama Yöneticisi (PDM):** Yönetir, tüm çalışan örneklerinde için [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)], olabilir ya da hata ayıklama yapılan tüm programların listesi. Tarafından uygulanan [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
- **Hata ayıklama altyapısı (DE):** Hatası ayıklanmakta olan bir program izlemekten sorumludur SDM ve PDM çalışan programa durumunu satıcılarla iletişim kurmayı ve bir programın bellek durumunun gerçek zamanlı analiz sağlamak için ifade değerlendirici ve sembol sağlayıcısı ile etkileşim kurma ve değişkenler. Tarafından uygulanan [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] (için desteklediği dillerin) ve kendi çalışma zamanı desteklemek istediğiniz üçüncü taraf satıcıların.  
  
- **İfade değerlendirici (EE):** Değişkenleri ve ifadeleri belirli bir noktada bir program durduğunda, kullanıcı tarafından sağlanan dinamik olarak değerlendirmek için destek sağlar. Tarafından uygulanan [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] (için desteklediği dillerin) ve kendi dillerinde desteklemek istediğiniz üçüncü taraf satıcıların.  
  
- **Sembol sağlayıcısı (SP):** Olarak da adlandırılan bir sembol işleyici eşlemeleri bir programın hata ayıklama sembolleri program çalışan bir örneğini böylece anlamlı bilgiler (kaynak kodu düzeyi hata ayıklama ve ifade değerlendirme gibi) sağlanabilir. Tarafından uygulanan [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] (ortak dil çalışma zamanı için [/ CLR] simgeleri ve [PDB] Program veritabanı dosya biçimi simgesi) ve hata ayıklama bilgilerinin depolanması, kendi özel yöntem sahip üçüncü taraf satıcıları tarafından.  
  
  Aşağıdaki diyagramda, Visual Studio hata ayıklayıcı bu öğeleri arasındaki ilişkiyi gösterir.  
  
  ![Hata ayıklama Bileşenleri'ne genel bakış](../../extensibility/debugger/media/dbugcompovrview.gif "DBugCompOvrview")  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Paket Hatalarını Ayıklama](../../extensibility/debugger/debug-package.md)  
 Çalışan hata ayıklama paketi anlatılmaktadır [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] kabuk ve tüm UI işler.  
  
 [İşlem Hata Ayıklama Yöneticisi](../../extensibility/debugger/process-debug-manager.md)  
 Hata ayıklaması yapılabilir işlemlerin yöneticisidir PDM özelliklerinin genel bakış sağlar.  
  
 [Oturum Hata Ayıklama Yöneticisi](../../extensibility/debugger/session-debug-manager.md)  
 IDE hata ayıklama oturumu birleşik bir görünümünü sunan SDM tanımlar. SDM DE yönetir.  
  
 [Hata Ayıklama Altyapısı](../../extensibility/debugger/debug-engine.md)  
 DE sağlayan bir hata ayıklama Hizmetleri belgeleri.  
  
 [Çalışma Modları](../../extensibility/debugger/operational-modes.md)  
 IDE çalışabilir üç moddan genel bir bakış sağlar: Tasarım modunda, çalışma modunda ve kesme modu. Geçiş mekanizmalar da ele alınmıştır.  
  
 [İfade Değerlendirici](../../extensibility/debugger/expression-evaluator.md)  
 Çalışma zamanında EE amacını açıklar.  
  
 [Sembol Sağlayıcısı](../../extensibility/debugger/symbol-provider.md)  
 Değişkenler ve ifadeler uygulama, sembol sağlayıcısı nasıl değerlendirir açıklanır.  
  
 [Tür Görselleştiricisi ve Özel Görüntüleyici](../../extensibility/debugger/type-visualizer-and-custom-viewer.md)  
 Ne anlatılmaktadır bir tür görselleştiricisi ve özel Görüntüleyici ve ifade değerlendiricisi hangi rol hem destekleme.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Hata Ayıklayıcı Kavramları](../../extensibility/debugger/debugger-concepts.md)  
 Hata ayıklama ana mimari kavramlarını açıklar.  
  
 [Hata Ayıklayıcı Bağlamları](../../extensibility/debugger/debugger-contexts.md)  
 Nasıl DE aynı anda kod, belgeler ve ifade değerlendirme bağlamı içinde çalıştığı açıklanmaktadır. , Her üç bağlamları, konumu, konum veya değerlendirme için ilgili açıklar.  
  
 [Hata Ayıklama Görevleri](../../extensibility/debugger/debugging-tasks.md)  
 Program başlatma ve ifadeleri değerlendirme gibi çeşitli hata ayıklama görevlerini bağlantılar içerir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Başlarken](../../extensibility/debugger/getting-started-with-debugger-extensibility.md)
