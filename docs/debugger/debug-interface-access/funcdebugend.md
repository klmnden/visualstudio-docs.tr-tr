---
title: FuncDebugEnd | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- FuncDebugEnd symbol
- debugging [DIA SDK], end point
ms.assetid: 68f84fff-7cd3-4636-b929-7063a45009f8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1069d1a5f565d55fdb51d398087bd965933b6845
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62554648"
---
# <a name="funcdebugend"></a>FuncDebugEnd
Tanımlı bir noktada bir işlevi varsa, hangi hata ayıklama sona erdirmek için hata ayıklama başlangıç noktası ile bir simge ile tanımlanan bir `SymTagFuncDebugEnd` etiketi.

## <a name="properties"></a>Özellikler
 Aşağıdaki tabloda bu sembol türü için geçerli olan özellikleri gösterir.

|Özellik|Veri türü|Açıklama|
|--------------|---------------|-----------------|
|[IDiaSymbol::get_addressOffset](../../debugger/debug-interface-access/idiasymbol-get-addressoffset.md)|`DWORD`|Uzaklık bölümü konumunun; Ayrıntılar için bkz [LocationType numaralandırması](../../debugger/debug-interface-access/locationtype.md).|
|[IDiaSymbol::get_addressSection](../../debugger/debug-interface-access/idiasymbol-get-addresssection.md)|`DWORD`|Konum, bölüm parçası; Ayrıntılar için bkz [LocationType numaralandırması](../../debugger/debug-interface-access/locationtype.md).|
|[IDiaSymbol::get_customCallingConvention](../../debugger/debug-interface-access/idiasymbol-get-customcallingconvention.md)|`BOOL`|`TRUE` işlev özel bir çağırma kuralı (yalnızca DIA SDK V8.0 veya üzeri) kullanıyorsa.|
|[IDiaSymbol::get_farReturn](../../debugger/debug-interface-access/idiasymbol-get-farreturn.md)|`BOOL`|`TRUE` (yalnızca DIA SDK V8.0 veya üzeri sürümlerde) işlevi çok dönüş gerçekleştirir.|
|[IDiaSymbol::get_interruptReturn](../../debugger/debug-interface-access/idiasymbol-get-interruptreturn.md)|`BOOL`|`TRUE` işlev kesme (yalnızca DIA SDK V8.0 veya üzeri sürümlerde) geri döndürme içeriyorsa.|
|[IDiaSymbol::get_isStatic](../../debugger/debug-interface-access/idiasymbol-get-isstatic.md)|`BOOL`|`TRUE` işlev (yalnızca DIA SDK V8.0 veya üzeri sürümlerde) statik ise.|
|[IDiaSymbol::get_lexicalParent](../../debugger/debug-interface-access/idiasymbol-get-lexicalparent.md)|`IDiaSymbol*`|Kapsayan işlevin simgesi.|
|[IDiaSymbol::get_lexicalParentId](../../debugger/debug-interface-access/idiasymbol-get-lexicalparentid.md)|`DWORD`|Sözcük üst simge kimliği.|
|[IDiaSymbol::get_locationType](../../debugger/debug-interface-access/idiasymbol-get-locationtype.md)|`DWORD`|Uç noktaları statik konumuna sahip; Ayrıntılar için bkz [simge konumları](../../debugger/debug-interface-access/symbol-locations.md).|
|[IDiaSymbol::get_noInline](../../debugger/debug-interface-access/idiasymbol-get-noinline.md)|`BOOL`|`TRUE` işlevi ile belirtilmişse [noinline](/cpp/cpp/noinline) özniteliği (yalnızca DIA SDK V8.0 veya üzeri).|
|[IDiaSymbol::get_noReturn](../../debugger/debug-interface-access/idiasymbol-get-noreturn.md)|`BOOL`|`TRUE` işlevi ile belirtilmişse [noreturn](/cpp/cpp/noreturn) özniteliği (yalnızca DIA SDK V8.0 veya üzeri).|
|[IDiaSymbol::get_notReached](../../debugger/debug-interface-access/idiasymbol-get-notreached.md)|`BOOL`|`TRUE` işlev hiçbir zaman (yalnızca DIA SDK V8.0 veya üzeri sürümlerde) çağrılırsa.|
|[IDiaSymbol::get_offset](../../debugger/debug-interface-access/idiasymbol-get-offset.md)|`LONG`|Bellekte simgenin uzaklığı; Ayrıntılar için bkz [LocationType numaralandırması](../../debugger/debug-interface-access/locationtype.md), `LocIsRegRel`.|
|[IDiaSymbol::get_optimizedCodeDebugInfo](../../debugger/debug-interface-access/idiasymbol-get-optimizedcodedebuginfo.md)|`BOOL`|`TRUE` işlev (yalnızca DIA SDK V8.0 veya üzeri sürümlerde) en iyi duruma getirilmiş kod için hata ayıklama bilgisi varsa.|
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol-get-symindexid.md)|`DWORD`|Sembol, dizin kimliği.|
|[IDiaSymbol::get_relativeVirtualAddress](../../debugger/debug-interface-access/idiasymbol-get-relativevirtualaddress.md)|`DWORD`|Alt modül içinde bu işlevin sonuna göreli konumu.|
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)|`DWORD`|Döndürür `SymTagFuncDebugEnd` (biri [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) değerler).|
|[IDiaSymbol::get_virtualAddress](../../debugger/debug-interface-access/idiasymbol-get-virtualaddress.md)|`ULONGLONG`|Bu işlev için yürütülebilir görüntü içindeki konumu.|

## <a name="see-also"></a>Ayrıca Bkz.
- [Simge Türlerinin Sözcük Hiyerarşisi](../../debugger/debug-interface-access/lexical-hierarchy-of-symbol-types.md)
- [LocationType Numaralandırması](../../debugger/debug-interface-access/locationtype.md)
- [Simge Konumları](../../debugger/debug-interface-access/symbol-locations.md)