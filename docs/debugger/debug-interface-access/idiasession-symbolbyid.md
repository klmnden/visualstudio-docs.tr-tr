---
title: Idiasession::symbolbyıd | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::symbolById method
ms.assetid: 062e4b5a-9c4d-4703-88da-ec13102c2b66
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9b58fcf55741975a776e222b2845ae50774e7fc9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62832921"
---
# <a name="idiasessionsymbolbyid"></a>IDiaSession::symbolById
Bir sembol benzersiz kimliğine göre alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT symbolById (
    DWORD        id,
    IDiaSymbol** ppSymbol
);
```

#### <a name="parameters"></a>Parametreler
`id`

[in] Benzersiz tanımlayıcısı.

`ppSymbol`

[out] Döndürür bir [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) sembol temsil eden bir nesne alındı.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
Belirtilen tanımlayıcı, dahili olarak tüm sembolleri benzersiz olacak şekilde DIA SDK'sı tarafından kullanılan benzersiz bir değerdir.

Bu yöntem, örneğin, başka bir simge türünü gösteren simgenin almak için kullanılabilir (örneğe bakın).

## <a name="example"></a>Örnek
Bu örnek alır bir [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) temsil eden başka bir simge türü. Bu örnek nasıl kullanılacağını gösterir `symbolById` oturumdaki yöntemi. Basit bir yaklaşım çağırmaktır [Idiasymbol::get_type](../../debugger/debug-interface-access/idiasymbol-get-type.md) tür simgesi doğrudan almak için yöntemi.

```C++
IDiaSymbol *GetSymbolType(IDiaSymbol *pSymbol, IDiaSession *pSession)
{
    IDiaSymbol *pTypeSymbol = NULL;
    if (pSymbol != NULL && pSession != NULL)
    {
        DWORD symbolTypeId;
        pSymbol->get_typeId(&symbolTypeId);
        pSession->symbolById(symbolTypeId, &pTypeSymbol);
    }
    return(pTypeSymbol);
}
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSession](../../debugger/debug-interface-access/idiasession.md)
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [IDiaSymbol::get_type](../../debugger/debug-interface-access/idiasymbol-get-type.md)
