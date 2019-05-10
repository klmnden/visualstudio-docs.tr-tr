---
title: IEEDataStorage::GetSize | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEEDataStorage::GetSize
helpviewer_keywords:
- IEEDataStorage::GetSize
ms.assetid: 33d232c4-1239-4abc-922b-e1bc5b908169
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: e5bcbfe60284cb254054e66b9e03b5e0e31ce4b1
ms.sourcegitcommit: 6196d0b7fdcb08ba6d28a8151ad36b8d1139f2cc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65224128"
---
# <a name="ieedatastoragegetsize"></a>IEEDataStorage::GetSize
Bu nesnede bulunan bayt sayısını döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetSize(
   ULONG* size
);
```

```csharp
int GetSize(
   out uint size
);
```

## <a name="parameters"></a>Parametreler
 `size`\

 [out] Bu nesnede bulunan bayt sayısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Kullanım [GetData](../../../extensibility/debugger/reference/ieedatastorage-getdata.md) gerçek veri baytı almak için yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)
- [GetData](../../../extensibility/debugger/reference/ieedatastorage-getdata.md)