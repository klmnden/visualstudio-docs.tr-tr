---
title: IDebugAddress::GetAddress | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugAddress::GetAddress
helpviewer_keywords:
- IDebugAddress:GetAddress method
ms.assetid: 2590387b-5d36-4116-9a75-737957b8898e
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: f787f041c6c39b8120a768f9288efe86649bb227
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66318002"
---
# <a name="idebugaddressgetaddress"></a>IDebugAddress::GetAddress
Bir nesne ve onun kapsamındaki veya kapsayıcı konumunu tanımlayan bir yapıyı döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetAddress (
   DEBUG_ADDRESS * pAddress
);
```

```csharp
int GetAddress(
   DEBUG_ADDRESS[] pAddress
);
```

## <a name="parameters"></a>Parametreler
`pAddress`\
[out içinde] A [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) bu yöntem tarafından girilir yapısının.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) yapısı, ilgili bilgileri ile oturum kaplayacak şekilde bu yönteme geçirilir. Bu bilgileri nasıl yorumlanacağını döndürülen bilgileri ve sembol işleyici türüne bağlıdır. Bkz: [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) daha fazla ayrıntı için.

## <a name="see-also"></a>Ayrıca bkz.
- [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)