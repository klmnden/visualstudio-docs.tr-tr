---
title: IDebugSettingsCallback2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugSettingsCallback2 interface
ms.assetid: 7e525d0b-7d7a-4d1c-8b78-e1398fa922f2
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 859522ebdbe231146c73b25c5e4c92fba9809727
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66321949"
---
# <a name="idebugsettingscallback2"></a>IDebugSettingsCallback2
Hata ayıklama altyapıları Ölçüm ayarlarını okumak üzere etkinleştirir uzaktan.

## <a name="syntax"></a>Sözdizimi

```
IDebugSettingsCallback2D : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
Bu arabirim oturum hata ayıklama Yöneticisi olay geri çağırma tarafından uygulanan ve hata ayıklama motoru tarafından kullanılan. Bu da yerel olarak Dbgmetric [d] .lib yerine kullanılabilir.

## <a name="methods"></a>Yöntemler
Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugSettingsCallback2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[EnumEEs](../../../extensibility/debugger/reference/idebugsettingscallback2-enumees.md)|Dil ve satıcı tanımlayıcıları verilen kullanılabilir ifade değerlendiricilerini numaralandırır.|
|[GetEELocalObject](../../../extensibility/debugger/reference/idebugsettingscallback2-geteelocalobject.md)|Ölçüm verilen bir ifade değerlendirici yerel bir nesne alır.|
|[GetEEMetricDword](../../../extensibility/debugger/reference/idebugsettingscallback2-geteemetricdword.md)|İfade değerlendirici belirtilen ölçüm için karşılık gelen bir değer alır.|
|[GetEEMetricFile](../../../extensibility/debugger/reference/idebugsettingscallback2-geteemetricfile.md)|Ad veya ölçüm verilen ifade değerlendirici ölçüm dosya alır.|
|[GetEEMetricGuid](../../../extensibility/debugger/reference/idebugsettingscallback2-geteemetricguid.md)|Bir ifade değerlendirici ölçüm adı verilen benzersiz tanımlayıcısını alır.|
|[GetEEMetricString](../../../extensibility/debugger/reference/idebugsettingscallback2-geteemetricstring.md)|Bir ifade değerlendirici ölçüm adı verilen değer dizesi alır.|
|[GetMetricDword](../../../extensibility/debugger/reference/idebugsettingscallback2-getmetricdword.md)|Adı verilen bir ölçüm değerini alır.|
|[GetMetricGuid](../../../extensibility/debugger/reference/idebugsettingscallback2-getmetricguid.md)|Bir ölçüm adı verilen benzersiz tanımlayıcısını alır.|
|[GetMetricString](../../../extensibility/debugger/reference/idebugsettingscallback2-getmetricstring.md)|Ölçüm adı verilen değer dizesi alır.|

## <a name="requirements"></a>Gereksinimler
Üst bilgi: Msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="example"></a>Örnek
Aşağıdaki örnek, alan bir işlev gösterir. bir **IDebugSettingsCallback2** bir parametre olarak nesne.

```cpp
HRESULT GetDebugSettingsCallback (IDebugSettingsCallback2 **ppCallback)
{
    HRESULT hRes = E_FAIL;

    if ( ppCallback )
    {
        if ( EVAL(m_pdec) )
            hRes = m_pdec->QueryInterface(IID_IDebugSettingsCallback2, (void **)ppCallback);
        else
            hRes = E_FAIL;
    }
    else
        hRes = E_INVALIDARG;

    return ( hRes );
}
```
