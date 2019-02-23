---
title: IDebugMethodField::EnumArguments | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugMethodField::EnumArguments
helpviewer_keywords:
- IDebugMethodField::EnumArguments method
ms.assetid: 3ab55488-2437-4ff6-a9ae-78ea6d7b23a8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bf62392118ed3ddfb2dfbfca06588f0935f3192d
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56719905"
---
# <a name="idebugmethodfieldenumarguments"></a>IDebugMethodField::EnumArguments
Yöntemini çağırmak için gereken her bağımsız değişken türü için bir numaralandırıcı oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumArguments( 
   IEnumDebugFields** ppParams
);
```

```csharp
int EnumArguments(
   out IEnumDebugFields ppParams
);
```

#### <a name="parameters"></a>Parametreler
 `ppParams`

 [out] Döndürür bir [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) bağımsız değişken türleri listesini temsil eden nesne. Hiçbir bağımsız değişken varsa, bir null değer döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür veya hiçbir bağımsız değişken varsa S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Her öğe bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) her parametre türleri temsil eden nesne. Çağrı [GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md) her parametresinin türü hakkında bilgi almak için yöntemi.

 Parametrenin adı türü ile birlikte gerekirse, ardından çağırın [EnumParameters](../../../extensibility/debugger/reference/idebugmethodfield-enumparameters.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)
- [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [EnumParameters](../../../extensibility/debugger/reference/idebugmethodfield-enumparameters.md)