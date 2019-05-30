---
title: Hata ayıklayıcı bileşenleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Visual Studio], components
- components [Visual Studio SDK], debugging
- debugging [Debugging SDK], components
ms.assetid: 8b8ab77f-a134-495c-be42-3bc51aa62dfb
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 28afdd7f12e7d83b042f5c705c85fa567fdbb979
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66345885"
---
# <a name="debugger-components"></a>Hata ayıklayıcı bileşenleri
[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Hata ayıklayıcı bir VSPackage uygulanır ve tüm hata ayıklama oturumu yönetir. Hata ayıklama oturumu şu öğelerden oluşur:

- **Paket hata ayıklama:** [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Hata ayıklayıcı ayıklanmakta olan ne olursa olsun aynı kullanıcı arayüzü sağlar.

- **Oturum hata ayıklama Yöneticisi (SDM):** İçin tutarlı bir programlama arabirimi sağlayan [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklayıcı hata ayıklama altyapısı çeşitli yönetimi için. Tarafından uygulanan [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

- **İşlem Hata Ayıklama Yöneticisi (PDM):** Yönetir, tüm çalışan örneklerinde için [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], olabilir ya da hata ayıklama yapılan tüm programların listesi. Tarafından uygulanan [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

- **Hata ayıklama altyapısı (DE):** Hatası ayıklanmakta olan bir program izlemekten sorumludur SDM ve PDM çalışan programa durumunu satıcılarla iletişim kurmayı ve bir programın bellek durumunun gerçek zamanlı analiz sağlamak için ifade değerlendirici ve sembol sağlayıcısı ile etkileşim kurma ve değişkenler. Tarafından uygulanan [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] (için desteklediği dillerin) ve kendi çalışma zamanı desteklemek istediğiniz üçüncü taraf satıcıların.

- **İfade değerlendirici (EE):** Değişkenleri ve ifadeleri belirli bir noktada bir program durduğunda, kullanıcı tarafından sağlanan dinamik olarak değerlendirmek için destek sağlar. Tarafından uygulanan [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] (için desteklediği dillerin) ve kendi dillerinde desteklemek istediğiniz üçüncü taraf satıcıların.

- **Sembol sağlayıcısı (SP):** Olarak da adlandırılan bir sembol işleyici eşlemeleri bir programın hata ayıklama sembolleri program çalışan bir örneğini böylece anlamlı bilgiler (kaynak kodu düzeyi hata ayıklama ve ifade değerlendirme gibi) sağlanabilir. Tarafından uygulanan [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] (ortak dil çalışma zamanı için [/ CLR] simgeleri ve [PDB] Program veritabanı dosya biçimi simgesi) ve hata ayıklama bilgilerinin depolanması, kendi özel yöntem sahip üçüncü taraf satıcıları tarafından.

  Aşağıdaki diyagramda, Visual Studio hata ayıklayıcı bu öğeleri arasındaki ilişkiyi gösterir.

  ![Hata ayıklama Bileşenleri'ne genel bakış](../../extensibility/debugger/media/dbugcompovrview.gif "DBugCompOvrview")

## <a name="in-this-section"></a>Bu bölümde
 [Paket hatalarını ayıklama](../../extensibility/debugger/debug-package.md) çalışan hata ayıklama paketi anlatılmaktadır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] kabuk ve tüm UI işler.

 [İşlem Hata Ayıklama Yöneticisi](../../extensibility/debugger/process-debug-manager.md) yöneticisidir ayıklanabilir işlemlerin PDM özelliklerinin genel bir bakış sağlar.

 [Oturum hata ayıklama Yöneticisi](../../extensibility/debugger/session-debug-manager.md) IDE hata ayıklama oturumu birleşik bir görünümünü sunan SDM tanımlar. SDM DE yönetir.

 [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md) belgeleri hata ayıklama Hizmetleri DE sağlar.

 [Çalışma modları](../../extensibility/debugger/operational-modes.md) IDE çalışabilir üç moddan genel bir bakış sağlar: Tasarım modunda, çalışma modunda ve kesme modu. Geçiş mekanizmalar da ele alınmıştır.

 [İfade değerlendirici](../../extensibility/debugger/expression-evaluator.md) çalışma zamanında EE amacını açıklar.

 [Sembol sağlayıcısı](../../extensibility/debugger/symbol-provider.md) değişkenler ile ifadeler uygulama, sembol sağlayıcısı nasıl değerlendirir açıklanır.

 [Tür görselleştiricisi ve özel Görüntüleyici](../../extensibility/debugger/type-visualizer-and-custom-viewer.md) Discusses bir tür görselleştiricisi ve özel Görüntüleyici ve ifade değerlendiricisi hangi rol hem destekleme.

## <a name="related-sections"></a>İlgili bölümler
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md) ana hata ayıklama mimari kavramlarını açıklar.

 [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md) DE kod, belgeler ve ifade değerlendirme bağlamı içinde aynı anda nasıl çalıştığı açıklanmaktadır. , Her üç bağlamları, konumu, konum veya değerlendirme için ilgili açıklar.

 [Hata ayıklama görevleri](../../extensibility/debugger/debugging-tasks.md) çeşitli program başlatma ve ifadeleri değerlendirme gibi hata ayıklama görevleri bağlantılar içerir.

## <a name="see-also"></a>Ayrıca bkz.
- [Kullanmaya başlama](../../extensibility/debugger/getting-started-with-debugger-extensibility.md)