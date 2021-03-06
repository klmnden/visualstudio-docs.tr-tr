---
title: Arkadaş (hata ayıklama arabirimi Erişim SDK'sı) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- friend functions [DIA SDK]
- friend classes [DIA SDK]
- Friend symbol
ms.assetid: 5147a170-41ce-4727-8ace-c318e8d11647
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 118a6b6caf6a208898bba3894d532e5dc6e4a14a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62554697"
---
# <a name="friend-debug-interface-access-sdk"></a>Arkadaş (Arabirim Erişimi SDK'sında Hata Ayıklama)
Arkadaş sınıfları ve arkadaş işlevleri tanımlanır `SymTagFriend` semboller. Kullanıcı tanımlı türler(UDT) üst öğesinin alt öğeleri olan ve sahip bir [Idiasymbol::get_classparent](../../debugger/debug-interface-access/idiasymbol-get-classparent.md) özelliği.

## <a name="properties"></a>Özellikler
 Bu sembol türü için geçerli ek özellikler aşağıdaki tabloda gösterilmektedir.

|Özellik|Veri türü|Açıklama|
|--------------|---------------|-----------------|
|[IDiaSymbol::get_classParent](../../debugger/debug-interface-access/idiasymbol-get-classparent.md)|`IDiaSymbol*`|UDT üst simge.|
|[IDiaSymbol::get_classParentId](../../debugger/debug-interface-access/idiasymbol-get-classparentid.md)|`DWORD`|Sınıf üst simge kimliği.|
|[IDiaSymbol::get_name](../../debugger/debug-interface-access/idiasymbol-get-name.md)|`BSTR`|Sınıf veya işlevin adı.|
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol-get-symindexid.md)|`DWORD`|Sembol, dizin kimliği.|
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)|`DWORD`|Döndürür `SymTagFriend` (biri [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) değerler).|
|[IDiaSymbol::get_type](../../debugger/debug-interface-access/idiasymbol-get-type.md)|`IDiaSymbol*`|Sınıf veya işlev simgesi.|
|[IDiaSymbol::get_typeId](../../debugger/debug-interface-access/idiasymbol-get-typeid.md)|`DWORD`|Tür simgesi kimliği.|

## <a name="see-also"></a>Ayrıca Bkz.
- [Simge Türlerinin Sınıf Hiyerarşisi](../../debugger/debug-interface-access/class-hierarchy-of-symbol-types.md)