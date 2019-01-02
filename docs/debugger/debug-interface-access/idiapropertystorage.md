---
title: Idiapropertystorage | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage interface
ms.assetid: d3197a38-5973-4e56-873e-4f1b84c3f674
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 8b896cf54f06e84316f67a32c10f66dda21c2cd9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53910733"
---
# <a name="idiapropertystorage"></a>IDiaPropertyStorage
DIA özellik kümesi kalıcı özelliklerini okumanıza izin verir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDiaPropertyStorage : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDiaPropertyStorage`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDiaPropertyStorage::Enum](../../debugger/debug-interface-access/idiapropertystorage-enum.md)|Bir işaretçi özellikleri bu kümesi içinde numaralandırıcıyı alır.|  
|[IDiaPropertyStorage::ReadBOOL](../../debugger/debug-interface-access/idiapropertystorage-readbool.md)|Okur `BOOL` değerlerde özellik kümesi.|  
|[IDiaPropertyStorage::ReadBSTR](../../debugger/debug-interface-access/idiapropertystorage-readbstr.md)|Okur `BSTR` değerlerde özellik kümesi.|  
|[IDiaPropertyStorage::ReadDWORD](../../debugger/debug-interface-access/idiapropertystorage-readdword.md)|Okur `DWORD` değerlerde özellik kümesi.|  
|[IDiaPropertyStorage::ReadLONG](../../debugger/debug-interface-access/idiapropertystorage-readlong.md)|Okur `LONG` değerlerde özellik kümesi.|  
|[IDiaPropertyStorage::ReadMultiple](../../debugger/debug-interface-access/idiapropertystorage-readmultiple.md)|Bir özellik kümesi özellik değerlerini okur.|  
|[IDiaPropertyStorage::ReadPropertyNames](../../debugger/debug-interface-access/idiapropertystorage-readpropertynames.md)|Dize adları için karşılık gelen alır, özellik tanımlayıcıları verilir.|  
|[IDiaPropertyStorage::ReadULONGLONG](../../debugger/debug-interface-access/idiapropertystorage-readulonglong.md)|Okur `ULONGLONG` değerlerde özellik kümesi.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir özellik kümesi içindeki her bir özellik bir özellik tanımlayıcısı (ID), dört baytlık tanımlanır `ULONG` küme için benzersiz bir değer. Aracılığıyla kullanıma sunulan özellikleri `IDiaPropertyStorage` arabirimi üst arabiriminde özellikleri karşılık gelir. Örneğin, özelliklerini [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) arabirimi adıyla erişilebilir `IDiaPropertyStorage` arabirimi (ancak özelliği erişilebilir olsa da, bu özelliği için geçerli gelmez olduğunu unutmayın bir belirli `IDiaSymbol` nesne).  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirim çağırarak elde `QueryInterface` başka bir arabirimdeki yöntem. İçin aşağıdaki arabirimlerinden sorgulanabilir `IDiaPropertyStorage` arabirimi:  
  
-   [IDiaSectionContrib](../../debugger/debug-interface-access/idiasectioncontrib.md)  
  
-   [IDiaSegment](../../debugger/debug-interface-access/idiasegment.md)  
  
-   [IDiaInjectedSource](../../debugger/debug-interface-access/idiainjectedsource.md)  
  
-   [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)  
  
-   [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)  
  
-   [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md)  
  
-   [IDiaLineNumber](../../debugger/debug-interface-access/idialinenumber.md)  
  
## <a name="example"></a>Örnek  
 Bu örnek tarafından kullanıma sunulan tüm özellikleri görüntüleyen bir işlev göstermektedir `IDiaPropertyStorage` nesne. Bkz: [Idiaenumınjectedsources](../../debugger/debug-interface-access/idiaenuminjectedsources.md) örneği nasıl arabirimi `IDiaPropertyStorage` arabirimi öğesinden alınan [Idiaınjectedsource](../../debugger/debug-interface-access/idiainjectedsource.md) arabirimi.  
  
```C++  
void PrintPropertyStorage(IDiaPropertyStorage* pPropertyStorage)  
{  
    IEnumSTATPROPSTG* pEnumProps;  
    STATPROPSTG       prop;  
    DWORD             celt = 1;  
  
    if (pPropertyStorage->Enum(&pEnumProps) == S_OK)  
    {  
        while (pEnumProps->Next(celt, &prop, &celt) == S_OK)  
        {  
            PROPSPEC pspec = { PRSPEC_PROPID, prop.propid };  
            PROPVARIANT vt = { VT_EMPTY };  
  
            if (pPropertyStorage->ReadMultiple( 1, &pspec, &vt) == S_OK)  
            {  
                switch( vt.vt ){  
                    case VT_BOOL:  
                        wprintf( L"%32s:\t %s\n", prop.lpwstrName, vt.bVal ? L"true" : L"false" );  
                        break;  
                    case VT_I2:  
                        wprintf( L"%32s:\t %d\n", prop.lpwstrName, vt.iVal );  
                        break;  
                    case VT_UI2:  
                        wprintf( L"%32s:\t %d\n", prop.lpwstrName, vt.uiVal );  
                        break;  
                    case VT_I4:  
                        wprintf( L"%32s:\t %d\n", prop.lpwstrName, vt.intVal );  
                        break;  
                    case VT_UI4:  
                        wprintf( L"%32s:\t 0x%0x\n", prop.lpwstrName, vt.uintVal );  
                        break;  
                    case VT_UI8:  
                        wprintf( L"%32s:\t 0x%x\n", prop.lpwstrName, vt.uhVal.QuadPart );  
                        break;  
                    case VT_BSTR:  
                        wprintf( L"%32s:\t %s\n", prop.lpwstrName, vt.bstrVal );  
                        break;  
                    case VT_UNKNOWN:  
                        wprintf( L"%32s:\t %p\n", prop.lpwstrName, vt.punkVal );  
                        break;  
                    case VT_SAFEARRAY:  
                        break;  
                    default:  
                       break;  
                }  
                VariantClear((VARIANTARG*) &vt);  
            }  
        }  
        pEnumProps->Release();  
    }  
}  
```  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: dia2.h  
  
 Kitaplık: diaguids.lib  
  
 DLL: msdia80.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Arabirimler (arabirim erişimi SDK'SINDA hata ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [Idiasession::getenumtables](../../debugger/debug-interface-access/idiasession-getenumtables.md)   
 [Idiasectioncontrib](../../debugger/debug-interface-access/idiasectioncontrib.md)   
 [Idiasegment](../../debugger/debug-interface-access/idiasegment.md)   
 [Idiaınjectedsource](../../debugger/debug-interface-access/idiainjectedsource.md)   
 [Idiaframedata](../../debugger/debug-interface-access/idiaframedata.md)   
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [Idiasourcefile](../../debugger/debug-interface-access/idiasourcefile.md)   
 [Idialinenumber](../../debugger/debug-interface-access/idialinenumber.md)   
 [IDiaEnumInjectedSources](../../debugger/debug-interface-access/idiaenuminjectedsources.md)