---
title: Olayları gönderme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], sending events
ms.assetid: 064231e7-59b5-4437-8240-a23c0a7ec2a9
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 98247b894d2db628d508713875ba0ea7d0642729
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68204736"
---
# <a name="sending-events"></a>Olayları Gönderme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklayıcı ile hata ayıklama altyapısı (DE) arasındaki iletişim için DCOM bir olay modeline mekanizmadır. Olayları COM nesneleri olarak gönderilir ve aşağıda belirttiğiniz parametreler her olay vardır:  
  
- Olay adında DE.  
  
- Ne açıklaması.  
  
- İşlem, program ve iş parçacığı bilgisi, olayın gerçekleştiği bağlamı tanımlar. İşlem, bir DE gönderilen olaylar için gönderilmez.  
  
- Zaman uyumlu veya zaman uyumsuz olay olup olmadığını belirten bir olay türü.  
  
  Tüm hata ayıklama olaylarını yöntemi kullanılarak gönderilen [IDebugEventCallback2::Event](../../extensibility/debugger/reference/idebugeventcallback2-event.md).  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Olay Kaynakları](../../extensibility/debugger/event-sources-visual-studio-sdk.md)  
 İki olay kaynağını açıklar: hata ayıklama altyapısı (DE) ve oturum Yöneticisi (SDM) hata ayıklama.  
  
 [Desteklenen Olay Türleri](../../extensibility/debugger/supported-event-types.md)  
 Şu anda desteklenen olay türleri ele alınmaktadır: zaman uyumsuz ve zaman uyumlu.  
  
 [Olay Açıklamaları](../../extensibility/debugger/event-descriptions.md)  
 Olayları ve bunların kullanılması nedeniyle tanımlar.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Özel Hata Ayıklama Altyapısı Oluşturma](../../extensibility/debugger/creating-a-custom-debug-engine.md)  
 Bir DE hata ayıklama hizmetleri sağlamak için yorumlayıcı veya işletim sistemi ile nasıl çalıştığı açıklanır.
