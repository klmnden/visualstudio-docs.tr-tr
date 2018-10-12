---
title: CompilandEnv | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- CompilandEnv symbol
ms.assetid: 808404bb-ece1-47f1-b9ea-c76d4d86ddd9
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3c0579595814e882cb7cab73cf7fd20ae6f267e2
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49199270"
---
# <a name="compilandenv"></a>CompilandEnv
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Derleyici simgelerle ek ortam değişkenleri içerebilir. Bir `SymTagCompilandEnv` her biri bu değişkenler için Sembol.  
  
## <a name="properties"></a>Özellikler  
 Aşağıdaki tabloda bu sembol türü için geçerli olan özellikleri gösterir.  
  
|Özellik|Veri türü|Açıklama|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_lexicalParent](../../debugger/debug-interface-access/idiasymbol-get-lexicalparent.md)|`IDiaSymbol*`|Üst derlenecek dosya simgesi.|  
|[IDiaSymbol::get_lexicalParentId](../../debugger/debug-interface-access/idiasymbol-get-lexicalparentid.md)|`DWORD`|Sözcük üst simge kimliği.|  
|[IDiaSymbol::get_name](../../debugger/debug-interface-access/idiasymbol-get-name.md)|`BSTR`|Değişkenin adı.|  
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol-get-symindexid.md)|`DWORD`|Sembol, dizin kimliği.|  
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)|`DWORD`|Döndürür `SymTagCompilandEnv` (biri [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) değerler).|  
|[IDiaSymbol::get_value](../../debugger/debug-interface-access/idiasymbol-get-value.md)|`VARIANT`|Değişken dize değerli içeriğini (`VT_BSTR`).|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Derlenecek](../../debugger/debug-interface-access/compiland.md)   
 [Simge Türlerinin Sözcük Hiyerarşisi](../../debugger/debug-interface-access/lexical-hierarchy-of-symbol-types.md)



