---
title: IDebugExpressionEvaluator::GetMethodProperty | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugExpressionEvaluator::GetMethodProperty
helpviewer_keywords:
- IDebugExpressionEvaluator::GetMethodProperty method
ms.assetid: c394fe4d-eeb6-4feb-828c-098d84a6f1ba
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 0d965161f6f0a6aadd8aab89a3001e56c2e807fa
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66325702"
---
# <a name="idebugexpressionevaluatorgetmethodproperty"></a>IDebugExpressionEvaluator::GetMethodProperty
Bu yöntem, yerel öğeler, bağımsız değişkenleri ve diğer bir yöntem özelliklerini içeren bir özellik nesnesi alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetMethodProperty( 
   IDebugSymbolProvider* pSymbolProvider,
   IDebugAddress*        pAddress,
   IDebugBinder*         pBinder,
   BOOL                  fIncludeHiddenLocals,
   IDebugProperty2**     ppProperty
);
```

```csharp
int GetMethodProperty(
   IDebugSymbolProvider pSymbolProvider,
   IDebugAddress        pAddress,
   IDebugBinder         pBinder,
   int                  fIncludeHiddenLocals,
   out IDebugProperty2  ppProperty
);
```

## <a name="parameters"></a>Parametreler
`pSymbolProvider`\
[in] Sembol sağlayıcısı kullanılmak üzere ifade olarak bir [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md) nesne.

`pAddress`\
[in] Adresi olarak ifade edilen kodda bir [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) yakın içeren çözümleneceği nesne, işlev.

`pBinder`\
[in] Bağlayıcı kullanılmak üzere ifade olarak bir [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md) nesne.

`fIncludeHiddenLocals`\
[in] Sıfır olmayan (`TRUE`) anlamına gelir; gizli Yereller dahil etmek sıfır (`FALSE`) gizli Yereller bırakmak anlamına gelir

`ppProperty`\
[out] Döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) yöntemi temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Gizli yerel öğeler, genellikle derleyici tarafından oluşturulan değişkenleri de kullanılabilir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugExpressionEvaluator](../../../extensibility/debugger/reference/idebugexpressionevaluator.md)
- [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)
- [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)
- [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)