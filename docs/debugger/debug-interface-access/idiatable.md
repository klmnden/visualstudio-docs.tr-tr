---
title: Idiatable | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaTable interface
ms.assetid: c99a2c44-7b72-4e3c-b963-25fe3df3a555
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 604c68ef82f66358238f94b43f000fae24a076f1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62834158"
---
# <a name="idiatable"></a>IDiaTable
DIA veri kaynağı tablosu numaralandırır.

## <a name="syntax"></a>Sözdizimi

```
IDiaTable : IEnumUnknown
```

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDiaTable`.

|Yöntem|Açıklama|
|------------|-----------------|
|[IDiaTable::get__NewEnum](../../debugger/debug-interface-access/idiatable-get-newenum.md)|Alır [IEnumVARIANT arabirimi](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) bu Numaralandırıcının sürümü.|
|[IDiaTable::get_name](../../debugger/debug-interface-access/idiatable-get-name.md)|Tablonun adını alır.|
|[IDiaTable::get_Count](../../debugger/debug-interface-access/idiatable-get-count.md)|Tablodaki öğe sayısını alır.|
|[IDiaTable::Item](../../debugger/debug-interface-access/idiatable-item.md)|Belirli bir giriş dizini bir başvuru alır.|

## <a name="remarks"></a>Açıklamalar
Bu arabirimi uygulayan `IEnumUnknown` Microsoft.VisualStudio.OLE.Interop ad alanında numaralandırma yöntemlerini. `IEnumUnknown` Numaralandırma arabirimidir İçindekiler üzerinde yineleme için çok daha verimli [Idiatable::get_Count](../../debugger/debug-interface-access/idiatable-get-count.md) ve [Idiatable::Item](../../debugger/debug-interface-access/idiatable-item.md) yöntemleri.

Yorumu `IUnknown` arabirimi öğesinden döndürülen `IDiaTable::Item` yöntemi veya `Next` yöntemi (Microsoft.VisualStudio.OLE.Interop uzayında) tablo türüne bağlıdır. Örneğin, varsa `IDiaTable` arabirimi temsil eder, eklenen kaynakları listesini `IUnknown` arabirimi için sorgulanabilir [Idiaınjectedsource](../../debugger/debug-interface-access/idiainjectedsource.md) arabirimi.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
Bu arabirim çağırarak elde [Idiaenumtables::Item](../../debugger/debug-interface-access/idiaenumtables-item.md) veya [Idiaenumtables::Next](../../debugger/debug-interface-access/idiaenumtables-next.md) yöntemleri.

Aşağıdaki arabirimlerinden ile uygulanan `IDiaTable` arabirimi (diğer bir deyişle, sorgu `IDiaTable` arabirimi için aşağıdaki arabirimlerinden birini):

- [IDiaEnumSymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)

- [IDiaEnumSourceFiles](../../debugger/debug-interface-access/idiaenumsourcefiles.md)

- [IDiaEnumLineNumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)

- [IDiaEnumSectionContribs](../../debugger/debug-interface-access/idiaenumsectioncontribs.md)

- [IDiaEnumSegments](../../debugger/debug-interface-access/idiaenumsegments.md)

- [IDiaEnumInjectedSources](../../debugger/debug-interface-access/idiaenuminjectedsources.md)

- [IDiaEnumFrameData](../../debugger/debug-interface-access/idiaenumframedata.md)

## <a name="example"></a>Örnek
İlk işlev `ShowTableNames`, oturumda tüm tabloların adlarını görüntüler. İkinci işlevi `GetTable`, tüm tabloları, belirtilen arabirimi uygulayan bir tablo için arar. Üçüncü işlev `UseTable`, nasıl kullanılacağını gösterir `GetTable` işlevi.

> [!NOTE]
> `CDiaBSTR` sarmalayan bir sınıf bir `BSTR` ve dize örnekleme kapsam dışına çıktığında boşaltma otomatik olarak işler.

```C++
void ShowTableNames(IDiaSession *pSession)
{
    CComPtr<IDiaEnumTables> pTables;
    if ( FAILED( psession->getEnumTables( &pTables ) ) )
    {
        Fatal( "getEnumTables" );
    }
    CComPtr< IDiaTable > pTable;
    while ( SUCCEEDED( hr = pTables->Next( 1, &pTable, &celt ) )
            && celt == 1 )
    {
        CDiaBSTR bstrTableName;
        if ( pTable->get_name( &bstrTableName ) != 0 )
        {
            Fatal( "get_name" );
        }
        printf( "Found table: %ws\n", bstrTableName );
    }

// Searches the list of all tables for a table that supports
// the specified interface.  Use this function to obtain an
// enumeration interface.
HRESULT GetTable(IDiaSession* pSession,
                 REFIID       iid,
                 void**       ppUnk)
{
    CComPtr<IDiaEnumTables> pEnumTables;
    HRESULT hResult;

    if (FAILED(pSession->getEnumTables(&pEnumTables)))
        Fatal("getEnumTables");

    CComPtr<IDiaTable> pTable;
    ULONG celt = 0;
    while (SUCCEEDED(hResult = pEnumTables->Next(1, &pTable, &celt)) &&
           celt == 1)
    {
        if (pTable->QueryInterface(iid, (void**)ppUnk) == S_OK)
        {
            return S_OK;
        }
        pTable = NULL;
    }

    if (FAILED(hResult))
        Fatal("EnumTables->Next");

    return E_FAIL;
}

// This function shows how to use the GetTable function.
void UseTable(IDiaSession *pSession)
{
    CComPtr<IDiaEnumSegments> pEnumSegments;
    if (SUCCEEDED(GetTable(pSession, __uuidof(IDiaEnumSegments), &pEnumSegments)))
    {
        // Do something with pEnumSegments.
    }
}
```

## <a name="requirements"></a>Gereksinimler
Üst bilgi: dia2.h

Kitaplık: diaguids.lib

DLL: msdia80.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Arabirimler (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)
- [IDiaEnumTables](../../debugger/debug-interface-access/idiaenumtables.md)
- [IDiaEnumTables::Item](../../debugger/debug-interface-access/idiaenumtables-item.md)
- [IDiaEnumTables::Next](../../debugger/debug-interface-access/idiaenumtables-next.md)
