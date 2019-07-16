---
title: Çağrı yığını değerlendirme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], call stack evaluation
- call stacks, evaluation
ms.assetid: 373d6b49-0459-4cce-816e-05745a44fe49
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 15fecbc61fec8ba7aa62ca7d79cf11c56b7ce938
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68146409"
---
# <a name="call-stack-evaluation"></a>Çağrı Yığını Değerlendirme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Kesme modu sırasında yığın çerçevelerini çağrı yığını görmek için uygulamanız gereken [EnumFrameInfo](../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md) yöntemi.  
  
## <a name="methods-for-evaluation"></a>Değerlendirme için yöntemleri  
 Basit hata ayıklama altyapısı (DE), yalnızca bir yığın çerçevesi olabilir. Kesme modu sırasında yığın çerçevesini incelemek için aşağıdaki yöntemleri uygulamalıdır [IDebugStackFrame2](../../extensibility/debugger/reference/idebugstackframe2.md).  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetCodeContext](../../extensibility/debugger/reference/idebugstackframe2-getcodecontext.md)|Kod bağlamı için bir yığın çerçevesini alır. Kod bağlamı dosyadaki geçerli yönerge işaretçisini bir yığın çerçevesinde temsil eder.|  
|[GetDocumentContext](../../extensibility/debugger/reference/idebugstackframe2-getdocumentcontext.md)|Belge bağlamı için bir yığın çerçevesini alır. Belge bağlamı geçerli yığın çerçevesi için kaynak kodu konumu temsil eder. Bir programda durduğunda, kaynak kodunu görüntülemek için gereklidir.|  
  
 Bu yöntemlerin birden çok içerik ile ilgili arabirimler ve yöntemler uygulaması gerektirir. Bu nedenle, uygulamanız gereken [GetDocumentContext](../../extensibility/debugger/reference/idebugcodecontext2-getdocumentcontext.md) yöntemi ve aşağıdaki yöntemlerden birini [IDebugDocumentContext2](../../extensibility/debugger/reference/idebugdocumentcontext2.md).  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetStatementRange](../../extensibility/debugger/reference/idebugdocumentcontext2-getstatementrange.md)|Bir belge bağlamına dosya deyimi aralığını alır.|  
  
 Kod bağlamı numaralandırmak için tüm yöntemleri uygulamalıdır [IEnumDebugCodeContexts2](../../extensibility/debugger/reference/ienumdebugcodecontexts2.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yürütme Denetimi ve Durum Değerlendirmesi](../../extensibility/debugger/execution-control-and-state-evaluation.md)
