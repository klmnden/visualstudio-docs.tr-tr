---
title: IDebugSymbolProvider | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugSymbolProvider
helpviewer_keywords:
- IDebugSymbolProvider interface
ms.assetid: df5f095f-1dee-46f9-84cf-92417c71d5fb
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: db4e5592fac73f629aba69fa23d1a7163c794875
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62915807"
---
# <a name="idebugsymbolprovider"></a>IDebugSymbolProvider
Bu arabirim sembollere ve türlere, alanları olarak döndürme sağlayan bir sembol sağlayıcısını temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugSymbolProvider : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
Sembol sağlayıcısı sembol sağlayın ve ifade değerlendiricisi bilgi yazmak için bu arabirimi uygulamalıdır.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
Bu arabirim, COM'ın kullanarak elde edilen `CoCreateInstance` işlevi (yönetilmeyen sembol sağlayıcıları) veya yönetilen bir kod derlemesi ve bu derlemede bulunan bilgilere dayanarak sembol sağlayıcısı örnekleme uygun yükleniyor. Hata ayıklama altyapısı ifade değerlendiricisi ile birlikte çalışmak için Sembol sağlayıcısı oluşturur. Bu arabirim örnekleme bir yaklaşım için örneğe bakın.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugSymbolProvider`.

|Yöntem|Açıklama|
|------------|-----------------|
|`Initialize`|Kullanım dışı. Kullanmayın.|
|`Uninitialize`|Kullanım dışı. Kullanmayın.|
|[GetContainerField](../../../extensibility/debugger/reference/idebugsymbolprovider-getcontainerfield.md)|Hata ayıklama adresi içeren alanı alır.|
|`GetField`|Kullanım dışı. Kullanmayın.|
|[GetAddressesFromPosition](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromposition.md)|Hata ayıklama adresi bir belge konumu dizisine eşler.|
|[GetAddressesFromContext](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromcontext.md)|Bir belge bağlamına bir hata ayıklama adresleri dizisine eşler.|
|[GetContextFromAddress](../../../extensibility/debugger/reference/idebugsymbolprovider-getcontextfromaddress.md)|Bir hata ayıklama adresi bir belge bağlamına eşler.|
|[GetLanguage](../../../extensibility/debugger/reference/idebugsymbolprovider-getlanguage.md)|Hata ayıklama adresten Kodu derlemek için kullanılan dili alır.|
|`GetGlobalContainer`|Kullanım dışı. Kullanmayın.|
|[GetMethodFieldsByName](../../../extensibility/debugger/reference/idebugsymbolprovider-getmethodfieldsbyname.md)|Temsil eden bir tam yöntemi ad alanını alır.|
|[GetClassTypeByName](../../../extensibility/debugger/reference/idebugsymbolprovider-getclasstypebyname.md)|Tam nitelikli sınıf adınız temsil eden sınıf alan türünü alır.|
|[GetNamespacesUsedAtAddress](../../../extensibility/debugger/reference/idebugsymbolprovider-getnamespacesusedataddress.md)|Hata ayıklama adresiyle ilişkili ad alanları için bir numaralandırıcı oluşturur.|
|[GetTypeByName](../../../extensibility/debugger/reference/idebugsymbolprovider-gettypebyname.md)|Sembol adı için bir simge türü eşler.|
|[GetNextAddress](../../../extensibility/debugger/reference/idebugsymbolprovider-getnextaddress.md)|Bir yöntemde belirli hata ayıklama adresi aşağıdaki hata ayıklama adresi alır.|

## <a name="remarks"></a>Açıklamalar
Bu arabirim, hata ayıklama adreslere ve belge konumları eşler.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="example"></a>Örnek
Bu örnekte, sembol sağlayıcısı (hata ayıklama altyapısı bu değer bilmeniz gerekir) GUID'sine verilen örneği gösterilmektedir.

```cpp
// A debug engine uses its own symbol provider and would know the GUID
// of that provider.
IDebugSymbolProvider *GetSymbolProvider(GUID *pSymbolProviderGuid)
{
    // This is typically defined globally. For this example, it is
    // defined here.
    static const WCHAR strRegistrationRoot[] = L"Software\\Microsoft\\VisualStudio\\8.0Exp";
    IDebugSymbolProvider *pProvider = NULL;
    if (pSymbolProviderGuid != NULL) {
        CLSID clsidProvider = { 0 };
        ::GetSPMetric(*pSymbolProviderGuid,
                      storetypeFile,
                      metricCLSID,
                      &clsidProvider,
                      strRegistrationRoot);
        if (IsEqualGUID(clsidProvider,GUID_NULL)) {
            // No file type provider, try metadata provider.
            ::GetSPMetric(*pSymbolProviderGuid,
                          ::storetypeMetadata,
                          metricCLSID,
                          &clsidProvider,
                          strRegistrationRoot);
        }
        if (!IsEqualGUID(clsidProvider,GUID_NULL)) {
            CComPtr<IDebugSymbolProvider> spSymbolProvider;
            spSymbolProvider.CoCreateInstance(clsidProvider);
            if (spSymbolProvider != NULL) {
                pProvider = spSymbolProvider.Detach();
            }
        }
    }
    return(pProvider);
}
```

## <a name="see-also"></a>Ayrıca Bkz.
- [Sembol Sağlayıcısı Arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
