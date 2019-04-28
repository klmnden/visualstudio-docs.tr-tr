---
title: Idiasession::findlinesbyva | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::findLinesByVA method
ms.assetid: f647eee9-a73c-483b-9fe9-21f42e560a7b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 29f3f714cdcbe529dac98948f6568934a6f508af
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62832412"
---
# <a name="idiasessionfindlinesbyva"></a>IDiaSession::findLinesByVA
Belirtilen sanal adres (VA) aralığında bulunan satırlar için satır numarası bilgisi alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT findLinesByVA (
    ULONGLONG             va,
    DWORD                 length,
    IDiaEnumLineNumbers** ppResult
);
```

#### <a name="parameters"></a>Parametreler
`va`

[in] Bir VA. adresini belirtir

`length`

[in] Bu sorguyu kapsayacak şekilde adres aralığını bayt sayısını belirtir.

`ppResult`

[out] Döndürür bir [Idiaenumlinenumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md) tüm satır listesini içeren nesne belirtilen adres aralığını kapsayan numaralandırır.

## <a name="example"></a>Örnek
Bu örnek, sanal işlevin adresi ve uzunluğu kullanarak bir işlev içinde yer alan tüm satır numaralarını alır bir işlev gösterir.

```C++
IDiaEnumLineNumbers *GetLineNumbersByVA(IDiaSymbol *pFunc, IDiaSession *pSession)
{
    IDiaEnumLineNumbers* pEnum = NULL;
    ULONGLONG            va;
    ULONGLONG            length;

    if (pFunc->get_virtualAddress ( &va ) == S_OK)
    {
        pFunc->get_length( &length );
        pSession->findLinesByVA( va, static_cast<DWORD>( length ), &pEnum );
    }
    return(pEnum);
}
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumLineNumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)
- [IDiaSession](../../debugger/debug-interface-access/idiasession.md)
