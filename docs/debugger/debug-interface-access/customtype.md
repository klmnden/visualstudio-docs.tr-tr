---
title: CustomType | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- CustomType symbol
ms.assetid: 1b66bc0a-7979-416f-bf7f-e5df91584c91
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f960ebddbe5e58371f6a8bc7bd592be2fc2f25fa
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62555058"
---
# <a name="customtype"></a>CustomType
Satıcı tanımlı türleri (derleyici özel türleri) tarafından tanımlanır bir `SymTagCustomType` sembol.

## <a name="properties"></a>Özellikler
 Bu sembol türü için geçerli ek özellikler aşağıdaki tabloda gösterilmektedir.

|Özellik|Veri türü|Açıklama|
|--------------|---------------|-----------------|
|[IDiaSymbol::get_oemId](../../debugger/debug-interface-access/idiasymbol-get-oemid.md)|`DWORD`|OEM tanımlayıcısı.|
|[IDiaSymbol::get_oemSymbolId](../../debugger/debug-interface-access/idiasymbol-get-oemsymbolid.md)|`DWORD`|OEM iç kimliği.|
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol-get-symindexid.md)|`DWORD`|Sembol, dizin kimliği.|
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)|`DWORD`|Döndürür `SymTagCustomType` (biri [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) değerler).|
|[IDiaSymbol::get_type](../../debugger/debug-interface-access/idiasymbol-get-type.md)|`IDiaSymbol*`|Özel tür simgesi tarafından başvurulan ilk türü.|
|[IDiaSymbol::get_typeId](../../debugger/debug-interface-access/idiasymbol-get-typeid.md)|`DWORD`|Tür simgesi kimliği.|
|[IDiaSymbol::get_types](../../debugger/debug-interface-access/idiasymbol-get-types.md)|`IDiaSymbol**`|Özel tür simgesi tarafından başvurulan tüm türleri dizisi.|

## <a name="see-also"></a>Ayrıca Bkz.
- [Simge Türlerinin Sınıf Hiyerarşisi](../../debugger/debug-interface-access/class-hierarchy-of-symbol-types.md)