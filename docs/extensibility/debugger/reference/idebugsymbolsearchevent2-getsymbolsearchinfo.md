---
title: IDebugSymbolSearchEvent2::GetSymbolSearchInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugSymbolSearchEvent2::GetSymbolSearchInfo
helpviewer_keywords:
- IDebugSymbolSearchEvent2::GetSymbolSearchInfo
ms.assetid: ae9eb72b-f2aa-43b8-87ca-da19d2e78d17
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 9dcd584e600849ad30f83adef768671dc8f2ab57
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66320392"
---
# <a name="idebugsymbolsearchevent2getsymbolsearchinfo"></a>IDebugSymbolSearchEvent2::GetSymbolSearchInfo
Sembol yükleme işlemiyle ilgili sonuçları almak için bir olay işleyicisi olarak çağrılır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetSymbolSearchInfo(
   IDebugModule3**    pModule,
   BSTR*              pbstrDebugMessage,
   MODULE_INFO_FLAGS* pdwModuleInfoFlags
);
```

```csharp
int GetSymbolSearchInfo(
   IDebugModule3              pModule,
   ref string                 pbstrDebugMessage,
   out enum_MODULE_INFO_FLAGS pdwModuleInfoFlags
);
```

## <a name="parameters"></a>Parametreler
`pModule`\
[out] Bir IDebugModule3 simgeleri en iyi duruma yüklenen modül temsil eden nesne.

`pbstrDebugMessage`\
[out içinde] Modülünden herhangi bir hata iletisi içeren bir dize döndürür. Hata yoksa bu dize yalnızca modülün adı içerir ancak hiçbir zaman boş değildir.

> [!NOTE]
> [C++] `pbstrDebugMessage` olamaz `NULL` ve ile serbest bırakılmalıdır `SysFreeString`.

`pdwModuleInfoFlags`\
[out] Bayraklarının bir birleşimi [MODULE_INFO_FLAGS](../../../extensibility/debugger/reference/module-info-flags.md) simgeleri yüklenmiş olup olmadığını belirten sabit listesi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir işleyici aldığında [IDebugSymbolSearchEvent2](../../../extensibility/debugger/reference/idebugsymbolsearchevent2.md) bir modül için hata ayıklama sembolleri için bir girişimde sonra olay işleyicisi Bu yük sonuçları belirlemek için bu yöntem çağırabilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugModule3](../../../extensibility/debugger/reference/idebugmodule3.md)
- [MODULE_INFO_FLAGS](../../../extensibility/debugger/reference/module-info-flags.md)
- [IDebugSymbolSearchEvent2](../../../extensibility/debugger/reference/idebugsymbolsearchevent2.md)