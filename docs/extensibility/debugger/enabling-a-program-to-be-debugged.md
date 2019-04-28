---
title: Ayıklanacak Program etkinleştirme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], enabling for programs
ms.assetid: 61d24820-0cd9-48b6-8674-6813f7493237
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1f301de66421ef1327b86d900305cb4ecbfb5623
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62889700"
---
# <a name="enable-a-program-to-be-debugged"></a>Bir program görüntüde hata ayıklamayı etkinleştir
Bir program, hata ayıklama altyapısı (DE) hata ayıklama yapılabilmesi, önce DE başlatın ya varolan bir program ekleyin.

## <a name="in-this-section"></a>Bu bölümde
 [Bir bağlantı noktası alma](../../extensibility/debugger/getting-a-port.md) ayıklanacak bir programı etkinleştirmek için ilk adım olarak bir bağlantı noktası alınacağını açıklar.

 [Program kaydetme](../../extensibility/debugger/registering-the-program.md) ayıklanacak program etkinleştirme bir sonraki adım açıklanır: bağlantı noktası ile kaydediliyor. Kaydedildikten sonra program ayıklanabilir ya da ekleme veya just-in-time (JIT) hata ayıklama işlemi.

 [Programa ekleme](../../extensibility/debugger/attaching-to-the-program.md) sonraki adımda açıklanmaktadır: hata ayıklayıcı programa ekleme.

 [Başlatma tabanlı ekleme](../../extensibility/debugger/launch-based-attachment.md) otomatik başlatma SDM ile bağlı olan bir program için başlatma tabanlı ek açıklar.

 [Gerekli olayları gönderme](../../extensibility/debugger/sending-the-required-events.md) hata ayıklama altyapısı (DE) oluştururken gerekli olayları adımları ve programa ekleme.

## <a name="related-sections"></a>İlgili bölümler
 [Bir özel hata ayıklama altyapısı oluşturma](../../extensibility/debugger/creating-a-custom-debug-engine.md) hata ayıklama altyapısı (DE) tanımlar ve DE arabirimler ve bunlar farklı çalışma modları arasında geçiş için hata ayıklayıcının nasıl neden aracılığıyla uygulanan hizmetlerini açıklar.