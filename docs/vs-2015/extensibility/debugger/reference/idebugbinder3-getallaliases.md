---
title: IDebugBinder3::GetAllAliases | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBinder3::GetAllAliases
helpviewer_keywords:
- IDebugBinder3::GetAllAliases method
ms.assetid: 1f9ab2ee-2ab3-4a61-8b99-95dd7fdf3511
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: dc2075ccc37d280640f7559b1454990ee6684f25
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62555754"
---
# <a name="idebugbinder3getallaliases"></a>IDebugBinder3::GetAllAliases
Bu yöntem programın diğer adları listesini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetAllAliases(
   UINT          uRequest,
   IDebugAlias** ppAliases,
   UINT*         puFetched
);
```

```csharp
int GetAllAliases(
   uint          uRequest,
   IDebugAlias[] ppAliases,
   out uint      puFetched
);
```

#### <a name="parameters"></a>Parametreler
 `uRequest`

 [in] En fazla sayısını döndürmek için diğer adlar (içine geçirilen dizinin uzunluğunu belirtir `ppAliases`).

 `ppAliases`

 [out içinde] Diğer adlar ile oturum doldurmak için dizi (Bu bir null değer ise ve `uRequest` 0 ise, döndürülen diğer adlar sayısı tarafından döndürülen `puFetched`).

 `puFetched`

 [out] Elde ettiğiniz diğer adları sayısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugBinder3](../../../extensibility/debugger/reference/idebugbinder3.md)