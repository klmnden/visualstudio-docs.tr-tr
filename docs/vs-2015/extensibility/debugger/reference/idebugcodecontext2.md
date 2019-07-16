---
title: IDebugCodeContext2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugCodeContext2
helpviewer_keywords:
- IDebugCodeContext2 interface
ms.assetid: 3670439e-2171-405d-9d77-dedb0f1cba93
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 2e06fd709b2d076b6fa8de7f104e907eb1b35a42
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68190950"
---
# <a name="idebugcodecontext2"></a>IDebugCodeContext2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, bir kod yönergesi başlangıç konumunu temsil eder. Çoğu çalışma zamanı mimarileri için bugün, bir kod bağlamı, program yürütme stream'de adresi olarak düşünülebilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugCodeContext2 : IDebugMemoryContext2  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı, bir kod yönergesi belge konumuna konumunu ilişkilendirmek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Birçok arabirimlerindeki yöntemler bu arabirimi en yaygın dönüş [GetCodeContext](../../../extensibility/debugger/reference/idebugstackframe2-getcodecontext.md). Ayrıca kapsamlı olarak kullanıldığında [IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md) kesme noktası çözümleme bilgileri olduğu gibi de arabirimi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Yöntemlere ek olarak [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) arabirimi bu arabirim, aşağıdaki yöntemleri uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetDocumentContext](../../../extensibility/debugger/reference/idebugcodecontext2-getdocumentcontext.md)|Etkin kod kapsamına karşılık gelen belge bağlamını alır.|  
|[GetLanguageInfo](../../../extensibility/debugger/reference/idebugcodecontext2-getlanguageinfo.md)|Bu kod bağlamı için dil bilgilerini alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Arasındaki temel fark bir `IDebugCodeContext2` arabirimi ve [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) arabirimi olan bir `IDebugCodeContext2` her zaman yönerge hizalanır. Diğer bir deyişle bir `IDebugCodeContext2` ise bir yönerge başlangıcına işaret her zaman bir `IDebugMemoryContext2` herhangi bayt bellek çalışma zamanı mimarisinde işaret edebilir. `IDebugCodeContext2` yönergeler yerine temel depolama alanı boyutu (bayt genellikle) göre artırılır.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [GetDisassemblyStream](../../../extensibility/debugger/reference/idebugprogram2-getdisassemblystream.md)   
 [CanSetNextStatement](../../../extensibility/debugger/reference/idebugthread2-cansetnextstatement.md)   
 [SetNextStatement](../../../extensibility/debugger/reference/idebugthread2-setnextstatement.md)   
 [GetCodeContext](../../../extensibility/debugger/reference/idebugcanstopevent2-getcodecontext.md)   
 [GetCodeContext](../../../extensibility/debugger/reference/idebugstackframe2-getcodecontext.md)   
 [Sonraki](../../../extensibility/debugger/reference/ienumdebugcodecontexts2-next.md)   
 [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)
