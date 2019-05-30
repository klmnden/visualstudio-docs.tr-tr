---
title: IDebugObject2::GetBackingFieldForProperty | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject2::GetBackingFieldForProperty
helpviewer_keywords:
- IDebugObject2::GetBackingFieldForProperty method
ms.assetid: e72c6338-5573-4fad-8075-f3ade3435424
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 9aaf4111670ad67f6a01bde60bf5f35c3b793983
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66317355"
---
# <a name="idebugobject2getbackingfieldforproperty"></a>IDebugObject2::GetBackingFieldForProperty
Alan veya değişken (varsa) alır, yedekleme bu nesne tarafından temsil edilen özelliği.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetBackingFieldForProperty(
   IDebugObject2** ppObject
);
```

```csharp
int GetBackingFieldForProperty(
   out IDebugObject2 ppObject
);
```

## <a name="parameters"></a>Parametreler
`ppObject`\
[out] Bir [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md) yedekleme alanını tanımlayan nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md) temsil eden bir yönetilen kod sınıf özelliği, diğer bir deyişle, bir get yöntemi nesnesi ve/veya set erişimcisine. Bu özellikler genellikle özelliği tarafından yönetilen değeri içeren bir değişkeni gerektirir. Bu değişken yedekleme alanı olarak bilinir. Nesne için yedekleme alanı yok ise, ardından bir null değer döndürmek emin olun: bazı çağıranlar dönüş değerine dikkatini ödeme değil ancak bunun yerine, bir null değer döndürüldü, görmek için görüneceğini `ppObject`.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)