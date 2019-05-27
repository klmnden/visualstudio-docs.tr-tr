---
title: IDebugExpressionContext2::ParseText | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugExpressionContext2::ParseText
helpviewer_keywords:
- IDebugExpressionContext2::ParseText
ms.assetid: f58575db-f926-4ac8-83ff-7b3b86ab61e2
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: f0f11c3b1770ca32b34f7a5480d5d56acc2b2478
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66201040"
---
# <a name="idebugexpressioncontext2parsetext"></a>IDebugExpressionContext2::ParseText
Daha sonra değerlendirmesi için metin biçiminde bir ifade ayrıştırır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT ParseText(
    LPCOLESTR           pszCode,
    PARSEFLAGS          dwFlags,
    UINT                nRadix,
    IDebugExpression2** ppExpr,
    BSTR*               pbstrError,
    UINT*               pichError
);
```

```csharp
int ParseText(
    string                pszCode,
    enum_PARSEFLAGS       dwFlags,
    uint                  nRadix,
    out IDebugExpression2 ppExpr,
    out string            pbstrError,
    out uint              pichError
);
```

## <a name="parameters"></a>Parametreler
`pszCode`\
[in] Ayrıştırılacak ifade.

`dwFlags`\
[in] Bayraklarının bir birleşimi [PARSEFLAGS](../../../extensibility/debugger/reference/parseflags.md) ayrıştırma denetleyen sabit listesi.

`nRadix`\
[in] Herhangi bir sayısal bilgisi Ayrıştırmada kullanılacak sayı tabanı `pszCode`.

`ppExpr`\
[out] Döndürür [IDebugExpression2](../../../extensibility/debugger/reference/idebugexpression2.md) bağlama ve değerlendirme için hazır olan ayrıştırılmış ifadeyi temsil eden nesne.

`pbstrError`\
[out] İfade bir hata varsa hata iletisi döndürür.

`pichError`\
[out] Hata karakter dizinini döndürür `pszCode` ifade bir hata içeriyorsa.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
Bu yöntem çağrıldığında, hata ayıklama altyapısı (DE) ifade ayrıştırma ve doğruluğu doğrulayın. `pbstrError` Ve `pichError` parametreleri doldurulmuş ifade geçersizse.

İfade, yalnızca ayrıştırılmış değerlendirilmez olduğunu unutmayın. Bir sonraki çağrı [EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) veya [EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md) yöntemleri ayrıştırılmış ifadeyi değerlendirir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu yöntem için basit bir uygulama gösterilmektedir `CEnvBlock` gösteren nesne [IDebugExpressionContext2](../../../extensibility/debugger/reference/idebugexpressioncontext2.md) arabirimi. Bu örnek, bir ortam değişkeni adı olarak ayrıştırılmak için ifadeyi değerlendirir ve söz konusu değişkeninin değerini alır.

```cpp
HRESULT CEnvBlock::ParseText(
    LPCOLESTR           pszCode,
    PARSEFLAGS          dwFlags,
    UINT                nRadix,
    IDebugExpression2 **ppExpr,
    BSTR               *pbstrError,
    UINT               *pichError)
{
    HRESULT hr = E_OUTOFMEMORY;
    // Create an integer variable with a value equal to one plus
    // twice the length of the passed expression to be parsed.
    int iAnsiLen      = 2 * (wcslen(pszCode)) + 1;
    // Allocate a character string of the same length.
    char *pszAnsiCode = (char *) malloc(iAnsiLen);

    // Check for successful memory allocation.
    if (pszAnsiCode) {
        // Map the wide-character pszCode string to the new pszAnsiCode character string.
        WideCharToMultiByte(CP_ACP, 0, pszCode, -1, pszAnsiCode, iAnsiLen, NULL, NULL);
        // Check to see if the app can succesfully get the environment variable.
        if (GetEnv(pszAnsiCode)) {

            // Create and initialize a CExpression object.
            CComObject<CExpression> *pExpr;
            CComObject<CExpression>::CreateInstance(&pExpr);
            pExpr->Init(pszAnsiCode, this, NULL);

            // Assign the pointer to the new object to the passed argument
            // and AddRef the object.
            *ppExpr = pExpr;
            (*ppExpr)->AddRef();
            hr = S_OK;
        // If the program cannot succesfully get the environment variable.
        } else {
            // Set the errror message and return E_FAIL.
            *pbstrError = SysAllocString(L"No such environment variable.");
            hr = E_FAIL;
        }
        // Free the local character string.
        free(pszAnsiCode);
    }
    return hr;
}
```

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugExpressionContext2](../../../extensibility/debugger/reference/idebugexpressioncontext2.md)
- [PARSEFLAGS](../../../extensibility/debugger/reference/parseflags.md)
- [IDebugExpression2](../../../extensibility/debugger/reference/idebugexpression2.md)
- [EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md)
- [EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md)
