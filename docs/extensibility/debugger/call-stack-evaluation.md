---
title: Çağrı yığını değerlendirme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], call stack evaluation
- call stacks, evaluation
ms.assetid: 373d6b49-0459-4cce-816e-05745a44fe49
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fa28460c2680a5301768c950eac39caefc5d1dae
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66332481"
---
# <a name="call-stack-evaluation"></a>Çağrı yığını değerlendirme
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

## <a name="see-also"></a>Ayrıca bkz.
- [Yürütme denetimi ve durum değerlendirmesi](../../extensibility/debugger/execution-control-and-state-evaluation.md)