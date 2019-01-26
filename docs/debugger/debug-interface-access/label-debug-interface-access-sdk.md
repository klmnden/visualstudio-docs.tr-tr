---
title: Etiket (hata ayıklama arabirimi Erişim SDK'sı) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- locations, in program code
- Label symbol
ms.assetid: 8cef7620-5bc8-4500-8bd0-e9e638bccb24
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6286f2973068fd39fe59c55e0af0464444a44aad
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54991963"
---
# <a name="label-debug-interface-access-sdk"></a>Etiket (Arabirim Erişimi SDK'sında Hata Ayıklama)
Program kodunda bir konum ile tanımlanan bir `SymTagLabel` sembol.  
  
## <a name="properties"></a>Özellikler  
 Aşağıdaki tabloda bu sembol türü için geçerli olan özellikleri gösterir.  
  
|Özellik|Veri türü|Açıklama|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_addressOffset](../../debugger/debug-interface-access/idiasymbol-get-addressoffset.md)|`DWORD`|Uzaklık bölümü konumunun; Ayrıntılar için bkz [LocationType numaralandırması](../../debugger/debug-interface-access/locationtype.md).|  
|[IDiaSymbol::get_addressSection](../../debugger/debug-interface-access/idiasymbol-get-addresssection.md)|`DWORD`|Konum, bölüm parçası; Ayrıntılar için bkz [LocationType numaralandırması](../../debugger/debug-interface-access/locationtype.md).|  
|[IDiaSymbol::get_customCallingConvention](../../debugger/debug-interface-access/idiasymbol-get-customcallingconvention.md)|`BOOL`|`TRUE` Etiket özel bir çağırma kuralı kullanıyorsa.|  
|[IDiaSymbol::get_farReturn](../../debugger/debug-interface-access/idiasymbol-get-farreturn.md)|`BOOL`|`TRUE` Etiket kadar dönüş uyguluyorsa.|  
|[IDiaSymbol::get_interruptReturn](../../debugger/debug-interface-access/idiasymbol-get-interruptreturn.md)|`BOOL`|`TRUE` Etiket kesme geri döndürme içeriyorsa.|  
|[IDiaSymbol::get_lexicalParent](../../debugger/debug-interface-access/idiasymbol-get-lexicalparent.md)|`IDiaSymbol*`|Kapsayan derlenecek, blok veya işlev simgesi.|  
|[IDiaSymbol::get_lexicalParentId](../../debugger/debug-interface-access/idiasymbol-get-lexicalparentid.md)|`DWORD`|Sözcük üst simge kimliği.|  
|[IDiaSymbol::get_locationType](../../debugger/debug-interface-access/idiasymbol-get-locationtype.md)|`DWORD`|Statik konumları etiketlere sahip; Ayrıntılar için bkz [simge konumları](../../debugger/debug-interface-access/symbol-locations.md) sabit listesi.|  
|[IDiaSymbol::get_name](../../debugger/debug-interface-access/idiasymbol-get-name.md)|`BSTR`|Etiketin adı.|  
|[IDiaSymbol::get_noInline](../../debugger/debug-interface-access/idiasymbol-get-noinline.md)|`BOOL`|`TRUE` Etiket ile belirtilmişse [noinline](/cpp/cpp/noinline) özniteliği.|  
|[IDiaSymbol::get_noReturn](../../debugger/debug-interface-access/idiasymbol-get-noreturn.md)|`BOOL`|`TRUE` Etiket ile belirtilmişse [noreturn](/cpp/cpp/noreturn) özniteliği.|  
|[IDiaSymbol::get_notReached](../../debugger/debug-interface-access/idiasymbol-get-notreached.md)|`BOOL`|`TRUE` Etiket hiçbir zaman çağrılırsa.|  
|[IDiaSymbol::get_offset](../../debugger/debug-interface-access/idiasymbol-get-offset.md)|`LONG`|Bellekte simgenin uzaklığı; Ayrıntılar için bkz [LocationType numaralandırması](../../debugger/debug-interface-access/locationtype.md), `LocIsRegRel`.|  
|[IDiaSymbol::get_optimizedCodeDebugInfo](../../debugger/debug-interface-access/idiasymbol-get-optimizedcodedebuginfo.md)|`BOOL`|`TRUE` kodu en iyi duruma getirilmiş kod için hata ayıklama bilgisi varsa.|  
|[IDiaSymbol::get_relativeVirtualAddress](../../debugger/debug-interface-access/idiasymbol-get-relativevirtualaddress.md)|`DWORD`|Bu etiket, modül içinde göreli konumu.|  
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol-get-symindexid.md)|`DWORD`|Sembol, dizin kimliği.|  
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)|`DWORD`|Döndürür `SymTagFuncDebugLabel` (biri [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) değerler).|  
|[IDiaSymbol::get_virtualAddress](../../debugger/debug-interface-access/idiasymbol-get-virtualaddress.md)|`ULONGLONG`|Bu etiketi içinde yürütülebilir resmin konumu.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Simge türlerinin sözcük hiyerarşisi](../../debugger/debug-interface-access/lexical-hierarchy-of-symbol-types.md)   
 [LocationType numaralandırması](../../debugger/debug-interface-access/locationtype.md)   
 [Simge Konumları](../../debugger/debug-interface-access/symbol-locations.md)