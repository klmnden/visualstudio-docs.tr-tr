---
title: Idiaenumdebugstreamdata | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumDebugStreamData interface
ms.assetid: e2023c32-4c05-4d0c-a0be-f016a230c788
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e2865dbf3da103610407cd33eeeaf934caba3c7a
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56608623"
---
# <a name="idiaenumdebugstreamdata"></a>IDiaEnumDebugStreamData
Hata ayıklama veri akışı kayıtlara erişim sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDiaEnumDebugStreamData : IUnknown
```

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDiaEnumDebugStreamData`.

|Yöntem|Açıklama|
|------------|-----------------|
|[IDiaEnumDebugStreamData::get__NewEnum](../../debugger/debug-interface-access/idiaenumdebugstreamdata-get-newenum.md)|Alır [IEnumVARIANT arabirimi](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) bu Numaralandırıcının sürümü.|
|[IDiaEnumDebugStreamData::get_Count](../../debugger/debug-interface-access/idiaenumdebugstreamdata-get-count.md)|Hata ayıklama veri akışında kayıt sayısını alır.|
|[IDiaEnumDebugStreamData::get_name](../../debugger/debug-interface-access/idiaenumdebugstreamdata-get-name.md)|Hata ayıklama veri akışını adını alır.|
|[IDiaEnumDebugStreamData::Item](../../debugger/debug-interface-access/idiaenumdebugstreamdata-item.md)|Belirtilen kaydı alır.|
|[IDiaEnumDebugStreamData::Next](../../debugger/debug-interface-access/idiaenumdebugstreamdata-next.md)|Belirtilen kayıt sayısı numaralandırılmış dizisinden alır.|
|[IDiaEnumDebugStreamData::Skip](../../debugger/debug-interface-access/idiaenumdebugstreamdata-skip.md)|Kayıtları numaralandırılmış bir dizisinde belirtilen sayıda atlar.|
|[IDiaEnumDebugStreamData::Reset](../../debugger/debug-interface-access/idiaenumdebugstreamdata-reset.md)|Numaralandırılan sıralı başlangıç durumuna sıfırlar.|
|[IDiaEnumDebugStreamData::Clone](../../debugger/debug-interface-access/idiaenumdebugstreamdata-clone.md)|Geçerli Numaralandırıcı aynı numaralandırılmış dizi içeren bir numaralandırıcı oluşturur.|

## <a name="remarks"></a>Açıklamalar
Bu arabirim, hata ayıklama veri akışında kayıt akışını temsil eder. Boyutu ve her kaydı yorumu kaydı geldiği veri akışını bağımlı. Bu arabirim, etkili bir şekilde sembol dosyası ham veri baytları erişim sağlar.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
Çağrı [Idiaenumdebugstreams::Item](../../debugger/debug-interface-access/idiaenumdebugstreams-item.md) veya [Idiaenumdebugstreams::Next](../../debugger/debug-interface-access/idiaenumdebugstreams-next.md) edinmek için bir `IDiaEnumDebugStreamData` nesne.

## <a name="example"></a>Örnek
 Bu örnek, bir tek veri akışını ve kayıtlarını nasıl gösterir.

```C++
void PrintStreamData(IDiaEnumDebugStreamData* pStream)
{
    BSTR  wszName;
    LONG  dwElem;
    ULONG celt    = 0;
    DWORD cbData;
    DWORD cbTotal = 0;
    BYTE  data[1024];

    if(pStream->get_name(&wszName) != S_OK)
    {
        wprintf_s(L"ERROR - PrintStreamData() get_name\n");
    }
    else
    {
        wprintf_s(L"Stream: %s", wszName);
        SysFreeString(wszName);
    }
    if(pStream->get_Count(&dwElem) != S_OK)
    {
        wprintf(L"ERROR - PrintStreamData() get_Count\n");
    }
    else
    {
        wprintf(L"(%d)\n", dwElem);
    }
    while(pStream->Next(1, sizeof(data), &cbData, (BYTE *)&data, &celt) == S_OK)
    {
        DWORD i;
        for (i = 0; i < cbData; i++)
        {
            wprintf(L"%02X ", data[i]);
            if(i && i % 8 == 7 && i+1 < cbData)
            {
                wprintf(L"- ");
            }
        }
        wprintf(L"| ");
        for(i = 0; i < cbData; i++)
        {
            wprintf(L"%c", iswprint(data[i]) ? data[i] : '.');
        }
        wprintf(L"\n");
        cbTotal += cbData;
    }
    wprintf(L"Summary :\n\tSizeof(Elem) = %d\n\tNo of Elems = %d\n\n",
            cbTotal/dwElem, dwElem);
}
```

## <a name="requirements"></a>Gereksinimler
Üst bilgi: dia2.h

Kitaplık: diaguids.lib

DLL: msdia80.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Arabirimler (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)
- [IDiaEnumDebugStreams::Item](../../debugger/debug-interface-access/idiaenumdebugstreams-item.md)
- [IDiaEnumDebugStreams::Next](../../debugger/debug-interface-access/idiaenumdebugstreams-next.md)
