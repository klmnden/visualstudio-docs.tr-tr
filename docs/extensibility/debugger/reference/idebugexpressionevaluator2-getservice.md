---
title: IDebugExpressionEvaluator2::GetService | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugExpressionEvaluator2::GetService
- GetService
ms.assetid: f8988a9e-9d18-42af-84a7-55f41e9adf63
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ac6f73e31e7e15a2ffd86e2d969f98a686fbd004
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56677701"
---
# <a name="idebugexpressionevaluator2getservice"></a>IDebugExpressionEvaluator2::GetService
Bir hizmet nesnesi verilen benzersiz tanımlayıcısını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetService (
   GUID        uid,
   IUnknown ** ppService
);
```

```csharp
int GetService (
   Guid       uid,
   out object ppService
);
```

#### <a name="parameters"></a>Parametreler
 `uid`

 [in] Alınacak hizmet benzersiz tanımlayıcısı.

 `ppService`

 [out] Hizmeti temsil eden bir nesne döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu hizmetleri başka bir ifade değerlendiricisi ' elde etmek için bir üçüncü taraf ifade değerlendiricisi tarafından kullanılabilir. Örneğin, bu yöntem, arabirim Görselleştirici hizmeti için varsayılan ifade değerlendiricisi ' elde etmek için kullanılabilir. Üçüncü taraf ifade değerlendiricilerini bu arabirimi uygulayan gerek düşüktür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugExpressionEvaluator2](../../../extensibility/debugger/reference/idebugexpressionevaluator2.md)