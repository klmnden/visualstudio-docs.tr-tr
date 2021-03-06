---
title: Idiaenumframedata | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumFrameData interface
ms.assetid: 2ca7fd5a-b2fa-4b3a-9492-0263eafc435b
caps.latest.revision: 16
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 3b3e2436d4b4eed6ac86591821090c89a538e06b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68190787"
---
# <a name="idiaenumframedata"></a>IDiaEnumFrameData
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Veri kaynağında bulunan çeşitli çerçeve veri öğeleri sıralar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDiaEnumFrameData : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDiaEnumFrameData`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDiaEnumFrameData::get__NewEnum](../../debugger/debug-interface-access/idiaenumframedata-get-newenum.md)|Alır `IEnumVARIANT Interface` bu Numaralandırıcının sürümü.|  
|[IDiaEnumFrameData::get_Count](../../debugger/debug-interface-access/idiaenumframedata-get-count.md)|Çerçeve veri öğe sayısını alır.|  
|[IDiaEnumFrameData::Item](../../debugger/debug-interface-access/idiaenumframedata-item.md)|Bir dizini yoluyla bir çerçeve veri öğesi alır.|  
|[IDiaEnumFrameData::Next](../../debugger/debug-interface-access/idiaenumframedata-next.md)|Belirtilen sayıda sabit listesi sırası çerçeve veri öğelerini alır.|  
|[IDiaEnumFrameData::Skip](../../debugger/debug-interface-access/idiaenumframedata-skip.md)|Belirtilen sayıda bir numaralandırma sıralı çerçeve veri öğeleri atlar.|  
|[IDiaEnumFrameData::Reset](../../debugger/debug-interface-access/idiaenumframedata-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|  
|[IDiaEnumFrameData::Clone](../../debugger/debug-interface-access/idiaenumframedata-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|  
|[IDiaEnumFrameData::frameByRVA](../../debugger/debug-interface-access/idiaenumframedata-framebyrva.md)|Bir çerçeve göreli sanal adres (RVA) göre döndürür.|  
|[IDiaEnumFrameData::frameByVA](../../debugger/debug-interface-access/idiaenumframedata-framebyva.md)|Bir çerçeve sanal adres (VA) döndürür.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirimden elde [Idiasession::getenumtables](../../debugger/debug-interface-access/idiasession-getenumtables.md) yöntemi. Ayrıntılar için örneğe bakın.  
  
## <a name="example"></a>Örnek  
 Bu örnek nasıl alınacağını gösterir ( `GetEnumFrameData` işlevi) ve ( `ShowFrameData` işlevi) `IDiaEnumFrameData` arabirimi. Bkz: [Idiaframedata](../../debugger/debug-interface-access/idiaframedata.md) arabirimi ilişkin bir örnek `PrintFrameData` işlevi.  
  
```cpp#  
  
      IDiaEnumFrameData* GetEnumFrameData(IDiaSession *pSession)  
{  
    IDiaEnumFrameData* pUnknown    = NULL;  
    REFIID             iid         = __uuidof(IDiaEnumFrameData);  
    IDiaEnumTables*    pEnumTables = NULL;  
    IDiaTable*         pTable      = NULL;  
    ULONG              celt        = 0;  
  
    if (pSession->getEnumTables(&pEnumTables) != S_OK)  
    {  
        wprintf(L"ERROR - GetTable() getEnumTables\n");  
        return NULL;  
    }  
    while (pEnumTables->Next(1, &pTable, &celt) == S_OK && celt == 1)  
    {  
        // There is only one table that matches the given iid  
        HRESULT hr = pTable->QueryInterface(iid, (void**)&pUnknown);  
        pTable->Release();  
        if (hr == S_OK)  
        {  
            break;  
        }  
    }  
    pEnumTables->Release();  
    return pUnknown;  
}  
  
void ShowFrameData(IDiaSession *pSession)  
{  
    IDiaEnumFrameData* pEnumFrameData = GetEnumFrameData(pSession);;  
  
    if (pEnumFrameData != NULL)  
    {  
        IDiaFrameData* pFrameData;  
        ULONG celt = 0;  
  
        while(pEnumFrameData->Next(1, &pFrameData, &celt) == S_OK &&  
              celt == 1)  
        {  
            PrintFrameData(pFrameData);  
            pFrameData->Release();  
        }  
        pEnumFrameData->Release();   
    }  
}  
```  
  
## <a name="requirements"></a>Gereksinimler  
 **Üst bilgi:** dia2.h  
  
 **Kitaplığı:** diaguids.lib  
  
 **DLL:** msdia80.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Arabirimler (arabirim erişimi SDK'SINDA hata ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [Idiasession::getenumtables](../../debugger/debug-interface-access/idiasession-getenumtables.md)   
 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)
