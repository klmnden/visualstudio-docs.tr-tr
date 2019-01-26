---
title: Hata ayıklama motoru özel oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debug engines, implementing
- debug engines, custom
- debugging [Debugging SDK], custom debug engines
ms.assetid: 52794238-6fae-451c-bf1c-99f344c6f173
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: aff0f3ba1bef25c7754f80dcbb6fb04e2e7da60e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55029914"
---
# <a name="create-a-custom-debug-engine"></a>Bir özel hata ayıklama altyapısı oluşturma
Hata ayıklama altyapısı (DE), belirli çalışma zamanı mimarileri hata ayıklamasını sağlayan bir bileşendir. Genellikle çalışma zamanı ortam başına yalnızca bir DE uygulama yok.  
  
> [!NOTE]
>  Transact-SQL ve JScript için ayrı DE uygulamaları olsa da, tek bir DE VBScript ve JScript paylaşın.  
  
 Yürütme denetimi, kesme noktaları ve ifade değerlendirme gibi hata ayıklama hizmetleri sağlamak için yorumlayıcı veya işlemi sistemi bir DE çalışır. Bu hizmetler DE arabirimleri aracılığıyla uygulanır ve farklı çalışma modları arasında geçiş için hata ayıklayıcı neden olabilir. Daha fazla bilgi için [çalışma modları](../../extensibility/debugger/operational-modes.md).  
  
 Bir DE oluşturma, aşağıdaki adımlardan oluşur:  
  
1.  Bir DE Visual Studio ile kaydetme  
  
2.  Bir program görüntüde hata ayıklamayı etkinleştir  
  
3.  Yürütme denetimi ve durum değerlendirme uygulayın  
  
4.  Olayları gönderme  
  
5.  Sonlandırma ve ayırma ayarlama  
  
## <a name="in-this-section"></a>Bu bölümde  
 [Bir özel hata ayıklama altyapısını kaydetme](../../extensibility/debugger/registering-a-custom-debug-engine.md)  
 Böylece kullanılabilmesi için Visual Studio ile hata ayıklama altyapısı kaydetmek için gereken adımları açıklar.  
  
 [Bir program görüntüde hata ayıklamayı etkinleştir](../../extensibility/debugger/enabling-a-program-to-be-debugged.md)  
 Sizin DE bir program hata ayıklama yapılabilmesi gerekir ilk DE başlatın veya varolan bir program ekleyin, açıklar.  
  
 [Yürütme denetimi ve durum değerlendirme uygulayın](../../extensibility/debugger/execution-control-and-state-evaluation.md)  
 Neden bir uygulamada hata ayıklama yürütme denetimi özelliklerini uygulama gerektirir açıklanır.  
  
 [Olayları gönderme](../../extensibility/debugger/sending-events.md)  
 Hata ayıklayıcı ve DE arasındaki iletişim, DCOM göre bir olay modeli olarak açıklar.  
  
 [Sonlandırma ve ayırma ayarlama](../../extensibility/debugger/termination-and-detaching.md)  
 Hiçbir kesme noktaları, özel durumlar, çalışma zamanı hataları veya uygulamada hata ayıklaması için sonsuz döngüler olduğu anlamına gelir normal sonlandırması elde etmek açıklanmaktadır.  
  
 [Hata ayıklayıcı olayları çağırma](../../extensibility/debugger/calling-debugger-events.md)  
 Hata ayıklama oturumunda gerçekleşen olayların arama sırası belgeler.  
  
 [Nasıl yapılır: Özel hata ayıklama altyapısında hata ayıklama](../../extensibility/debugger/how-to-debug-a-custom-debug-engine.md)  
 Özel bir DE hata ayıklama açıklanmaktadır.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio hata ayıklayıcı genişletilebilirliği](../../extensibility/debugger/visual-studio-debugger-extensibility.md)