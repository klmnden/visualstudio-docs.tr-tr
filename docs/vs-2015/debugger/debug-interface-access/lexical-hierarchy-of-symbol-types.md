---
title: Simge türlerinin sözcük hiyerarşisi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- symbols [DIA SDK], type hierarchies
ms.assetid: 912da653-ddfe-45a4-84aa-64281283739a
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: dac4ae8357d62813abb3f4735ec6e1f8b552d324
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54797485"
---
# <a name="lexical-hierarchy-of-symbol-types"></a>Simge Türlerinin Sözcük Hiyerarşisi
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

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
>  Ek Sembol Özellikleri sembol türüne bağlı olarak kullanılabilir. Bu özellikleri tek tek sembol konularında listelenmiştir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Simge türlerinin sınıf hiyerarşisi](../../debugger/debug-interface-access/class-hierarchy-of-symbol-types.md)   
 [Idiasymbol::get_symtag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)   
 [Simgeler ve simge etiketleri](../../debugger/debug-interface-access/symbols-and-symbol-tags.md)   
 [SymTagEnum Numaralandırması](../../debugger/debug-interface-access/symtagenum.md)
