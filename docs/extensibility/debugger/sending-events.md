---
title: Olayları gönderme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], sending events
ms.assetid: 064231e7-59b5-4437-8240-a23c0a7ec2a9
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 8f4ee7ab58f95ede913536102573a8c6061f860a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53959991"
---
# <a name="send-events"></a>Olayları gönderme
Hata ayıklayıcı ile hata ayıklama altyapısı (DE) arasındaki iletişim için DCOM bir olay modeline mekanizmadır. Olayları COM nesneleri olarak gönderilir ve her bir olay belirtin parametreleri vardır:  
  
- Olay adında DE.  
  
- Ne açıklaması.  
  
- İşlem, program ve iş parçacığı bilgisi, olayın gerçekleştiği bağlamı tanımlar. İşlem, bir DE gönderilen olaylar için gönderilmez.  
  
- Zaman uyumlu veya zaman uyumsuz olay olup olmadığını belirten bir olay türü.  
  
  Tüm hata ayıklama olaylarını yöntemi kullanılarak gönderilen [IDebugEventCallback2::Event](../../extensibility/debugger/reference/idebugeventcallback2-event.md).  
  
## <a name="in-this-section"></a>Bu bölümde  
 [Olay kaynakları](../../extensibility/debugger/event-sources-visual-studio-sdk.md)  
 İki olay kaynağını açıklar: hata ayıklama altyapısı (DE) ve oturum Yöneticisi (SDM) hata ayıklama.  
  
 [Desteklenen olay türleri](../../extensibility/debugger/supported-event-types.md)  
 Şu anda desteklenen olay türleri ele alınmaktadır: zaman uyumsuz ve zaman uyumlu.  
  
 [Olay açıklamaları](../../extensibility/debugger/event-descriptions.md)  
 Olayları ve bunların kullanılması nedeniyle tanımlar.  
  
## <a name="related-sections"></a>İlgili bölümler  
 [Bir özel hata ayıklama altyapısı oluşturma](../../extensibility/debugger/creating-a-custom-debug-engine.md)  
 Bir DE hata ayıklama hizmetleri sağlamak için yorumlayıcı veya işletim sistemi ile nasıl çalıştığı açıklanır.