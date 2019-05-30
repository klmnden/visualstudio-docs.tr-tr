---
title: THREADSTATE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- THREADSTATE
helpviewer_keywords:
- THREADSTATE enumeration
ms.assetid: 62efdd7c-25b1-4fd3-9d06-ac1830a418a9
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 50f487b3d44fc1b871b00348ec28693b36c49685
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66316138"
---
# <a name="threadstate"></a>THREADSTATE
İş parçacığı durumunu belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_THREADSTATE { 
   THREADSTATE_RUNNING = 0x0001,
   THREADSTATE_STOPPED = 0x0002,
   THREADSTATE_FRESH   = 0x0003,
   THREADSTATE_DEAD    = 0x0004,
   THREADSTATE_FROZEN  = 0x0005
};
typedef DWORD THREADSTATE;
```

```csharp
public enum enum_THREADSTATE { 
   THREADSTATE_RUNNING = 0x0001,
   THREADSTATE_STOPPED = 0x0002,
   THREADSTATE_FRESH   = 0x0003,
   THREADSTATE_DEAD    = 0x0004,
   THREADSTATE_FROZEN  = 0x0005
};
```

## <a name="fields"></a>Alanlar
 `THREADSTATE_RUNNING`\
 İş parçacığı çalıştığını gösterir.

 `THREADSTATE_STOPPED`\
 İş parçacığı bir kesme noktası nedeniyle durdurulduğunu gösterir.

 `THREADSTATE_FRESH`\
 İş parçacığı oluşturuldu, ancak henüz kod çalışmıyor gösterir.

 `THREADSTATE_DEAD`\
 İş parçacığı geçersiz olduğunu gösterir.

 `THREADSTATE_FROZEN`\
 İş parçacığı'nın dondurulmuş olup olmadığını gösterir (hiçbir yürütme gerçekleştirilebilir).

## <a name="remarks"></a>Açıklamalar
 İçin kullanılan `dwThreadState` alanını [THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md) yapısı.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md)