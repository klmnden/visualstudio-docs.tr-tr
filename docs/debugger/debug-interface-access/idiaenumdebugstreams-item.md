---
title: Idiaenumdebugstreams::Item | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumDebugStreams::Item method
ms.assetid: 6b388fe1-eabc-4720-9d59-dc09b0ceaeac
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5df6e50185bf04dd1f4dbb9f1016a1d6b73b1185
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56318283"
---
# <a name="idiaenumdebugstreamsitem"></a>IDiaEnumDebugStreams::Item
Bir dizin veya ad ile bir hata ayıklama akışı alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Item (
    VARIANT                   index,
    IDiaEnumDebugStreamData** stream
);
```

#### <a name="parameters"></a>Parametreler
dizin  
[in] Dizin veya hata ayıklama akışının adı alınamıyor. Bir tamsayı değişken kullandıysanız, aralığı 0 olmalıdır `count`-1, burada `count` tarafından döndürülen [Idiaenumdebugstreams::get_Count](../../debugger/debug-interface-access/idiaenumdebugstreams-get-count.md) yöntemi.

akış  
[out] Döndürür bir [Idiaenumdebugstreamdata](../../debugger/debug-interface-access/idiaenumdebugstreamdata.md) belirtilen hata ayıklama akışını temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="example"></a>Örnek

```C++
IDiaEnumDebugStreamData *GetStreamData(IDiaEnumDebugStreams *pStreamList,
                                       LONG whichStream)
{
    IDiaEnumDebugStreamData *pStreamData = NULL;
    if (pStreamList != NULL)
    {
        LONG numStreams = 0;
        if (pStreamList->get_count(&numStreams) == S_OK &&
            whichStream >= 0 && whichStream < numStreams)
        {
            VARIANT vIndex;
            vIndex.vt   = VT_I4;
            vIndex.lVal = whichStream;
            if (pStreamList->Item(vIndex,&pStreamData) != S_OK)
            {
                std::cerr << "Error retrieving stream " << whichStream << std::endl;
            }
        }
    }
    return(pStreamData);
}
```

## <a name="see-also"></a>Ayrıca Bkz.
[IDiaEnumDebugStreamData](../../debugger/debug-interface-access/idiaenumdebugstreamdata.md)  
[IDiaEnumDebugStreams](../../debugger/debug-interface-access/idiaenumdebugstreams.md)
