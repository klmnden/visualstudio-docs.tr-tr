---
title: Idiasession::findlinesbylinenum | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::findLinesByLinenum method
ms.assetid: 76d5622d-9a91-4c2a-a98f-263af5d1daef
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9d5999febf6e926ef8e9beb365728a3b150e1a38
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839273"
---
# <a name="idiasessionfindlinesbylinenum"></a>IDiaSession::findLinesByLinenum
Belirtilen satır numarası kaynak dosyada içinde ya da yakın bulunma derlenecek satır numaralarını belirler.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT findLinesByLinenum ( 
    IDiaSymbol*           compiland,
    IDiaSourceFile*       file,
    DWORD                 linenum,
    DWORD                 column,
    IDiaEnumLineNumbers** ppResult
);
```

#### <a name="parameters"></a>Parametreler
`compiland`

[in] Bir [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) için satır numaralarını aranacağı derlenecek temsil eden nesne. Bu parametre olamaz `NULL`.

`file`

[in] Bir [Idiasourcefile](../../debugger/debug-interface-access/idiasourcefile.md) içinde arama yapmak istediğiniz kaynak dosyasını temsil eden nesne. Bu parametre olamaz `NULL`.

`linenum`

[in] Bir tane tabanlı satır numarasını belirtir.

> [!NOTE]
> Tüm satırları belirtmek için sıfır kullanamazsınız (kullanın [Idiasession::findlines](../../debugger/debug-interface-access/idiasession-findlines.md) tüm satırları Bul yöntemi).

`column`

[in] Sütun sayısını belirtir. Sıfır tüm sütunları belirtmek için kullanın. Bir bayt uzaklığı içine satır bir sütundur.

`ppResult`

[out] Döndürür bir [Idiaenumlinenumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md) satır numaralarını listesini içeren objta alınır.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bir kaynak dosyasını açın, bu dosya tarafından katkıda bulunulan derleme listeleme ve her derlenecek başladığı kaynak dosyadaki satır numaralarını bulmak gösterilmektedir.

```C++
void ShowLinesInCompilands(IDiaSession *pSession, LPCOLESTR filename)
{
    IDiaEnumSourceFiles* pEnum;
    IDiaSourceFile*      pFile;
    DWORD                celt;

    pSession->findFile ( NULL, filename, nsFNameExt, &pEnum );
    while ( pEnum->Next ( 1, &pFile, &celt ) == S_OK ) // for each file
    {
        IDiaEnumSymbols* pEnumCompilands;
        IDiaSymbol* pCompiland;

        pFile->get_compilands ( &pEnumCompilands );
        // for each compiland
        while ( pEnumCompilands->Next ( 1, &pCompiland, &celt ) == S_OK )
        {
            IDiaEnumLineNumbers* pEnum;
            // Find first compiland closest to line 1 of the file.
            if (pSession->findLinesByLinenum( pCompiland, pFile, 1, 0, &pEnum ) == S_OK)
            {
                IDiaLineNumber *pLineNumber;
                DWORD lineCount;
                while ( pEnum->Next(1,&pLineNumber,&lineCount) == S_OK)
                {
                    DWORD lineNum;
                    if (pLineNumber->get_line(&lineNum) == S_OK)
                    {
                        printf("compiland starts in source at line number = %lu\n",lineNum);
                    }
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumLineNumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)
- [IDiaSession](../../debugger/debug-interface-access/idiasession.md)
- [IDiaSession::findLinesByAddr](../../debugger/debug-interface-access/idiasession-findlinesbyaddr.md)
- [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md)
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
