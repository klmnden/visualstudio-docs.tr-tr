---
title: IDebugStackFrame2::GetDebugProperty | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugStackFrame2::GetDebugProperty
helpviewer_keywords:
- IDebugStackFrame2::GetDebugProperty
ms.assetid: 02c2fa04-1424-4bca-9936-feaecd2afab6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 930f3d7ec2500adaaf9b499e4e327aedabaf8d52
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56691936"
---
# <a name="idebugstackframe2getdebugproperty"></a>IDebugStackFrame2::GetDebugProperty
Yığın çerçevesinin özellikleri açıklamasını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetDebugProperty ( 
   IDebugProperty2** ppDebugProp
);
```

```csharp
int GetDebugProperty ( 
   out IDebugProperty2 ppDebugProp
);
```

#### <a name="parameters"></a>Parametreler
 `ppDebugProp`

 [out] Döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) Bu yığın çerçevesinin özellikleri tanımlayan nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Çağırma [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md) yerel değişkenler, yöntem parametreleri, yazmaçlar ve yığın çerçevesiyle ilgili "this" işaretçisi uygun filtreleri yöntemle alabilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)