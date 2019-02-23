---
title: IDebugField::GetContainer | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugField::GetContainer
helpviewer_keywords:
- IDebugField::GetContainer method
ms.assetid: 6d6c8213-6181-4adf-9584-3e4cac163dd8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 283e23a70b95e3882569dbb18dda7ba365b8b765
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56718150"
---
# <a name="idebugfieldgetcontainer"></a>IDebugField::GetContainer
Bu yöntem, bir alan kapsayıcısını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetContainer( 
   IDebugContainerField** ppContainerField
);
```

```csharp
int GetContainer(
   out IDebugContainerField ppContainerField
);
```

#### <a name="parameters"></a>Parametreler
 `ppContainerField`

 [out] Kapsayıcı tarafından temsil edilen döndürür [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md) arabirimi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu alan döndürülen bir kapsayıcı yoksa `ppContainerField` bir null değer olacaktır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md)