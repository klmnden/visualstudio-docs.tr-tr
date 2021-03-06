---
title: IEEDataStorage | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEEDataStorage
helpviewer_keywords:
- IEEDataStorage interface
ms.assetid: 704e932d-2325-410e-89c4-ce88c6ec19da
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ab42216df5c7d5f3d2d349ccf07e595ab3fc616c
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66335629"
---
# <a name="ieedatastorage"></a>IEEDataStorage
Bu arabirim, bayt dizisini temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IEEDataStorage : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 İfade değerlendirici (EE) bayt dizisini temsil etmek için bu arabirimi uygulayan (tür görselleştiricilerde almak ve verileri aracılığıyla değiştirmek için kullanılan [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md) arabirimi). EE genellikle dış tür görselleştiricileri desteklemek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Yöntemlerde `IPropertyProxyEESide` tüm arabirimi bu arabirim döndürür. Çağrı [GetPropertyProxy](../../../extensibility/debugger/reference/ipropertyproxyprovider-getpropertyproxy.md) edinme [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md) arabirimi. Çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde bir [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) almak için arabirimi [IPropertyProxyProvider](../../../extensibility/debugger/reference/ipropertyproxyprovider.md) arabirimi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 `IEEDataStorage` Arabirimi aşağıdaki yöntemleri uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[GetData](../../../extensibility/debugger/reference/ieedatastorage-getdata.md)|Belirtilen arabellek için sağlanan veri bayt sayısını alır.|
|[GetSize](../../../extensibility/debugger/reference/ieedatastorage-getsize.md)|Kullanılabilir veri bayt sayısını alır.|

## <a name="remarks"></a>Açıklamalar
 Bu arabirim, belirli bir nesne tarafından tutulan verilere erişmek için bir tür görselleştiricisi tarafından kullanılır. Veri yolu kullanıcıya sunmak için gerekli olan işlemek tür görselleştiricisi sağlayan bir bayt dizisi olarak değerlendirilir.

 Genellikle özel Görüntüleyici özel bir arabirim kullanır ancak özel Görüntüleyici de bu arabirimi isterseniz kullanabilirsiniz [GetMemoryBytes](../../../extensibility/debugger/reference/idebugproperty2-getmemorybytes.md) veya [GetStringChars](../../../extensibility/debugger/reference/idebugproperty3-getstringchars.md) (için dize odaklı veriler).

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)
- [Tür Görselleştiricisi ve Özel Görüntüleyici](../../../extensibility/debugger/type-visualizer-and-custom-viewer.md)