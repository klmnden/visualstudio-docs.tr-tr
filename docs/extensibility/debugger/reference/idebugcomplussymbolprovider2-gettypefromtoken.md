---
title: IDebugComPlusSymbolProvider2::GetTypeFromToken | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugComPlusSymbolProvider2::GetTypeFromToken
- GetTypeFromToken
ms.assetid: 4452bc5d-0225-40e0-a467-c472a5c7c4ee
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 5212fe733e3590a7b15b5ade55d2bfd2aa4048dc
ms.sourcegitcommit: 748d9cd7328a30f8c80ce42198a94a4b5e869f26
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/15/2019
ms.locfileid: "66326162"
---
# <a name="idebugcomplussymbolprovider2gettypefromtoken"></a>IDebugComPlusSymbolProvider2::GetTypeFromToken
Kendi belirteci verilen bir türü alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetTypeFromToken(
    ULONG32       appDomain,
    GUID          guidModule,
    DWORD         tdToken,
    IDebugField** ppField
);
```

```csharp
int GetTypeFromToken(
    uint            appDomain,
    Guid            guidModule,
    uint            tdToken,
    out IDebugField ppField
);
```

## <a name="parameters"></a>Parametreler
`appDomain`\
[in] Uygulama etki alanı tanımlayıcısı.

`guidModule`\
[in] Modülün benzersiz tanımlayıcısı.

`tdToken`\
[in] Belirteci alınacak tür.

`ppField`\
[out] Tarafından temsil edilen türünü döndürüyor [IDebugField](../../../extensibility/debugger/reference/idebugfield.md).

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="example"></a>Örnek
Aşağıdaki örnek için bu yöntemi uygulaması gösterilmiştir bir **CDebugSymbolProvider** gösteren nesne [IDebugComPlusSymbolProvider2](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2.md) arabirimi.

```cpp
HRESULT CDebugSymbolProvider::GetTypeFromToken(
    ULONG32 ulAppDomainID,
    GUID guidModule,
    DWORD tdToken,
    IDebugField **ppField)
{
    HRESULT hr = E_FAIL;

    METHOD_ENTRY( CDebugDynamicFieldSymbol::GetTypeFromToken );

    ASSERT(IsValidObjectPtr(this, CDebugSymbolProvider));
    ASSERT(IsValidWritePtr(ppField, IDebugField*));

    Module_ID idModule(ulAppDomainID, guidModule);

    IfFailGo( this->CreateClassType(idModule, tdToken, ppField) );

Error:

    METHOD_EXIT( CDebugDynamicFieldSymbol::GetTypeFromToken, hr );

    return hr;
}
```

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugComPlusSymbolProvider2](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2.md)
