---
title: 'Nasıl yapılır: __Analysis_assume Kullanarak Ek Kod Bilgileri Belirtme'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- _Analysis_assume
helpviewer_keywords:
- _Analysis_assume
ms.assetid: 51205d97-4084-4cf4-a5ed-3eeaf67deb1b
author: mikeblome
ms.author: mblome
manager: wpickett
ms.workload:
- multiple
ms.openlocfilehash: 25ce2a97acd248e546fdfab1a1b5c3f22e085f0c
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63403116"
---
# <a name="how-to-specify-additional-code-information-by-using-analysisassume"></a>Nasıl yapılır: __Analysis_assume Kullanarak Ek Kod Bilgileri Belirtme
Analiz işlemine yardımcı olmak ve Uyarıları azaltmak C/C++ kodu için kod analizi aracı için ipuçları sağlar. Ek bilgi sağlamak için aşağıdaki işlevi kullanın:

 `_Analysis_assume(`  `expr`  `)`

 `expr` -herhangi bir ifade doğru olarak değerlendirilebilmesi için kabul edilir.

 Kod Analizi aracı ifade tarafından temsil edilen koşul true işlevi burada görünür ve ifade, örneğin, bir değişkene atama ile değiştirilinceye kadar doğrudur noktada olduğunu varsayar.

> [!NOTE]
> `_Analysis_assume` kod iyileştirme etkilemez. Kod Analizi aracı dışında `_Analysis_assume` bir İşlemsiz tanımlanır.

## <a name="example"></a>Örnek
 Aşağıdaki kod `_Analysis_assume` Kod Analizi uyarısı düzeltmek için [C6388](../code-quality/c6388.md):

```
#include<windows.h>
#include<codeanalysis\sourceannotations.h>

using namespace vc_attributes;

// calls free and sets ch to null
void FreeAndNull(char* ch);

//requires pc to be null
void f([Pre(Null=Yes)] char* pc);

void test( )
{
  char *pc = (char*)malloc(5);
  FreeAndNull(pc);
  _Analysis_assume(pc == NULL);
  f(pc);
}
```

## <a name="see-also"></a>Ayrıca Bkz.
 [__assume](/cpp/intrinsics/assume)