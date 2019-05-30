---
title: IDebugPortSupplier2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortSupplier2
helpviewer_keywords:
- IDebugPortSupplier2 interface
ms.assetid: 37067324-2ea6-4a01-8829-a6e9c7a70068
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 947a311cb1e83eaa131730725aeb7938e5615f0f
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66340057"
---
# <a name="idebugportsupplier2"></a>IDebugPortSupplier2
Bu arabirim bağlantı noktalarına oturum hata ayıklama Yöneticisi (SDM) sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugPortSupplier2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
Özel bağlantı noktası sağlayıcısı bağlantı noktası sağlayıcısı temsil etmek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
Bir çağrı `CoCreateInstance` ile bir bağlantı noktası tedarikçi `GUID` (Bu, bu arabirimi sağlamak için normal şekilde) Bu arabirim döndürür. Örneğin:

```cpp
IDebugPortSupplier2 *GetPortSupplier(GUID *pPortSupplierGuid)
{
    IDebugPortSupplier2 *pPS = NULL;
    if (pPortSupplierGuid != NULL) {
        CComPtr<IDebugPortSupplier2> spPortSupplier;
        spPortSupplier.CoCreateInstance(*pPortSupplierGuid);
        if (spPortSupplier != NULL) {
            pPS = spPortSupplier.Detach();
        }
    }
    return (pPS);
}
```

Bir çağrı [GetPortSupplier](../../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md) tarafından kullanılan geçerli bağlantı noktası sağlayıcısı gösteren bu bir arabirim döndürür [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)].

- [GetPortSupplier](../../../extensibility/debugger/reference/idebugport2-getportsupplier.md) bağlantı noktası oluşturulan bağlantı noktası sağlayıcısı temsil eden bu arabirimi döndürür.

- [IEnumDebugPortSuppliers2](../../../extensibility/debugger/reference/ienumdebugportsuppliers2.md) listesini temsil `IDebugPortSupplier` arabirimleri ( `IEnumDebugPortSuppliers` arabirimi öğesinden alınan [EnumPortSuppliers](../../../extensibility/debugger/reference/idebugcoreserver2-enumportsuppliers.md), tüm bağlantı noktası sağlayıcıları temsil eden ilekayıtlı[!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)]).

Hata ayıklama altyapısı genellikle bağlantı noktası sağlayıcısı ile etkileşime girmez.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugPortSupplier2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetPortSupplierName](../../../extensibility/debugger/reference/idebugportsupplier2-getportsuppliername.md)|Bağlantı sağlayıcı adını alır.|
|[GetPortSupplierId](../../../extensibility/debugger/reference/idebugportsupplier2-getportsupplierid.md)|Bağlantı noktası tedarikçi tanımlayıcısını alır.|
|[GetPort](../../../extensibility/debugger/reference/idebugportsupplier2-getport.md)|Bir bağlantı noktasına bağlantı noktası sağlayıcısı alır.|
|[EnumPorts](../../../extensibility/debugger/reference/idebugportsupplier2-enumports.md)|Mevcut bağlantı noktalarını listeler.|
|[CanAddPort](../../../extensibility/debugger/reference/idebugportsupplier2-canaddport.md)|Bağlantı noktası sağlayıcısı yeni bağlantı noktaları ekleme desteklediğini doğrular.|
|[AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md)|Bir bağlantı noktası ekler.|
|[RemovePort](../../../extensibility/debugger/reference/idebugportsupplier2-removeport.md)|Bir bağlantı noktası kaldırır.|

## <a name="remarks"></a>Açıklamalar
Bağlantı noktası sağlayıcısı adı ve kimliği ile kendisini tanımlamak, ekleyin ve bağlantı noktalarını kaldırın ve bağlantı noktası sağlayıcısı sağlayan tüm bağlantı noktalarını listele.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [GetPortSupplier](../../../extensibility/debugger/reference/idebugport2-getportsupplier.md)
- [GetPortSupplier](../../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md)
- [IEnumDebugPortSuppliers2](../../../extensibility/debugger/reference/ienumdebugportsuppliers2.md)
