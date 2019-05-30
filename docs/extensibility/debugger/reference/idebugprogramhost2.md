---
title: IDebugProgramHost2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramHost2
helpviewer_keywords:
- IDebugProgramHost2 interface
ms.assetid: 2c37b3aa-97a9-4665-8709-edd917f18cb1
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: dc7a3222b2fab85657eea1eb0203f8c8da7dd5dc
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351226"
---
# <a name="idebugprogramhost2"></a>IDebugProgramHost2
Bu arabirim bir programla ilgili konak (işlem) bilgi sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugProgramHost2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı aynı nesne üzerinde bu arabirimi uygulayan [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) barındırma işlemi hakkında bilgi sağlamak için arabirim. Bu isteğe bağlı bir arabirimdir.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde bir `IDebugProgram2` arabirimi bu arabirim elde edilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProgramHost2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetHostName](../../../extensibility/debugger/reference/idebugprogramhost2-gethostname.md)|Başlık, kolay ad veya bu programın barındırma işlemi dosya adını alır.|
|[GetHostId](../../../extensibility/debugger/reference/idebugprogramhost2-gethostid.md)|Bu programın barındırma işlemin işlem tanımlayıcısını alır.|
|[GetHostMachineName](../../../extensibility/debugger/reference/idebugprogramhost2-gethostmachinename.md)|Barındırma işlemi bu programın üzerinde çalıştığı makinenin adını alır.|

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)