---
title: THREADPROPERTIES | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- THREADPROPERTIES
helpviewer_keywords:
- THREADPROPERTIES structure
ms.assetid: 7d397207-db03-4ec0-9f79-3794056ed89f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 59b0fd83202ea8a5514d1ed637404d4864bf6b57
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65460718"
---
# <a name="threadproperties"></a>THREADPROPERTIES
Bir iş parçacığı özelliklerini açıklar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _tagTHREADPROPERTIES { 
   THREADPROPERTY_FIELDS dwFields;
   DWORD                 dwThreadId;
   DWORD                 dwSuspendCount;
   DWORD                 dwThreadState;
   BSTR                  bstrPriority;
   BSTR                  bstrName;
   BSTR                  bstrLocation;
} THREADPROPERTIES;
```

```csharp
public struct THREADPROPERTIES { 
   public uint   dwFields;
   public uint   dwThreadId;
   public uint   dwSuspendCount;
   public uint   dwThreadState;
   public string bstrPriority;
   public string bstrName;
   public string bstrLocation;
};
```

## <a name="members"></a>Üyeler
 `dwFields`\
 Bayraklarının bir birleşimi [THREADPROPERTY_FIELDS](../../../extensibility/debugger/reference/threadproperty-fields.md) bu yapının hangi alanlarda geçerli olduğunu açıklayan sabit listesi,.

 `dwThreadId`\
 İş parçacığı kimliği.

 `dwSuspendCount`\
 İş parçacığını askıya alma sayısı.

 `dwThreadState`\
 Bir değer [THREADSTATE](../../../extensibility/debugger/reference/threadstate.md) çalışma iş parçacığı durumunu belirten sabit listesi.

 `bstrPriority`\
 İş parçacığı önceliği belirten bir dize; Örneğin, "yukarıda Normal", "Normal" veya "Zaman kritik".

 `bstName`\
 İş parçacığı adı.

 `bstrLocation`\
 Genellikle burada yürütme şu anda durdu yöntemin adı ifade edilen iş parçacığı konumu (en üstteki yığın çerçevesi genellikle).

## <a name="remarks"></a>Açıklamalar
 Bu yapı için bir çağrı tarafından doldurulur [GetThreadProperties](../../../extensibility/debugger/reference/idebugthread2-getthreadproperties.md) yöntemi. Bu nedenle döndürülen bilgileri, genellikle doldurma içinde kullanılır **iş parçacıkları** penceresi.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [GetThreadProperties](../../../extensibility/debugger/reference/idebugthread2-getthreadproperties.md)
- [THREADPROPERTY_FIELDS](../../../extensibility/debugger/reference/threadproperty-fields.md)
- [THREADSTATE](../../../extensibility/debugger/reference/threadstate.md)