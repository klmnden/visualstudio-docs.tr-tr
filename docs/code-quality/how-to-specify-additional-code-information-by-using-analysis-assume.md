---
title: __Analysis_assume kullanmak için kod çözümleme ipuçları
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
ms.openlocfilehash: f23dd3821744687d4f595ad404bc076e1d05af7b
ms.sourcegitcommit: cc5fd59e5dc99181601b7db8b28d7f8a83a36bab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2019
ms.locfileid: "66835902"
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

```cpp
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

## <a name="see-also"></a>Ayrıca bkz.

- [__assume](/cpp/intrinsics/assume)
