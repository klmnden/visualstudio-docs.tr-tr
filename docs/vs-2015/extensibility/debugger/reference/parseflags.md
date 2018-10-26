---
title: PARSEFLAGS | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- PARSEFLAGS
helpviewer_keywords:
- PARSEFLAGS enumeration
ms.assetid: 47943f0a-54cb-4493-a62e-5dba97bd4c35
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 27f0c32c8a432a6aaa0ef83b06d6b424486ce29b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49898362"
---
# <a name="parseflags"></a>PARSEFLAGS
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir ifade ayrıştırmayı belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
enum enum_PARSEFLAGS {   
   PARSE_EXPRESSION            = 0x0001,  
   PARSE_FUNCTION_AS_ADDRESS   = 0x0002,  
   PARSE_DESIGN_TIME_EXPR_EVAL = 0x1000  
};  
typedef DWORD PARSEFLAGS;  
```  
  
```csharp  
public enum enum_PARSEFLAGS {   
   PARSE_EXPRESSION            = 0x0001,  
   PARSE_FUNCTION_AS_ADDRESS   = 0x0002,  
   PARSE_DESIGN_TIME_EXPR_EVAL = 0x1000  
};  
```  
  
## <a name="members"></a>Üyeler  
 PARSE_EXPRESSION  
 İfade bir deyim olmadığını gösterir.  
  
 PARSE_FUNCTION_AS_ADDRESS  
 İfade bir adres olarak ayrıştırılması (ve daha sonra değerlendirilmesi için) olduğunu gösterir.  
  
 PARSE_DESIGN_TIME_EXPR_EVAL  
 Tasarım sırasında Ayrıştırılmakta olan ifade gösterir (diğer bir deyişle, bir tasarımcı açık olduğunda).  
  
## <a name="remarks"></a>Açıklamalar  
 Bir parametre olarak geçirilen [ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) ve [ayrıştırma](../../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md) yöntemleri.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md)   
 [Parse](../../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md)

