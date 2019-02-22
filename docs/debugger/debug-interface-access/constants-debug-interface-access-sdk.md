---
title: Sabitler (arabirim erişimi SDK'SINDA hata ayıklama) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- constants, DIA SDK
- DIA SDK, constants
ms.assetid: aca4ec77-bc08-4cdd-a6ce-8d4a28ea5ea3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ed505499efcabd7173fea9d668cd9afa5ed6d925
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56608584"
---
# <a name="constants-debug-interface-access-sdk"></a>Sabitler (Arabirim Erişimi SDK'sında Hata Ayıklama)
Bu dize sabitleri, program hata ayıklama veritabanı (PDB) dosyası DIA SDK'sı aracılığıyla çeşitli bölümlerini belirlemek için kullanılabilir.

## <a name="constants"></a>Sabitler
Aşağıdaki C/C++ makroları olarak bildirilir.

|Makrosu|Değer|
|-----------|-----------|
|`DiaTable_Symbols`|L "Simge"|
|`DiaTable_Sections`|L "Bölümler"|
|`DiaTable_SrcFiles`|L "Kaynakdosyalar"|
|`DiaTable_LineNums`|L "Lınenumbers"|
|`DiaTable_SegMap`|L"SegmentMap"|
|`DiaTable_Dbg`|L "Dbg"|
|`DiaTable_InjSrc`|L "InjectedSource"|
|`DiaTable_FrameData`|L "FrameData"|

## <a name="example"></a>Örnek
Şu simgelerden birini kullanarak bir örnek aşağıda verilmiştir:

```C++
HRESULT GetSymbolTable(IDiaEnumTables *pEnumTables, IDiaTable **pTable)
{
    HRESULT hr;
    VARIANT var;
    var.vt      = VT_BSTR;
    var.bstrVal = SysAllocString( DiaTable_Symbols );
    hr = pEnumTables->Item( var, pTable );
    return(hr);
}
```

## <a name="requirements"></a>Gereksinimler
Üstbilgi: dia2.h

## <a name="see-also"></a>Ayrıca Bkz.
- [Başvuru](../../debugger/debug-interface-access/debug-interface-access-sdk-reference.md)
- [Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [Arabirimler (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)
- [IDiaEnumTables::Item](../../debugger/debug-interface-access/idiaenumtables-item.md)
