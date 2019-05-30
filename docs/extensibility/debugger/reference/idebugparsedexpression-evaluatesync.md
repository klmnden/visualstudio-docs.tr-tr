---
title: IDebugParsedExpression::EvaluateSync | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugParsedExpression::EvaluateSync
helpviewer_keywords:
- IDebugParsedExpression::EvaluateSync method
ms.assetid: 0ea04cfa-de87-4b6c-897e-4572c1a28942
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: aac58831224a6bebadd625dad72177f2aec3fc76
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66311819"
---
# <a name="idebugparsedexpressionevaluatesync"></a>IDebugParsedExpression::EvaluateSync
Bu yöntem, Ayrıştırılan ifadeyi değerlendirir ve isteğe bağlı olarak başka bir veri türü sonucu çevirir.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EvaluateSync( 
   DWORD                 dwEvalFlags,
   DWORD                 dwTimeout,
   IDebugSymbolProvider* pSymbolProvider,
   IDebugAddress*        pAddress,
   IDebugBinder*         pBinder,
   BSTR                  bstrResultType,
   IDebugProperty2**     ppResult
);
```

```csharp
int EvaluateSync(
   uint                 dwEvalFlags,
   uint                 dwTimeout,
   IDebugSymbolProvider pSymbolProvider,
   IDebugAddress        pAddress,
   IDebugBinder         pBinder,
   string               bstrResultType,
   out IDebugProperty2  ppResult
);
```

## <a name="parameters"></a>Parametreler
`dwEvalFlags`\
[in] Bir birleşimi [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md) ifade nasıl değerlendirileceğini kontrol sabitler.

`dwTimeout`\
[in] Bu yöntemden geri dönmeden önce beklenecek milisaniye cinsinden en uzun süreyi belirtir. Kullanım `INFINITE` süresiz bekleme.

`pSymbolProvider`\
[in] Sembol sağlayıcısı olarak ifade edilen, bir [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md) arabirimi.

`pAddress`\
[in] Geçerli yürütme konumu olarak ifade edilen bir yöntem içinde bir [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi.

`pBinder`\
[in] İfade bağlayıcı bir [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md) arabirimi.

`bstrResultType`\
[in] Sonuç türü için atamalısınız. Bu bağımsız değişken null değeri olabilir.

`ppResult`\
[out] Döndürür [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) değerlendirme sonuçlarını temsil eden arabirim.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 İfade değerlendirme bağlamının tarafından verilen `pAddress`, hangi içeren yöntemini belirlemek üzere mümkün kılar ve ardından ifade sembolleri değerini belirlemek için kullanım dil kapsam kuralları.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)
- [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)
- [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)
- [IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md)