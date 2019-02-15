---
title: GetMethodProperty uygulama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- GetMethodProperty method
- IDebugExpressionEvaluator2 property
ms.assetid: 6305874f-a2c4-4432-834c-07530ea84bff
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 41a198b56576367058a8f3f701e03d0772bad47a
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56315956"
---
# <a name="implement-getmethodproperty"></a>GetMethodProperty uygulama
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için bkz: [CLR ifade değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

Visual Studio hata ayıklama altyapısının (DE) çağıran [GetDebugProperty](../../extensibility/debugger/reference/idebugstackframe2-getdebugproperty.md), sırayla çağıran [GetMethodProperty](../../extensibility/debugger/reference/idebugexpressionevaluator-getmethodproperty.md) yığın çerçevesinde geçerli yöntemi hakkında bilgi edinmek için.

Bu uygulaması `IDebugExpressionEvaluator::GetMethodProperty` aşağıdaki görevleri gerçekleştirir:

1. Çağrıları [GetContainerField](../../extensibility/debugger/reference/idebugsymbolprovider-getcontainerfield.md), içinde geçen [IDebugAddress](../../extensibility/debugger/reference/idebugaddress.md) nesne. Sembol sağlayıcısı (SP) döndüren bir [IDebugContainerField](../../extensibility/debugger/reference/idebugcontainerfield.md) belirtilen adres içeren yöntemi temsil eden.

2. Alır [IDebugMethodField](../../extensibility/debugger/reference/idebugmethodfield.md) gelen `IDebugContainerField`.

3. Bir sınıf oluşturur (adlı `CFieldProperty` Bu örnekte) uygulayan [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) arabirim ve içeren `IDebugMethodField` nesne SP'yi döndürdü

4. Döndürür `IDebugProperty2` alanından arabirim `CFieldProperty` nesne.

## <a name="managed-code"></a>Yönetilen kod
Bu örnekte uygulanışı gösterilmektedir `IDebugExpressionEvaluator::GetMethodProperty` yönetilen kod.

```csharp
namespace EEMC
{
    [GuidAttribute("462D4A3D-B257-4AEE-97CD-5918C7531757")]
    public class EEMCClass : IDebugExpressionEvaluator
    {
        public HRESULT GetMethodProperty(
                IDebugSymbolProvider symbolProvider,
                IDebugAddress        address,
                IDebugBinder         binder,
                int                  includeHiddenLocals,
            out IDebugProperty2      property)
        {
            IDebugContainerField containerField = null;
            IDebugMethodField methodField       = null;
            property = null;

            // Get the containing method field.
            symbolProvider.GetContainerField(address, out containerField);
            methodField = (IDebugMethodField) containerField;

            // Return the property of method field.
            property = new CFieldProperty(symbolProvider, address, binder, methodField);
            return COM.S_OK;
        }
    }
}
```

## <a name="unmanaged-code"></a>Yönetilmeyen kod
Bu örnekte uygulanışı gösterilmektedir `IDebugExpressionEvaluator::GetMethodProperty` yönetilmeyen kod.

```
[CPP]
STDMETHODIMP CExpressionEvaluator::GetMethodProperty(
        in IDebugSymbolProvider *pprovider,
        in IDebugAddress        *paddress,
        in IDebugBinder         *pbinder,
        in BOOL                  includeHiddenLocals,
        out IDebugProperty2    **ppproperty
    )
{
    if (pprovider == NULL)
        return E_INVALIDARG;

    if (ppproperty == NULL)
        return E_INVALIDARG;
    else
        *ppproperty = 0;

    HRESULT hr;
    IDebugContainerField* pcontainer = NULL;

    hr = pprovider->GetContainerField(paddress, &pcontainer);
    if (FAILED(hr))
        return hr;

    IDebugMethodField*    pmethod    = NULL;
    hr = pcontainer->QueryInterface( IID_IDebugMethodField,
            reinterpret_cast<void**>(&pmethod));
    pcontainer->Release();
    if (FAILED(hr))
        return hr;

    CFieldProperty* pfieldProperty = new CFieldProperty( pprovider,
                                                         paddress,
                                                         pbinder,
                                                         pmethod );
    pmethod->Release();
    if (!pfieldProperty)
        return E_OUTOFMEMORY;

    hr = pfieldProperty->Init();
    if (FAILED(hr))
    {
        pfieldProperty->Release();
        return hr;
    }

    hr = pfieldProperty->QueryInterface( IID_IDebugProperty2,
            reinterpret_cast<void**>(ppproperty));
    pfieldProperty->Release();

    return hr;
}
```

## <a name="see-also"></a>Ayrıca bkz.
[Örnek yerel öğeler uygulaması](../../extensibility/debugger/sample-implementation-of-locals.md)
