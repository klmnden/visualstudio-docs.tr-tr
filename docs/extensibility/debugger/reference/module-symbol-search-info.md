---
title: MODULE_SYMBOL_SEARCH_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MODULE_SYMBOL_SEARCH_INFO
helpviewer_keywords:
- MODULE_SYMBOL_SEARCH_INFO structure
ms.assetid: 432aff03-08a5-4c5a-b2d5-e212090fc70a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: e374860bcd80f0a199e5dc55b4b556d94d99aba6
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65460936"
---
# <a name="modulesymbolsearchinfo"></a>MODULE_SYMBOL_SEARCH_INFO

Arandığını sembol arama yolları hakkındaki durum bilgilerini içerir.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _tagSYMBOL_SEARCH_INFO
{
    SYMBOL_SEARCH_INFO_FIELDS dwValidFields;
    BSTR                      bstrVerboseSearchInfo;
} MODULE_SYMBOL_SEARCH_INFO;
```

```csharp
public struct MODULE_SYMBOL_SEARCH_INFO {
    public uint   dwValidFields;
    public string bstrVerboseSearchInfo;
}
```

## <a name="members"></a>Üyeler

`dwValidFields`\

Bayraklarının bir birleşimi [SYMBOL_SEARCH_INFO_FIELDS](../../../extensibility/debugger/reference/symbol-search-info-fields.md) bu yapısı içinde açıklanan arama bilgi türünü belirten sabit listesi.

`bstrVerboseSearchInfo`\

Arama yolu ve tek bir dize olarak birleştirilmiş sonuçlar.

## <a name="remarks"></a>Açıklamalar

Bu yapı çağrısından döndürülen [GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md) yöntemi.

Varsa `bstrVerboseSearchInfo` alanı boş değil ve ardından arama yolları ve bu arama sonuçlarının bir listesini içerir. Listenin sonuca göre ve ardından üç nokta ("..."), ardından bir yol ile biçimlendirilir. Birden fazla yol sonuç çifti varsa, her bir çifti "\r\n" (satır başı-başı/satır besleme) çifti tarafından ayrılmış. Desen şöyle görünür:

\<yolu >... \<sonucu > \r\n\<yolu >... \<sonucu > \r\n\<yolu >... \<sonucu >

En son giriş \r\n dizisi yok unutmayın.

Olası bir işte `bstrVerboseSearchInfo` standart çıkış için gönderilen bir dize.

`c:\symbols\user32.pdb... File not found.`

`c:\winnt\symbols\user32.pdb... Version does not match.`

`\\symbols\symbols\user32.dll\0a8sd0ad8ad\user32.pdb... Symbols loaded.`

## <a name="requirements"></a>Gereksinimler

Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.

- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md)