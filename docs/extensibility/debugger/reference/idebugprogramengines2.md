---
title: IDebugProgramEngines2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramEngines2
helpviewer_keywords:
- IDebugProgramEngines2 interface
ms.assetid: 53d648f0-6c11-4337-badd-c43f3872b62c
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b45cbe8cd1b68e1681b07fcdf1fc715973a11295
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66325257"
---
# <a name="idebugprogramengines2"></a>IDebugProgramEngines2
Bu arabirim tarafından program düğümleri bu programda hata ayıklamak tüm olası hata ayıklama altyapısı (DE) belirtmek için kullanılır.

## <a name="syntax"></a>Sözdizimi

```
IDebugProgramEngines2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bir DE veya özel bağlantı noktası sağlayıcısı bu arabirimi uygulayan aynı nesne üzerinde uygulayan [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md) belirli bir program için kullanılacak belirli bir DE oluşturma desteklemek için.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde bir `IDebugProgramNode2` arabirimi bu arabirim elde edilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProgramEngines2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[EnumPossibleEngines](../../../extensibility/debugger/reference/idebugprogramengines2-enumpossibleengines.md)|Bu programda hata ayıklamak olası DEs gösterir.|
|[SetEngine](../../../extensibility/debugger/reference/idebugprogramengines2-setengine.md)|Bu program hata ayıklama için kullanılacak DE seçer.|

## <a name="remarks"></a>Açıklamalar
 Bir DE kullanıcı tarafından seçilen sonra bu seçimi program düğümle çağırarak kayıtlı [SetEngine](../../../extensibility/debugger/reference/idebugprogramengines2-setengine.md). Seçili olan altyapı tarafından döndürülen altyapısı olur [GetEngineInfo](../../../extensibility/debugger/reference/idebugprogramnode2-getengineinfo.md).

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)
- [GetEngineInfo](../../../extensibility/debugger/reference/idebugprogramnode2-getengineinfo.md)