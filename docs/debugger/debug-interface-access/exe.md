---
title: Exe | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- .dll files
- Exe symbol
- .exe files
- executable files, Exe symbol
ms.assetid: a781d2cf-55fe-4373-9cf1-b732864244e0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6078f4dae6bc6fb53dfa8b612972e28edd820f72
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62554759"
---
# <a name="exe"></a>Exe
Genel kapsam .exe veya .dll dosyasının temsil ettiğinden yalnızca olmadan bir sözcük sembol veya üst sınıf açılan bir Exe dosyasıdır. Yalnızca bir simgeyle yoktur `SymTagExe` dosya başına etiket. [Idiasession::get_globalscope](../../debugger/debug-interface-access/idiasession-get-globalscope.md) sembol yöntemi döndürür.

## <a name="properties"></a>Özellikler
 Aşağıdaki tabloda bu sembol türü için geçerli olan özellikleri gösterir.

|Özellik|Veri türü|Açıklama|
|--------------|---------------|-----------------|
|[IDiaSymbol::get_age](../../debugger/debug-interface-access/idiasymbol-get-age.md)|`DWORD`|Bu yürütülebilir dosyanın yaşı.|
|[IDiaSymbol::get_guid](../../debugger/debug-interface-access/idiasymbol-get-guid.md)|`GUID`|`GUID` Bu, yürütülebilir.|
|[IDiaSymbol::get_isCTypes](../../debugger/debug-interface-access/idiasymbol-get-isctypes.md)|`BOOL`|`TRUE` Sembol dosyası ile ilişkili ise bu yürütülebilir dosya (yalnızca DIA SDK v8.0 veya üzeri sürümlerde) C türleri içerir.|
|[IDiaSymbol::get_isStripped](../../debugger/debug-interface-access/idiasymbol-get-isstripped.md)|`BOOL`|`TRUE` Bu yürütülebilir (yalnızca DIA SDK v8.0 veya üzeri) ile ilişkili simge dosyasından özel semboller gizlenmiştir durumunda.|
|[IDiaSymbol::get_machineType](../../debugger/debug-interface-access/idiasymbol-get-machinetype.md)|`DWORD`|Hedef CPU belirten değer (biri [CV_CPU_TYPE_e numaralandırması](../../debugger/debug-interface-access/cv-cpu-type-e.md) değerler).|
|[IDiaSymbol::get_name](../../debugger/debug-interface-access/idiasymbol-get-name.md)|`BSTR`|.Exe dosyasının adı.|
|[IDiaSymbol::get_signature](../../debugger/debug-interface-access/idiasymbol-get-signature.md)|`DWORD`|Yürütülebilir dosya imzası.|
|[IDiaSymbol::get_symbolsFileName](../../debugger/debug-interface-access/idiasymbol-get-symbolsfilename.md)|`BSTR`|.Exe dosyasının .pdb veya .dbg dosyasının tam yolu.|
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol-get-symindexid.md)|`DWORD`|Sembol, dizin kimliği.|
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)|`DWORD`|Döndürür `SymTagExe` (biri [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) değerler).|

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSession::get_globalScope](../../debugger/debug-interface-access/idiasession-get-globalscope.md)
- [Simge Türlerinin Sözcük Hiyerarşisi](../../debugger/debug-interface-access/lexical-hierarchy-of-symbol-types.md)