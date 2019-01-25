---
title: IDebugDocument2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugDocument2
helpviewer_keywords:
- IDebugDocument2 interface
ms.assetid: 1bc58426-dbf5-4471-9aad-9d66cd80eef0
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 2cd6afb417de4d8a362916f91593d0d0e67d307c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54766754"
---
# <a name="idebugdocument2"></a>IDebugDocument2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, bir kaynak belge temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugDocument2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)] Genellikle bu arabirimi uygular. Bu kaynak kodu sağlaması gerekir ve kaynak disk üzerinde mevcut değil, hata ayıklama altyapısı (DE) Bu arabirim de uygulayabilirsiniz.  Böyle durumlarda da DE uygulamak [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) ve [IDebugActivateDocumentEvent2](../../../extensibility/debugger/reference/idebugactivatedocumentevent2.md) arabirimleri yanı sıra bazı ek yöntemlerde [ IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md) ve [IDebugDocumentPosition2](../../../extensibility/debugger/reference/idebugdocumentposition2.md) arabirimleri.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Yöntemlerde `IDebugDocumentContext2`, `IDebugDisassemblyStream2`, `IDebugDocumentPosition2`, ve `IDebugActivateDocumentEvent2` arabirimi bu arabirim döndürür.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugDocument2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetName](../../../extensibility/debugger/reference/idebugdocument2-getname.md)|Belge adını çeşitli biçimlerden birinde alır.|  
|[GetDocumentClassID](../../../extensibility/debugger/reference/idebugdocument2-getdocumentclassid.md)|Belge sınıfı tanımlayıcısını alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim, yalnızca kaynak kodu DE sağladığı zaman uygulanır. Bir HTML sayfasında komut dosyası ayıklanırken kaynak indirilen veya dinamik olarak oluşturulan gibi DE kaynak kodu sağlar ve bir disk dosyası olarak mevcut değil. C++ gibi geleneksel dilleri hata ayıklama sırasında uygulanması bu arabirimi gerekmez.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IsPositionInDocument](../../../extensibility/debugger/reference/idebugdocumentposition2-ispositionindocument.md)   
 [GetDocument](../../../extensibility/debugger/reference/idebugactivatedocumentevent2-getdocument.md)   
 [GetDocument](../../../extensibility/debugger/reference/idebugdocumentcontext2-getdocument.md)   
 [GetDocument](../../../extensibility/debugger/reference/idebugdocumentposition2-getdocument.md)   
 [GetDocument](../../../extensibility/debugger/reference/idebugdisassemblystream2-getdocument.md)
