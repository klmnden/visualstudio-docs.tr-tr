---
title: IDebugDocumentText2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugDocumentText2
helpviewer_keywords:
- IDebugDocumentText2 interface
ms.assetid: e85f50a3-211c-4220-a9f4-789950ba2782
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: cae0bfefe4ab39d42f9cc67080d17394b1a1418b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53838430"
---
# <a name="idebugdocumenttext2"></a>IDebugDocumentText2
Bu arabirim, bir metin belgesi temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugDocumentText2 : IDebugDocument2  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Metin biçiminde sağlaması gerekir kaynak kodu olduğunda, hata ayıklama altyapısı (DE) Bu arabirim uygular. Bir DE kullanılıyorsa, bu en sık karşılaşılan durum olduğundan [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md) arabirimi, bu da uygulamanız gerekir `IDebugDocumentText2` arabirimi.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Kullanım `QueryInterface` bu arabirimden elde etmek için yöntemi bir `IDebugDocument2` arabirimi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Yöntemlere ek olarak `IDebugDocument2` arabirimi bu arabirim, aşağıdaki yöntemleri uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetSize](../../../extensibility/debugger/reference/idebugdocumenttext2-getsize.md)|Belgedeki bu konumda metin boyutunu alır.|  
|[GetText](../../../extensibility/debugger/reference/idebugdocumenttext2-gettext.md)|Belge belirtilen konumda metin alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirimi uygulayan bir nesne de uygulamalıdır <xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer> arabirim, hangi kaynakları <xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint> için arabirim bir [IDebugDocumentTextEvents2](../../../extensibility/debugger/reference/idebugdocumenttextevents2.md) nesne.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md)   
 [IDebugDocumentTextEvents2](../../../extensibility/debugger/reference/idebugdocumenttextevents2.md)