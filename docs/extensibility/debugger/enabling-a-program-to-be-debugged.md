---
title: Ayıklanacak Program etkinleştirme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], enabling for programs
ms.assetid: 61d24820-0cd9-48b6-8674-6813f7493237
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 94034f54457a66b0dccd4ccf2d533915a8d818dc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53888484"
---
# <a name="enable-a-program-to-be-debugged"></a>Bir program görüntüde hata ayıklamayı etkinleştir
Bir program, hata ayıklama altyapısı (DE) hata ayıklama yapılabilmesi, önce DE başlatın ya varolan bir program ekleyin.  
  
## <a name="in-this-section"></a>Bu bölümde  
 [Bir bağlantı noktası alma](../../extensibility/debugger/getting-a-port.md)  
 Bir program görüntüde hata ayıklamayı etkinleştirmek için ilk adım olarak bir bağlantı noktası alınacağını açıklar.  
  
 [Kayıt programı](../../extensibility/debugger/registering-the-program.md)  
 Sonraki adım bir program görüntüde hata ayıklamayı etkinleştirme açıklanmaktadır: bağlantı noktası ile kaydediliyor. Kaydedildikten sonra program ayıklanabilir ya da ekleme veya just-in-time (JIT) hata ayıklama işlemi.  
  
 [Programa ekleme](../../extensibility/debugger/attaching-to-the-program.md)  
 Sonraki adımda açıklanmaktadır: hata ayıklayıcı programa ekleme.  
  
 [Başlatma tabanlı ekleme](../../extensibility/debugger/launch-based-attachment.md)  
 Otomatik başlatma SDM ile bağlı olan bir program için başlatma tabanlı ek açıklar.  
  
 [Gerekli olayları gönderme](../../extensibility/debugger/sending-the-required-events.md)  
 Hata ayıklama altyapısı (DE) oluştururken gerekli olayları adımları ve programa ekleme.  
  
## <a name="related-sections"></a>İlgili bölümler  
 [Bir özel hata ayıklama altyapısı oluşturma](../../extensibility/debugger/creating-a-custom-debug-engine.md)  
 Hata ayıklama altyapısı (DE) tanımlar ve DE arabirimler ve bunlar farklı çalışma modları arasında geçiş için hata ayıklayıcının nasıl neden aracılığıyla uygulanan hizmetlerini açıklar.