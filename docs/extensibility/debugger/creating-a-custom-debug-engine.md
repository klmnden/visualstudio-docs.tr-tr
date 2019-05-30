---
title: Hata ayıklama motoru özel oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debug engines, implementing
- debug engines, custom
- debugging [Debugging SDK], custom debug engines
ms.assetid: 52794238-6fae-451c-bf1c-99f344c6f173
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3756eb105ec562d902d4631318e7a5fc698601a2
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66345313"
---
# <a name="create-a-custom-debug-engine"></a>Bir özel hata ayıklama altyapısı oluşturma
Hata ayıklama altyapısı (DE), belirli çalışma zamanı mimarileri hata ayıklamasını sağlayan bir bileşendir. Genellikle çalışma zamanı ortam başına yalnızca bir DE uygulama yok.

> [!NOTE]
> Transact-SQL ve JScript için ayrı DE uygulamaları olsa da, tek bir DE VBScript ve JScript paylaşın.

 Yürütme denetimi, kesme noktaları ve ifade değerlendirme gibi hata ayıklama hizmetleri sağlamak için yorumlayıcı veya işlemi sistemi bir DE çalışır. Bu hizmetler DE arabirimleri aracılığıyla uygulanır ve farklı çalışma modları arasında geçiş için hata ayıklayıcı neden olabilir. Daha fazla bilgi için [çalışma modları](../../extensibility/debugger/operational-modes.md).

 Bir DE oluşturma, aşağıdaki adımlardan oluşur:

1. Bir DE Visual Studio ile kaydetme

2. Bir program görüntüde hata ayıklamayı etkinleştir

3. Yürütme denetimi ve durum değerlendirme uygulayın

4. Olayları gönderme

5. Sonlandırma ve ayırma ayarlama

## <a name="in-this-section"></a>Bu bölümde
 [Bir özel hata ayıklama altyapısını kaydetme](../../extensibility/debugger/registering-a-custom-debug-engine.md) kullanılabilmesi için Visual Studio ile hata ayıklama altyapısı kaydetmek için gereken adımları açıklar.

 [Ayıklanacak bir programı etkinleştirmek](../../extensibility/debugger/enabling-a-program-to-be-debugged.md) sizin DE bir program hata ayıklama yapılabilmesi gerekir ilk DE başlatın veya varolan bir program eklemek olduğunu açıklar.

 [Uygulama yürütme denetimi ve durum değerlendirme](../../extensibility/debugger/execution-control-and-state-evaluation.md) Discusses neden bir uygulamada hata ayıklama gerektirir yürütme denetimi özelliklerini uygulama.

 [Olayları gönderme](../../extensibility/debugger/sending-events.md) Describes iletişimine hata ayıklayıcı ve DE bir olay modeli olarak DCOM bağlı.

 [Sonlandırma ve ayırma ayarlama](../../extensibility/debugger/termination-and-detaching.md) hiçbir kesme noktaları, özel durumlar, çalışma zamanı hataları veya uygulamada hata ayıklaması için sonsuz döngüler olduğu anlamına gelir normal sonlandırması elde edileceğini açıklar.

 [Hata ayıklayıcı olayları çağırma](../../extensibility/debugger/calling-debugger-events.md) hata ayıklama oturumunda gerçekleşen olayların arama sırası belgeleri.

 [Nasıl yapılır: Özel hata ayıklama altyapısında hata ayıklama](../../extensibility/debugger/how-to-debug-a-custom-debug-engine.md) özel DE hata ayıklamak açıklanmaktadır.

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio hata ayıklayıcı genişletilebilirliği](../../extensibility/debugger/visual-studio-debugger-extensibility.md)