---
title: IDebugFunctionObject2::Evaluate | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugFunctionObject2::Evaluate
ms.assetid: bc54c652-904b-4297-a6db-faa329684881
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 441126724c78c2045e3e870fcdf7baa23f9149c3
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56708790"
---
# <a name="idebugfunctionobject2evaluate"></a>IDebugFunctionObject2::Evaluate
İşlevini çağırır ve bir nesne olarak elde edilen değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Evaluate (
   IDebugObject** ppParams,
   DWORD          dwParams,
   DWORD          dwEvalFlags,
   DWORD          dwTimeout,
   IDebugObject** ppResult
);
```

```csharp
int Evaluate (
   IDebugObject     ppParams,
   uint             dwParams,
   uint             dwEvalFlags,
   uint             dwTimeout,
   out IDebugObject ppResult
);
```

#### <a name="parameters"></a>Parametreler
 `ppParams`

 [in] Bir dizi [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) giriş parametrelerini temsil eden nesneleri. Bu parametrelerin her biri, bu arabirimde Oluştur yöntemlerden birini kullanarak oluşturuldu.

 `dwParams`

 [in] Parametre sayısı `ppParams` dizisi.

 `dwEvalFlags`

 [in] Bayraklarının bir birleşimi [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md) nasıl gerçekleştirilecek bir değerlendirme olduğunu belirten sabit listesi.

 `dwTimeout`

 [in] Bu yöntemden geri dönmeden önce beklenecek milisaniye cinsinden en uzun süreyi belirtir. Kullanım **SONSUZ** süresiz bekleme.

 `ppResult`

 [out] Döndürür bir **IDebugObject** temsil eden bir nesne olarak işlevin değeri.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugFunctionObject2](../../../extensibility/debugger/reference/idebugfunctionobject2.md)