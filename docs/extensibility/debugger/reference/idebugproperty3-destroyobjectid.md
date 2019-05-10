---
title: IDebugProperty3::DestroyObjectID | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProperty3::DestroyObjectID
helpviewer_keywords:
- IDebugProperty3::DestroyObjectID
ms.assetid: bd08f356-cc67-4717-98c9-c3d00cad2040
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 3375ce22a9b66077d635acd9a5a98f2640662467
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65457685"
---
# <a name="idebugproperty3destroyobjectid"></a>IDebugProperty3::DestroyObjectID
Arayanın artık bu özelliği diğer tüm özellikleri benzersiz olarak tanımlamak önemli olduğunu gösteren bu özellik ile ilişkilendirilmiş benzersiz kimliği yok eder.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT DestroyObjectID(
   void
);
```

```csharp
int DestroyObjectID();
```

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 (Bunu zaten bunları dahili olarak benzersiz bir şekilde izlediğinden) bir özellik için benzersiz kimliklerini desteklemek hata ayıklama altyapısı gerektirmez, sadece döndürebilir sonra `E_NOTIMPL` bu yöntem için.

 Benzersiz kimliklerinin bir çağrı ile oluşturulur [CreateObjectID](../../../extensibility/debugger/reference/idebugproperty3-createobjectid.md) yöntemi çağıran, bu özellik, diğer özellikler arasında benzersiz olarak tanımlanıyorsa emin olmak ister.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)
- [CreateObjectID](../../../extensibility/debugger/reference/idebugproperty3-createobjectid.md)