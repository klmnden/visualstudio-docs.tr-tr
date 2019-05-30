---
title: IDebugMethodField::EnumLocals | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugMethodField::EnumLocals
helpviewer_keywords:
- IDebugMethodField::EnumLocals method
ms.assetid: b0456a6d-2b96-49e2-a871-516571b4f6a5
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: bd4e2ffcaa66af58d3cc7ab57420de32d77eec92
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66346779"
---
# <a name="idebugmethodfieldenumlocals"></a>IDebugMethodField::EnumLocals
Yöntemin seçili yerel değişkenler için bir numaralandırıcı oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumLocals(
    IDebugAddress*     pAddress,
    IEnumDebugFields** ppLocals
);
```

```csharp
int EnumLocals(
    IDebugAddress        pAddress,
    out IEnumDebugFields ppLocals
);
```

## <a name="parameters"></a>Parametreler
`pAddress`\
[in] Bir [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) bağlamı veya kapsam Yereller alınmaya başlanacağı seçer hata ayıklama adresini temsil eden nesne.

`ppLocals`\
[out] Döndürür bir [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) hiçbir yerel öğeler varsa, aksi durumda null değer döndürür; yerel öğeler listesini temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
Başarılıysa S_OK döndürür veya hiçbir yerel öğeler varsa S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
Yalnızca belirli hata ayıklama adresi içeren bir blok içinde tanımlanan değişkenler numaralandırılır. Tüm derleyici tarafından oluşturulan yerel öğeler de dahil olmak üzere tüm Yereller gerekirse, çağrı [EnumAllLocals](../../../extensibility/debugger/reference/idebugmethodfield-enumalllocals.md) yöntemi.

Bir yöntem, birden çok kapsam belirleme bağlamları veya blok içerebilir. Örneğin, üç kapsamlar, iki iç blokları ve yöntem gövdesi aşağıdaki contrived yöntemi içerir.

```csharp
public void func(int index)
{
    // Method body scope
    int a = 0;
    if (index == 1)
    {
        // Inner scope 1
        int temp1 = a;
    }
    else
    {
        // Inner scope 2
        int temp2 = a;
    }
}
```

[IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md) nesnesini temsil `func` yöntemi. Çağırma `EnumLocals` yöntemi ile bir [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) kümesine `Inner Scope 1` adresini döndürür içeren bir sabit listesi `temp1` örneğin değişken.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)
- [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)
- [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)
- [EnumAllLocals](../../../extensibility/debugger/reference/idebugmethodfield-enumalllocals.md)
