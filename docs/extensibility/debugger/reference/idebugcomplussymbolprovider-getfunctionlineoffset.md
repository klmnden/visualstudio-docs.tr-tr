---
title: IDebugComPlusSymbolProvider::GetFunctionLineOffset | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugComPlusSymbolProvider::GetFunctionLineOffset
- GetFunctionLineOffset
ms.assetid: 51460f5a-4e98-427a-8315-27246e24fb61
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6ff64676ba99f16941044f18c8988a690bfc8a28
ms.sourcegitcommit: 7153e2fc717d32e0e9c8a9b8c406dc4053c9fd53
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "56412987"
---
# <a name="idebugcomplussymbolprovidergetfunctionlineoffset"></a>IDebugComPlusSymbolProvider::GetFunctionLineOffset
Belirtilen satır sapması temsil eden bir işlev içinde adresi alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetFunctionLineOffset(
    IDebugAddress*  pAddress,
    DWORD           dwLine,
    IDebugAddress** ppNewAddress
);
```

```csharp
int GetFunctionLineOffset(
    IDebugAddress     pAddress,
    uint              dwLine,
    out IDebugAddress ppNewAddress
);
```

#### <a name="parameters"></a>Parametreler
`pAddress`  
[in] Adresi işlevi temsil eder.

`dwLine`  
[in] Satırı işlevi başından uzaklığı.

`ppNewAddress`  
[out] İşlev başından uzaklığı satırı temsil eden yeni adresi.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="example"></a>Örnek
Aşağıdaki örnek için bu yöntemi uygulaması gösterilmiştir bir **CDebugSymbolProvider** gösteren nesne [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md) arabirimi.

```cpp
HRESULT CDebugSymbolProvider::GetFunctionLineOffset(
    IDebugAddress *pAddress,
    DWORD dwLine,
    IDebugAddress **ppNewAddress
)
{
    HRESULT hr = S_OK;
    CDEBUG_ADDRESS address;
    CComPtr<CModule> pModule;
    DWORD dwOffset;
    CDebugAddress* paddr = NULL;

    METHOD_ENTRY(CDebugSymbolProvider::GetFunctionLineOffset);

    IfFalseGo( pAddress, S_FALSE );
    IfFailGo( pAddress->GetAddress( &address ) );

    ASSERT(address.addr.dwKind == ADDRESS_KIND_METADATA_METHOD);
    IfFalseGo( address.addr.dwKind == ADDRESS_KIND_METADATA_METHOD, S_FALSE );

    IfFailGo( GetModule( address.GetModule(), &pModule) );

    // Find the first offset for dwLine in the function

    IfFailGo( pModule->GetFunctionLineOffset( address.addr.addr.addrMethod.tokMethod,
              address.addr.addr.addrMethod.dwVersion,
              dwLine,
              &dwOffset ) );

    // Create the new Address

    address.addr.addr.addrMethod.dwOffset = dwOffset;
    IfNullGo( paddr = new CDebugAddress(address), E_OUTOFMEMORY );
    IfFailGo( paddr->QueryInterface( __uuidof(IDebugAddress),
                                     (void**) ppNewAddress ) );

Error:

    METHOD_EXIT(CDebugSymbolProvider::GetFunctionLineOffset, hr);
    RELEASE( paddr );
    return hr;
}
```

## <a name="see-also"></a>Ayrıca Bkz.
[IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md)
