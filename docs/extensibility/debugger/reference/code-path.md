---
title: CODE_PATH | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- CODE_PATH
helpviewer_keywords:
- CODE_PATH structure
ms.assetid: 2d4b2890-4c9d-47e1-83c0-df9c6436427f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3d8459fd900edd0aba4532a8ce3e082dc4f300eb
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54966225"
---
# <a name="codepath"></a>CODE_PATH
Bir yöntem veya işlev çağrısı açıklar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
typedef struct tagCODE_PATH {   
   BSTR                bstrName;  
   IDebugCodeContext2* pCode;  
} CODE_PATH;  
```  
  
```csharp  
public struct CODE_PATH {  
   public string            bstrName;  
   public IDebugCodeContext pCode;  
}  
```  
  
## <a name="members"></a>Üyeler  
 bstrName  
 Kod yolu adı.  
  
 pCode  
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) bir işleve için kodu nerede tanımlayan nesne.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yapı, bir işlevin Adımlama uygulamak için kullanılır. [EnumCodePaths](../../../extensibility/debugger/reference/idebugprogram2-enumcodepaths.md) tüm çağrıları ayıklanan programın geçerli konumu döndürür. Bu yapı, böyle bir çağrısını temsil eder.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılar ve birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)   
 [EnumCodePaths](../../../extensibility/debugger/reference/idebugprogram2-enumcodepaths.md)