---
title: IDebugFunctionObject2::CreateObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugFunctionObject2::CreateObject
- CreateObject
ms.assetid: 148de615-941e-4b64-ab11-75b692aae465
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 23380106a1c78ba139beec94698bcfa5090c4b08
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66200750"
---
# <a name="idebugfunctionobject2createobject"></a>IDebugFunctionObject2::CreateObject
Verilen değerlendirme bayrağı ayarlar ve bir zaman aşımı değeri bir oluşturucu kullanan bir nesne oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT CreateObject (
   IDebugFunctionObject* pConstructor,
   DWORD                 dwArgs,
   IDebugObject*         pArgs[],
   DWORD                 dwEvalFlags,
   DWORD                 dwTimeout,
   IDebugObject**        ppObject
);
```

```csharp
int CreateObject (
   IDebugFunctionObject pConstructor,
   uint                 dwArgs,
   IDebugObject[]       pArgs,
   uint                 dwEvalFlags,
   uint                 dwTimeout,
   out IDebugObject**   ppObject
);
```

## <a name="parameters"></a>Parametreler
`pConstructor`\
[in] Bir [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) Oluşturucusu oluşturulacak nesne, temsil eden nesne.

`dwArgs`\
[in] Parametre sayısı `pArg` dizisi. Oluşturucuya geçirilen parametrelerin sayısını temsil eder.

`pArgs`\
[in] Bir dizi [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) parametreleri temsil eden nesneleri, oluşturucuya geçirilen.

`dwEvalFlags`\
[in] Bayraklarının bir birleşimi [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md) nasıl gerçekleştirilecek bir değerlendirme olduğunu belirten sabit listesi.

`dwTimeout`\
[in] Bu yöntemden geri dönmeden önce beklenecek milisaniye cinsinden en uzun süre. Kullanım **SONSUZ** süresiz bekleme.

`ppObject`\
[out] Döndürür bir **IDebugObject** temsil eden yeni oluşturulan nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir sınıf ya da bir parametresi olan bir oluşturucu gerektiren diğer karmaşık bir tür örneği temsil eden bir nesne oluşturmak için bu yöntemi çağırın.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugFunctionObject2](../../../extensibility/debugger/reference/idebugfunctionobject2.md)