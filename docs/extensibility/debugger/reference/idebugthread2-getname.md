---
title: IDebugThread2::GetName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugThread2::GetName
helpviewer_keywords:
- IDebugThread2::GetName
ms.assetid: eec54b8f-4a0e-4919-b0f9-81d4bd1e0b6f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: d6b57aac800027a4a591c3ea683761e19a31462c
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66320220"
---
# <a name="idebugthread2getname"></a>IDebugThread2::GetName
Bir iş parçacığı adını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetName ( 
   BSTR* pbstrName
);
```

```csharp
int GetName ( 
   out string pbstrName
);
```

## <a name="parameters"></a>Parametreler
`pbstrName`\
[out] İş parçacığı adını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Alınan adı her zaman görüntülenebilir bir addır ve bu ad iş parçacığı açıklar. İş parçacığı adı türetilen destekler adlı iş parçacıkları veya hata ayıklama altyapısı türetilmiş bir ad olabilir bir çalışma zamanı mimarisi. Alternatif olarak, iş parçacığının adı için bir çağrı tarafından ayarlanabilir [SetThreadName](../../../extensibility/debugger/reference/idebugthread2-setthreadname.md) yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
- [SetThreadName](../../../extensibility/debugger/reference/idebugthread2-setthreadname.md)