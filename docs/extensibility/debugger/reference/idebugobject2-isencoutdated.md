---
title: IDebugObject2::IsEncOutdated | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject2::IsEncOutdated
helpviewer_keywords:
- IDebugObject2::IsEncOutdated method
ms.assetid: d3a8c02d-895b-478c-9957-d663130f308e
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 9b2d26b49f3d2597e12e11a323a9281bd5c676fa
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66317410"
---
# <a name="idebugobject2isencoutdated"></a>IDebugObject2::IsEncOutdated
Bu yöntem, bu nesnenin veya üst kapsayıcı düzenleme ve devam et durumu güncel olup olmadığını belirler. Özel ifade değerlendiricisi, bu yöntem ve her zaman döndürür uygulamıyor `E_NOTIMPL`.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT IsEncOutdated(
   BOOL* pfEncOutdated
);
```

```csharp
int IsEncOutdated(
   out int pfEncOutdated
);
```

## <a name="parameters"></a>Parametreler
`pfEncOutdated`\
[out] Sıfır olmayan (`TRUE`) Düzenle ve devam et durumu güncel olduğunda sıfır (`FALSE`), değilse.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

> [!NOTE]
> Özel ifade değerlendiricisi her zaman döndürmelidir `E_NOTIMPL`.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)