---
title: Hata ayıklayıcı genişletilebilirliği ile çalışmaya başlama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- getting started, Debugging SDK
- debugging [Debugging SDK], getting started
- Debugging SDK, getting started
ms.assetid: d6ce6f43-1409-4bf7-93cd-f3464ca23504
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6f3fe14cff05f37ef7ee6f10026fd727696a223f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62925725"
---
# <a name="get-started-with-debugger-extensibility"></a>Hata ayıklayıcı genişletilebilirliği ile çalışmaya başlama
[!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] Oluşturmak ve içinden programlarda hata ayıklamak için kullanılan hata ayıklayıcı bileşenleri özelleştirmek için gereken bilgileri sağlar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ortam.

 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklama geliştirmeleri önceki üzerinde gerçekleştirilen test kapsamlı kullanılabilirlik türetilen ekledi [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklayıcıları. Kullanabileceğiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] çok dilli uygulama veya boyunca adım adım hata ayıklama uygulayabilirsiniz uygulamalar ve çok dilli çözümler hata ayıklama sırasında değişkenler üzerinde halindeyken düzenleme.

 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklama yürütülen giden işlem hataları ayıklanan programa ile ve bu nedenle uygulamanın işlem alanına daha az müdahale eden. Sonuç olarak, hata ayıklama programınızı etkilemeden hata ayıklayıcısı ile etkileşim kuran bileşenler yazmak kolaydır.

 En iyi şekilde kullanmanız [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)], aşağıdaki öğeleri içeren bilgi sahibi olmanız gerekir:

- [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Tümleşik geliştirme ortamı (IDE)

- C++ programlama dili

- ATL COM

## <a name="in-this-section"></a>Bu bölümde
 [Hata ayıklayıcıyı genişletmek için yol haritası](../../extensibility/debugger/roadmap-for-extending-the-debugger.md) ürününüzde derleyicinizin ve çıktısını bağlı olarak hata ayıklama uygulama sürecinde özetler.

 [Hata ayıklayıcı bileşenleri](../../extensibility/debugger/debugger-components.md) genel bir bakış sağlar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklama altyapısı (DE) ifade değerlendiricisi (EE) ve sembol işleyici (SH) bileşenleri, hata ayıklama.

 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md) ana hata ayıklama mimari kavramlarını açıklar.

 [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md) hata ayıklama altyapısı (DE) kod, belgeler ve ifade değerlendirme bağlamı içinde aynı anda nasıl çalıştığı açıklanmaktadır. , Her üç bağlamları, konumu, konum veya değerlendirme için ilgili açıklar.

 [Hata ayıklama görevleri](../../extensibility/debugger/debugging-tasks.md) çeşitli program başlatma ve ifadeleri değerlendirme gibi hata ayıklama görevleri bağlantılar içerir.