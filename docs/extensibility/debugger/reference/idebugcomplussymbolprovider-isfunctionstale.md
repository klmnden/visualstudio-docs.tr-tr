---
title: IDebugComPlusSymbolProvider::IsFunctionStale | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugComPlusSymbolProvider::IsFunctionStale
ms.assetid: dcffc090-4ed8-47b2-ba51-bce1a6b6428d
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 121782e7febeb93844689c140d1994a68e3903b4
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351801"
---
# <a name="idebugcomplussymbolproviderisfunctionstale"></a>IDebugComPlusSymbolProvider::IsFunctionStale
Belirtilen hata ayıklama adresten işlevi eski olarak kabul edileceğini belirler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT IsFunctionStale(
    IDebugAddress* pAddress
);
```

```csharp
int IsFunctionStale(
    IDebugAddress pAddress
);
```

## <a name="parameters"></a>Parametreler
`pAddress`\
[in] Tarafından temsil edilen hata ayıklama adresi bir [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi. Bu adresi bir METHOD_ADDRESS olmalıdır.

## <a name="return-value"></a>Dönüş Değeri
İşlev eski kabul ediliyorsa döndürür `S_OK`. İşlev eski değilse döndürür `S_FALSE`.

## <a name="example"></a>Örnek
Aşağıdaki örnek için bu yöntemi uygulaması gösterilmiştir bir **CDebugSymbolProvider** gösteren nesne [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md) arabirimi.

```cpp
HRESULT CDebugSymbolProvider::IsFunctionStale(
    IDebugAddress* pAddress
)
{
    HRESULT hr = S_OK;
    CDEBUG_ADDRESS address;
    CComPtr<CModule> pModule;

    ASSERT(IsValidObjectPtr(this, CDebugSymbolProvider));
    ASSERT(IsValidInterfacePtr(pAddress, IDebugAddress));

    METHOD_ENTRY( CDebugSymbolProvider::IsFunctionStale );

    IfFalseGo( pAddress, S_FALSE );
    IfFailGo( pAddress->GetAddress( &address ) );

    ASSERT(address.addr.dwKind == ADDRESS_KIND_METADATA_METHOD);
    IfFalseGo( address.addr.dwKind == ADDRESS_KIND_METADATA_METHOD, S_FALSE );

    IfFailGo( GetModule( address.GetModule(), &pModule) );

    if (!pModule->IsFunctionStale( address.addr.addr.addrMethod.tokMethod,
                                   address.addr.addr.addrMethod.dwVersion ))
    {

        // S_FALSE indicates the function is not stale

        hr = S_FALSE;
    }

Error:

    METHOD_EXIT( CDebugSymbolProvider::IsFunctionStale, hr );

    if (!SUCCEEDED(hr))
    {
        hr = S_FALSE;
    }

    return hr;
}
```

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md)
