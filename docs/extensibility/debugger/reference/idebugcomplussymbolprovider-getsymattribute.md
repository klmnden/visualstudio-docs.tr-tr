---
title: IDebugComPlusSymbolProvider::GetSymAttribute | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugComPlusSymbolProvider::GetSymAttribute
- GetSymAttribute
ms.assetid: 6cbaac92-a60b-4165-a7f5-c34407770f3c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: beee5d22212808eb4f6d99820e7a14a32fc16f5e
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66206363"
---
# <a name="idebugcomplussymbolprovidergetsymattribute"></a>IDebugComPlusSymbolProvider::GetSymAttribute
Belirtilen modül için belirtilen üst öznitelik ile hata ayıklama sembolleri alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetSymAttribute (
    ULONG32  ulAppDomainID,
    GUID     guidModule,
    _mdToken tokParent,
    LPOLESTR pstrName,
    ULONG32  cBuffer,
    ULONG32* pcBuffer,
    BYTE*    buffer
);
```

```csharp
int GetSymAttribute (
    uint      ulAppDomainID,
    Guid      guidModule,
    int       tokParent,
    string    pstrName,
    uint      cBuffer,
    out uint  pcBuffer,
    out int[] buffer
);
```

## <a name="parameters"></a>Parametreler
`ulAppDomainID`\
[in] Uygulama etki alanı tanımlayıcısı.

`guidModule`\
[in] Modülün benzersiz tanımlayıcısı.

`tokParent`\
[in] Üst öznitelikte belirteci.

`pstrName`\
[in] Modülün adı.

`cBuffer`\
[in] Çıkış için gereken bayt sayısını `buffer`.

`pcBuffer`\
[out] Çıkış uzunluğunu `buffer`.

`buffer`\
[out] Simgeleri içeren bir dizi.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="example"></a>Örnek
Aşağıdaki örnek için bu yöntemi uygulaması gösterilmiştir bir **CDebugSymbolProvider** gösteren nesne [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md) arabirimi.

```cpp
HRESULT CDebugSymbolProvider::GetSymAttribute(
    ULONG32 ulAppDomainID,
    GUID guidModule,
    _mdToken tokParent,
    __in_z LPOLESTR pstrName,
    ULONG32 cBuffer,
    ULONG32 *pcBuffer,
    BYTE buffer[])
{
    HRESULT hr = S_OK;
    CComPtr<CModule> pModule;
    Module_ID idModule(ulAppDomainID, guidModule);

    METHOD_ENTRY( CDebugSymbolProvider::GetSymAttribute );

    IfFailGo( GetModule( idModule, &pModule) );

    IfFailGo( pModule->GetSymAttribute( tokParent, pstrName, cBuffer, pcBuffer, buffer ) );

Error:

    METHOD_EXIT(CDebugSymbolProvider::GetSymAttribute, hr);

    return hr;
}
```

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md)
