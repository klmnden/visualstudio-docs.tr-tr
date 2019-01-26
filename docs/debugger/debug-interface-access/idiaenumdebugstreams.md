---
title: Idiaenumdebugstreams | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumDebugStreams interface
ms.assetid: 611caf4f-7a5f-4aa4-b909-52feeb3cc752
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3bc7895248e8ba201debf4d5020de9cef6b0a836
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55014633"
---
# <a name="idiaenumdebugstreams"></a>IDiaEnumDebugStreams
Veri kaynağında bulunan çeşitli hata ayıklama akışları numaralandırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDiaEnumDebugStreams : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDiaEnumDebugStreams`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDiaEnumDebugStreams::get__NewEnum](../../debugger/debug-interface-access/idiaenumdebugstreams-get-newenum.md)|Alır `IEnumVARIANT` bu Numaralandırıcının sürümü.|  
|[IDiaEnumDebugStreams::get_Count](../../debugger/debug-interface-access/idiaenumdebugstreams-get-count.md)|Hata ayıklama akış sayısını alır.|  
|[IDiaEnumDebugStreams::Item](../../debugger/debug-interface-access/idiaenumdebugstreams-item.md)|Hata ayıklama akışı yoluyla dizin alır.|  
|[IDiaEnumDebugStreams::Next](../../debugger/debug-interface-access/idiaenumdebugstreams-next.md)|Belirtilen bir sabit listesi sırası hata ayıklama akış sayısını alır.|  
|[IDiaEnumDebugStreams::Skip](../../debugger/debug-interface-access/idiaenumdebugstreams-skip.md)|Hata ayıklama akışları bir numaralandırma dizisinde belirtilen sayıda atlar.|  
|[IDiaEnumDebugStreams::Reset](../../debugger/debug-interface-access/idiaenumdebugstreams-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|  
|[IDiaEnumDebugStreams::Clone](../../debugger/debug-interface-access/idiaenumdebugstreams-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|  
  
## <a name="remarks"></a>Açıklamalar  
 Hata ayıklama akış içeriğini uygulamaya bağlıdır ve veri biçimleri belgelenmemiş.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Çağrı [Idiasession::getenumdebugstreams](../../debugger/debug-interface-access/idiasession-getenumdebugstreams.md) elde etmek için yöntemi bir `IDiaEnumDebugStreams` nesne.  
  
## <a name="example"></a>Örnek  
 Bu örnek, kullanılabilir veri akışlarını bu arabirimden nasıl gösterir. Bkz: [Idiaenumdebugstreamdata](../../debugger/debug-interface-access/idiaenumdebugstreamdata.md) arabirimi uygulaması için `PrintStreamData` işlevi.  
  
```C++  
void DumpAllDebugStreams( IDiaSession* pSession)  
{  
    IDiaEnumDebugStreams* pEnumStreams;  
  
    wprintf(L"\n\n*** DEBUG STREAMS\n\n");  
    // Retrieve an enumerated sequence of debug data streams  
    if(pSession->getEnumDebugStreams(&pEnumStreams) == S_OK)  
    {  
        IDiaEnumDebugStreamData* pStream;  
        ULONG celt = 0;  
  
        for(; pEnumStreams->Next(1, &pStream, &celt) == S_OK; pStream = NULL)  
        {  
            PrintStreamData(pStream);  
            pStream->Release();  
        }  
        pEnumStreams->Release();  
    }  
    else  
    {  
      wprintf(L"Failed to get any debug streams!\n");  
    }  
    wprintf(L"\n");  
}  
```  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: dia2.h  
  
 Kitaplık: diaguids.lib  
  
 DLL: msdia80.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Arabirimler (arabirim erişimi SDK'SINDA hata ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [Idiaenumdebugstreamdata](../../debugger/debug-interface-access/idiaenumdebugstreamdata.md)   
 [IDiaSession::getEnumDebugStreams](../../debugger/debug-interface-access/idiasession-getenumdebugstreams.md)