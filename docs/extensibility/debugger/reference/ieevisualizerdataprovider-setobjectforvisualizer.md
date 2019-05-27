---
title: IEEVisualizerDataProvider::SetObjectForVisualizer | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEEVisualizerDataProvider::SetObjectForVisualizer
helpviewer_keywords:
- IEEVisualizerDataProvider::SetObjectForVisualizer method
ms.assetid: 40dad2be-57ff-4f74-9d82-c48039c125c4
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 31bc89e248d609e8b828d4cc5b9ac41c8e15c70c
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66203700"
---
# <a name="ieevisualizerdataprovidersetobjectforvisualizer"></a>IEEVisualizerDataProvider::SetObjectForVisualizer
Bu yöntem Görselleştirici temsil eden nesneyi değiştirir.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetObjectForVisualizer(
   IDebugObject*  pNewObject,
   BSTR*          error,
   IDebugObject** pException
);
```

```csharp
int SetObjectForVisualizer(
   IDebugObject     pNewObject,
   out string       error,
   out IDebugObject pException
);
```

## <a name="parameters"></a>Parametreler
`pNewObject`\
[in] Ayarlanacağı nesne.

`error`\
[out] Bu dize, nesne ayarlanırken bir hata oluştu, hata iletisi tutar.

`pException`\
[out] Bir hata varsa, bu nesne, özel durum bilgilerini tutar.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu, nasıl hata bilgileri döndürülür belirlemek için en fazla uygulayan olur. Ancak, bir hata olduğunda bu yöntem her zaman bir özel durum nesnesi döndürmelidir bu nedenle bir özel durum nesnesi var. bilmek döndürüldü, görmek için Görünüm, bir hata oluştu. yalnızca bazı çağıranlar olabilir mümkündür. Çağıranın olun ister durumunda hata dizesi ayrıca sağlanan bunu kullanın.

## <a name="see-also"></a>Ayrıca bkz.
- [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md)
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)