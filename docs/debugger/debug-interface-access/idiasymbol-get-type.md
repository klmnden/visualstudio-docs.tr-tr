---
title: Idiasymbol::get_type | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_type method
ms.assetid: 1c6a4176-dd4e-4c22-8b8f-0e559fc078ba
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4fa57b1f289f9cc5e8c57c08b6d51bb1677c3db4
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "62835378"
---
# <a name="idiasymbolgettype"></a>IDiaSymbol::get_type
Bu simgenin türünü temsil eden simgeyi alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_type (
    IDiaSymbol** pRetVal
);
```

#### <a name="parameters"></a>Parametreler
`pRetVal`

[out] Döndürür bir [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) bu simgenin türünü temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.

## <a name="remarks"></a>Açıklamalar
Bir simge olan türü belirlemek için bu yöntemi çağırın ve ortaya çıkan inceleyin [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) nesne. Bir simge türü almamayı mümkün olduğunu unutmayın. Örneğin, bir yapının adını tür yok ancak alt simge olabilir (kullanın [Idiasymbol::findchildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md) alt incelemek için yöntemi).

## <a name="example"></a>Örnek

```C++
IDiaSymbol*         pType;
CComPtr<IDiaSymbol> pBaseType;
if (SUCCEEDED(pType->get_type( &pBaseType ))) {
    BasicType btBaseType;
    if (SUCCEEDED(pBaseType->get_baseType((DWORD *)&btBaseType))) {
        // Do something with basic type.
    }
}
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [IDiaSymbol::get_baseType](../../debugger/debug-interface-access/idiasymbol-get-basetype.md)
- [IDiaSymbol::findChildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md)
