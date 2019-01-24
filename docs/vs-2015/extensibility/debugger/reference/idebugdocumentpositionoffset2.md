---
title: IDebugDocumentPositionOffset2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- IDebugDocumentPositionOffset2 interface
ms.assetid: f1b05db3-50d8-453f-a72f-e68b239236a4
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c1f30c3a465d4803e5c91f14ee45ad582e76d986
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54752710"
---
# <a name="idebugdocumentpositionoffset2"></a>IDebugDocumentPositionOffset2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir karakter uzaklığı olarak kaynak dosyada bir konumu temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugDocumentPositionOffset2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 IDE tarafından uygulanan ve hata ayıklama motoru tarafından tüketilen.  
  
## <a name="methods"></a>Yöntemler  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugDocumentPositionOffset2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetRange](../../../extensibility/debugger/reference/idebugdocumentpositionoffset2-getrange.md)|Geçerli belge konumunu aralığını alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu aynı bilgileri döndürür [GetRange](../../../extensibility/debugger/reference/idebugdocumentposition2-getrange.md) ancak `char` belgenin başından kaydırır. Bu bir diskte diğer bir deyişle, normalde döndürülen satır ve sütun bilgisi yerine karakterlerin tek boyutlu dizi var gibi bu belgeyi sunar.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentPosition2](../../../extensibility/debugger/reference/idebugdocumentposition2.md)
