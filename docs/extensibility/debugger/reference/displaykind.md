---
title: DisplayKind | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- DisplayKind enumeration
ms.assetid: 940968c5-6065-4bda-8ee6-c31597db4d71
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: fd75220c202d65c11ac695e4fa27e736595cbc86
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53828884"
---
# <a name="displaykind"></a>DisplayKind
Düzenleyicinin bilgilerin türlerini temsil eden geçerli değerleri numaralandırır bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) nesne ve kullanıcıya görüntüler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
enum enum_DisplayKind  
{  
   DisplayKind_Value = 0x1,  
   DisplayKind_Name = 0x2,  
   DisplayKind_Type = 0x3,  
};  
typedef DWORD DisplayKind;  
```  
  
```csharp  
public enum enum_DisplayKind  
{  
   DisplayKind_Value = 0x1,  
   DisplayKind_Name = 0x2,  
   DisplayKind_Type = 0x3,  
};  
```  
  
#### <a name="parameters"></a>Parametreler  
 DisplayKind_Value  
 Alanın değeri.  
  
 DisplayKind_Name  
 Alanın adı.  
  
 DisplayKind_Type  
 Alan türü.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: EE.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetValueDisplayStringCount](../../../extensibility/debugger/reference/ieevisualizerservice-getvaluedisplaystringcount.md)