---
title: IDebugModule2::ReloadSymbols_Deprecated | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugModule2::ReloadSymbols
helpviewer_keywords:
- IDebugModule2::ReloadSymbols method
ms.assetid: 0f9f0133-7d58-4cd9-a6ca-1141e095749d
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 635e305c0dd88d72017048da6353f813fcc46406
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66323955"
---
# <a name="idebugmodule2reloadsymbolsdeprecated"></a>IDebugModule2::ReloadSymbols_Deprecated
ARTIK KULLANILMIYOR. KULLANMAYIN. Bu modüle ilişkin simgeleri yeniden yükler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT ReloadSymbols( 
   LPCOLESTR pszUrlToSymbols,
   BSTR*     pbstrDebugMessage
);
```

```csharp
int ReloadSymbols( 
   string     pszUrlToSymbols,
   out string pbstrDebugMessage
);
```

## <a name="parameters"></a>Parametreler
`pszUrlToSymbols`\
[in] Sembol deposu yolu.

`pbstrDebugMessage`\
[out] Örneğin modül adı modüller penceresini sağındaki görüntülenen bir durum veya hata iletisi, bir bilgilendirme iletisi döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Hata ayıklama altyapısı her zaman döndürmelidir `E_FAIL`.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem artık desteklenmiyor. Uygulama [LoadSymbols](../../../extensibility/debugger/reference/idebugmodule3-loadsymbols.md) yöntemi yerine.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md)
- [LoadSymbols](../../../extensibility/debugger/reference/idebugmodule3-loadsymbols.md)