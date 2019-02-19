---
title: IDebugComPlusSymbolProvider2::GetTypesByName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- GetTypesByName
- IDebugComPlusSymbolProvider2::GetTypesByName
ms.assetid: ef76b1a8-6910-48fe-b4af-d9045eefd23f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d23b88cbb9bc2c87ef42ba729d7b98359ac3a2a1
ms.sourcegitcommit: 7153e2fc717d32e0e9c8a9b8c406dc4053c9fd53
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "56413455"
---
# <a name="idebugcomplussymbolprovider2gettypesbyname"></a>IDebugComPlusSymbolProvider2::GetTypesByName
Adı verilen bir türü alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetTypesByName(
    LPCOLESTR          pszClassName,
    NAME_MATCH         nameMatch,
    IEnumDebugFields** ppEnum
);
```

```csharp
int GetTypesByName(
    string               pszClassName,
    enum_ NAME_MATCH     nameMatch,
    out IEnumDebugFields ppEnum
);
```

#### <a name="parameters"></a>Parametreler
`pszClassName`  
[in] Türün adı.

`nameMatch`  
[in] Türü eşleşen, örneğin, büyük/küçük harfe seçer. Bir değer [NAME_MATCH](../../../extensibility/debugger/reference/name-match.md) sabit listesi.

`ppEnum`  
[out] Belirtilen ada sahip türlerini içeren bir numaralandırıcı.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
Genel türler, adı için konum için ' listesi\<int >' veya ' listesi\<int, int >' 'List' olacaktır. Türleri aynı ada sahip birden çok modül içinde görünüp görünmediğini `ppEnum` parametresi tüm kopyalarını içerir. Kullanmak zorunda [GetTypeInfo](../../../extensibility/debugger/reference/idebugfield-gettypeinfo.md) ve temel alınarak ayırt `guidModule` parametresi.

## <a name="example"></a>Örnek
Aşağıdaki örnek için bu yöntemi uygulaması gösterilmiştir bir **CDebugSymbolProvider** gösteren nesne [IDebugComPlusSymbolProvider2](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2.md) arabirimi.

```cpp
HRESULT CDebugSymbolProvider::GetTypesByName(
    LPCOLESTR pszClassName,
    NAME_MATCH nameMatch,
    IEnumDebugFields** ppEnum
)
{
    HRESULT hr = S_OK;
    CModIter ModIter;
    CModule* pmodule; // the iterator owns the reference
    CFieldList listField;

    ASSERT(IsValidWideStringPtr(pszClassName));
    ASSERT(IsValidWritePtr(ppEnum, IEnumDebugFields*));

    METHOD_ENTRY( CDebugSymbolProvider::GetTypesByName );

    IfFalseGo( pszClassName && ppEnum, E_INVALIDARG );
    *ppEnum = NULL;

    IfFailGo( GetModuleIter(&ModIter) );

    hr = S_FALSE;

    if ( nameMatch == nmCaseInsensitive)
    {
        while (ModIter.GetNext(&pmodule))
        {
            if (pmodule->FindTypesByNameCaseInsensitive( pszClassName,
                    &listField,
                    this ) )
            {
                hr = S_OK;
            }
        }
    }
    else
    {
        while (ModIter.GetNext(&pmodule))
        {
            if (pmodule->FindTypesByName( pszClassName,
                                          &listField,
                                          this) )
            {
                hr = S_OK;
            }
        }
    }

    // If the list is empty then no type
    IfFalseGo( listField.GetCount(), E_FAIL );

    // Create enumerator
    IfFailGo( CreateEnumerator( ppEnum, &listField ) );

Error:

    METHOD_EXIT( CDebugSymbolProvider::GetTypesByName, hr );

    return hr;
}
```

## <a name="see-also"></a>Ayrıca Bkz.
[IDebugComPlusSymbolProvider2](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2.md)
