---
title: IDebugComPlusSymbolProvider::GetEntryPoint | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugComPlusSymbolProvider::GetEntryPoint
- GetEntryPoint
ms.assetid: 9640e121-1da1-41f9-8e66-76efca36baf2
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 961655b82873b01596c5baaf5aaf08997d4b5abc
ms.sourcegitcommit: 7153e2fc717d32e0e9c8a9b8c406dc4053c9fd53
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "56413156"
---
# <a name="idebugcomplussymbolprovidergetentrypoint"></a>IDebugComPlusSymbolProvider::GetEntryPoint
Uygulama giriş noktasını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetEntryPoint(
    ULONG32         ulAppDomainID,
    GUID            guidModule,
    IDebugAddress** ppAddress
);
```

```csharp
int GetEntryPoint(
    uint              ulAppDomainID,
    Guid              guidModule,
    out IDebugAddress ppAddress
);
```

#### <a name="parameters"></a>Parametreler
`ulAppDomainID`  
[in] Uygulama etki alanı için tanımlayıcı.

`guidModule`  
[in] Modül için benzersiz tanımlayıcı.

`ppAddress`  
[out] Tarafından temsil edilen giriş noktası döndüren bir [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="example"></a>Örnek
Aşağıdaki örnek için bu yöntemi uygulaması gösterilmiştir bir **CDebugSymbolProvider** gösteren nesne [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md) arabirimi.

```cpp
HRESULT CDebugSymbolProvider::GetEntryPoint(
    ULONG32 ulAppDomainID,
    GUID guidModule,
    IDebugAddress **ppAddress
)
{
    HRESULT hr = S_OK;
    CComPtr<CModule> pModule;
    Module_ID idModule(ulAppDomainID, guidModule);

    ASSERT(IsValidObjectPtr(this, CDebugSymbolProvider));
    ASSERT(IsValidWritePtr(ppAddress, IDebugAddress *));

    METHOD_ENTRY( CDebugSymbolProvider::GetEntryPoint );

    IfFalseGo( ppAddress, E_INVALIDARG );

    *ppAddress = NULL;

    IfFailGo( GetModule( idModule, &pModule) );

    IfFailGo( pModule->GetEntryPoint( ppAddress ) );

Error:

    METHOD_EXIT( CDebugSymbolProvider::GetEntryPoint, hr );

    return hr;
}
```

## <a name="see-also"></a>Ayrıca Bkz.
[IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md)
