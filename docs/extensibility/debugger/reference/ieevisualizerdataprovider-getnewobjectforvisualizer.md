---
title: IEEVisualizerDataProvider::GetNewObjectForVisualizer | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEEVisualizerDataProvider::GetNewObjectForVisualizer
helpviewer_keywords:
- IEEVisualizerDataProvider::GetNewObjectForVisualizer method
ms.assetid: a898d549-4898-4fde-aad1-e8bb89129652
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 95a06a283b417432fd755f100f8c2e68a0325571
ms.sourcegitcommit: 6196d0b7fdcb08ba6d28a8151ad36b8d1139f2cc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65225894"
---
# <a name="ieevisualizerdataprovidergetnewobjectforvisualizer"></a>IEEVisualizerDataProvider::GetNewObjectForVisualizer
Bu yöntem, yeni bir nesne için Görselleştirici alır. Bu yöntem, varolan nesneyi her zaman yeni bir nesne oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetNewObjectForVisualizer(
   IDebugObject** ppObject
);
```

```csharp
int GetNewObjectForVisualizer(
   out IDebugObject ppObject
);
```

## <a name="parameters"></a>Parametreler
 `ppObject`\

 [out] Yeni nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 `This method` Nesne şu anda temsil eder ve sonuç yeni bir nesne olarak döndüren yeniden değerlendirir. Varolan nesne değerlendirmesinin sonucu olarak güncelleştirilecektir.

## <a name="see-also"></a>Ayrıca bkz.
- [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md)
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)