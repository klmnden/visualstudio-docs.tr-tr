---
title: IDebugObject::SetValue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject::SetValue
helpviewer_keywords:
- IDebugObject::SetValue method
ms.assetid: d652e09c-cdc1-4519-8116-d7c743f5679b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: fec036357fb92563eba81c919ab32fea2e58c3b3
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66211274"
---
# <a name="idebugobjectsetvalue"></a>IDebugObject::SetValue
Nesnenin değerini ardışık bir bayt serisinden ayarlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetValue( 
   BYTE* pValue,
   UINT  nSize
);
```

```csharp
int SetValue(
   byte[] pValue,
   uint   nSize
);
```

## <a name="parameters"></a>Parametreler
`pValue`\
[in] Yeni değeri temsil eden bir bayt dizisi.

`nSize`\
[in] Değerin bayt cinsinden boyutu.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Dizideki değerleri bu kopyalanır [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) herhangi bir mevcut değer değiştirme, nesne. Yeni değer boyutu, mevcut değerinden küçük veya çok büyük olabilir. Bu `IDebugObject` bir null başvuru olamaz.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)
- [GetValue](../../../extensibility/debugger/reference/idebugobject-getvalue.md)