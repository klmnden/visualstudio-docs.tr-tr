---
title: IDebugDocumentContext2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugDocumentContext2
helpviewer_keywords:
- IDebugDocumentContext2
ms.assetid: 2a446c71-8100-4c09-a1cc-fd446bd74030
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: b6d040597f48d4514a58027df3335c080d6305a4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68144951"
---
# <a name="idebugdocumentcontext2"></a>IDebugDocumentContext2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim bir konumda bir kaynak dosyası belgeyi temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugDocumentContext2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı (DE), kaynak kod düzeyinde hata ayıklama desteği bir parçası olarak bu arabirimi uygular. Kaynak kodunda bir konuma ek olarak, bu arabirim bağlamları karşılaştırma ve kaynak kodu belgesinin arasında gezinmek için yöntemler sağlar.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 En yaygın yöntemlerde birkaç arabirimleri [GetDocumentContext](../../../extensibility/debugger/reference/idebugstackframe2-getdocumentcontext.md) ve [GetDocumentContext](../../../extensibility/debugger/reference/idebugcodecontext2-getdocumentcontext.md) arabirimler, bu arabirim döndürür.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugDocumentContext2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetDocument](../../../extensibility/debugger/reference/idebugdocumentcontext2-getdocument.md)|Bu belge bağlamına içeren belgeyi alır.|  
|[GetName](../../../extensibility/debugger/reference/idebugdocumentcontext2-getname.md)|Bu belge bağlamına içeren belge görüntülenebilir adını alır.|  
|[EnumCodeContexts](../../../extensibility/debugger/reference/idebugdocumentcontext2-enumcodecontexts.md)|Bu belge bağlamı ile ilişkili tüm kod bağlamı bir listesini alır.|  
|[GetLanguageInfo](../../../extensibility/debugger/reference/idebugdocumentcontext2-getlanguageinfo.md)|Bu belge bağlamı ile ilişkili dilini alır.|  
|[GetStatementRange](../../../extensibility/debugger/reference/idebugdocumentcontext2-getstatementrange.md)|Bu belge bağlamına dosya deyimi aralığını alır.|  
|[GetSourceRange](../../../extensibility/debugger/reference/idebugdocumentcontext2-getsourcerange.md)|Bu belge bağlamına dosya kaynağı aralığını alır.|  
|[Compare](../../../extensibility/debugger/reference/idebugdocumentcontext2-compare.md)|Bu belge bağlamları belirli bir dizi belge bağlamına karşılaştırır.|  
|[Seek](../../../extensibility/debugger/reference/idebugdocumentcontext2-seek.md)|Belge bağlamı belirli sayıda deyimleri veya satırları tarafından taşır.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [GetDocumentContext](../../../extensibility/debugger/reference/idebugcanstopevent2-getdocumentcontext.md)   
 [GetDocumentContext](../../../extensibility/debugger/reference/idebugactivatedocumentevent2-getdocumentcontext.md)   
 [GetDocumentContext](../../../extensibility/debugger/reference/idebugstackframe2-getdocumentcontext.md)   
 [GetDocumentContext](../../../extensibility/debugger/reference/idebugcodecontext2-getdocumentcontext.md)
