---
title: IDebugExpressionEvaluator | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugExpressionEvaluator
helpviewer_keywords:
- IDebugExpressionEvaluator interface
ms.assetid: 0636d8c3-625a-49fa-94b6-516f22b7e1bc
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0b54b8d4ab6c30bcefe99928409680ed5fa08cb0
ms.sourcegitcommit: 845442e2b515c3ca1e4e47b46cc1cef4df4f08d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56449859"
---
# <a name="idebugexpressionevaluator"></a>IDebugExpressionEvaluator
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

Bu arabirim, ifade değerlendiricisi temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugExpressionEvaluator : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
İfade değerlendirici bu arabirimini uygulaması gerekir.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
Bu arabirim elde etmek için ifade değerlendirici aracılığıyla örneği `CoCreateInstance` değerlendirici sınıfı kimliği (CLSID) kullanarak yöntemi. Örneğe bakın.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugExpressionEvaluator`.

|Yöntem|Açıklama|
|------------|-----------------|
|[Parse](../../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md)|Bir ifade dizesini ayrıştırılmış bir ifadeyi dönüştürür.|
|[GetMethodProperty](../../../extensibility/debugger/reference/idebugexpressionevaluator-getmethodproperty.md)|Yerel değişkenleri, bağımsız değişkenleri ve diğer bir yöntem özelliklerini alır.|
|[GetMethodLocationProperty](../../../extensibility/debugger/reference/idebugexpressionevaluator-getmethodlocationproperty.md)|Bir yöntem konum ve uzaklığı bir bellek adresine dönüştürür.|
|[SetLocale](../../../extensibility/debugger/reference/idebugexpressionevaluator-setlocale.md)|Yazdırılabilir sonuçları oluşturmak için kullanılacak dili belirler.|
|[SetRegistryRoot](../../../extensibility/debugger/reference/idebugexpressionevaluator-setregistryroot.md)|Kayıt defteri kökü ayarlar. Yan yana hata ayıklamak için kullanılır.|

## <a name="remarks"></a>Açıklamalar
Tipik bir durumda, hata ayıklama altyapısı (DE) çağrı sonucunda ifade değerlendiricisi (EE) başlatır [ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md). Dil ve istediği kullanılacak EE satıcı DE bildiği için DE EE'ın CLSID kayıt defterinden alır. ( [hata ayıklama için SDK Yardımcıları](../../../extensibility/debugger/reference/sdk-helpers-for-debugging.md) işlevi `GetEEMetric`, bu alma ile yardımcı olur).

EE örneği sonra DE çağırır [ayrıştırma](../../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md) ifade ayrıştırma ve depolamak için bir [IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md) nesne. Daha sonra bir çağrı [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md) ifadeyi değerlendirir.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: ee.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="example"></a>Örnek
Bu örnekte, kaynak kodunda bir sembol sağlayıcısı ve adresi verilen ifade değerlendiricisi örneği gösterilmektedir. Bu örnekte, bir işlev `GetEEMetric`, gelen [hata ayıklama için SDK Yardımcıları](../../../extensibility/debugger/reference/sdk-helpers-for-debugging.md) kitaplığı, dbgmetric.lib.

```cpp
IDebugExpressionEvaluator GetExpressionEvaluator(IDebugSymbolProvider pSymbolProvider,
                                                 IDebugAddress *pSourceAddress)
{
    // This is typically defined globally but is specified here just
    // for this example.
    static const WCHAR strRegistrationRoot[] = L"Software\\Microsoft\\VisualStudio\\8.0Exp";

    IDebugExpressionEvaluator *pEE = NULL;
    if (pSymbolProvider != NULL && pSourceAddress != NULL) {
        HRESULT hr         = S_OK;
        GUID  languageGuid = { 0 };
        GUID  vendorGuid   = { 0 };

        hr = pSymbolProvider->GetLanguage(pSourceAddress,
                                          &languageGuid,
                                          &vendorGuid);
        if (SUCCEEDED(hr)) {
            CLSID clsidEE = { 0 };
            CComPtr<IDebugExpressionEvaluator> spExpressionEvaluator;
            // Get the expression evaluator's CLSID from the registry.
            ::GetEEMetric(languageGuid,
                          vendorGuid,
                          metricCLSID,
                          &clsidEE,
                          strRegistrationRoot);
            if (!IsEqualGUID(clsidEE,GUID_NULL)) {
                // Instantiate the expression evaluator.
                spExpressionEvaluator.CoCreateInstance(clsidEE);
            }
            if (spExpressionEvaluator != NULL) {
                pEE = spExpressionEvaluator.Detach();
            }
        }
    }
    return pEE;
}
```

## <a name="see-also"></a>Ayrıca Bkz.
[İfade Değerlendirme Arabirimleri](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)  
[ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md)  
[IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md)  
[EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md)  
[Hata Ayıklama için SDK Yardımcıları](../../../extensibility/debugger/reference/sdk-helpers-for-debugging.md)
