---
title: Simge türlerinin sözcük hiyerarşisi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- symbols [DIA SDK], type hierarchies
ms.assetid: 912da653-ddfe-45a4-84aa-64281283739a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f4b2e6fc0b24cc96f617e7b78c6bdcc59ddc5c0d
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63399378"
---
# <a name="lexical-hierarchy-of-symbol-types"></a>Simge Türlerinin Sözcük Hiyerarşisi
Aşağıdaki tabloda, sözcük hiyerarşisi içinde Sembol türleri gösterilmektedir.

## <a name="symbol-types"></a>Sembol türleri

|Simge türü|Açıklama|
|-----------------|-----------------|
|[Ek Açıklama](../../debugger/debug-interface-access/annotation.md)|Program kodunda ek açıklamalı bir konumu belirtir.|
|[Block](../../debugger/debug-interface-access/block.md)|İç içe kapsamları işlevlerde belirtir.|
|`Compiland`|Belirtir bir `compiland` .exe dosyasına bağlanır.|
|[CompilandDetails](../../debugger/debug-interface-access/compilanddetails.md)|Ek derlenecek ayrıntıları yükleniyor gerektirir ve bu nedenle almak için çalışma zamanı yükü tabi derlenecek veri belirtir.|
|[CompilandEnv](../../debugger/debug-interface-access/compilandenv.md)|Derlenecek derlenmesi için önemli olan tüm ek ortam değişkenlerini belirtir.|
|[Özel (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/custom-debug-interface-access-sdk.md)|Kullanıcı tanımlı bir sembol belirtir.|
|[Veriler (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/data-debug-interface-access-sdk.md)|Bu değişkenleri parametreleri, yerel değişkenler, genel değişkenler ve sınıf üyeleri belirtir.|
|[Exe](../../debugger/debug-interface-access/exe.md)|Genel kapsamdaki verileri belirtir. Tüm bir .exe veya .dll dosyasına karşılık gelir.|
|[FuncDebugEnd](../../debugger/debug-interface-access/funcdebugend.md)|Tanımlı bir noktasında, bir işlevi belirtir sonlandırmak için hangi hata ayıklama sırasında değildir.|
|[FuncDebugStart](../../debugger/debug-interface-access/funcdebugstart.md)|Tanımlı bir noktasında, bir işlevi belirtir. başlamak için hangi hata ayıklama sırasında değildir.|
|[İşlev (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/function-debug-interface-access-sdk.md)|Bir işlevi belirtir.|
|[Etiket (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/label-debug-interface-access-sdk.md)|Program kodunda bir konumu belirtir.|
|[PublicSymbol](../../debugger/debug-interface-access/publicsymbol.md)|Yürütülebilir program oluşturma sırasında görüntülenen bir dış bir sembol belirtir.|
|[Dönüştürücü](../../debugger/debug-interface-access/thunk.md)|Belirtir bir `thunk`.|
|[UsingNameSpace](../../debugger/debug-interface-access/usingnamespace.md)|Belirtir bir `namespace`tanımlayıcısı.|

> [!NOTE]
> Ek Sembol Özellikleri sembol türüne bağlı olarak kullanılabilir. Bu özellikleri tek tek sembol konularında listelenmiştir.

## <a name="see-also"></a>Ayrıca Bkz.
- [Simge Türlerinin Sınıf Hiyerarşisi](../../debugger/debug-interface-access/class-hierarchy-of-symbol-types.md)
- [IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)
- [Simgeler ve Simge Etiketleri](../../debugger/debug-interface-access/symbols-and-symbol-tags.md)
- [SymTagEnum Numaralandırması](../../debugger/debug-interface-access/symtagenum.md)