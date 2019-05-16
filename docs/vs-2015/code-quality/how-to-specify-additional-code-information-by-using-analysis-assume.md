---
title: 'Nasıl yapılır: __Analysis_assume kullanarak ek kod bilgileri belirtme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
f1_keywords:
- __analysis_assume
helpviewer_keywords:
- __analysis_assume
ms.assetid: 51205d97-4084-4cf4-a5ed-3eeaf67deb1b
caps.latest.revision: 12
author: mikeblome
ms.author: mblome
manager: jillfra
ms.openlocfilehash: dfae7d858dbb462ec6a93de9eb63b1b3b2a711ab
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65685816"
---
# <a name="how-to-specify-additional-code-information-by-using-analysisassume"></a>Nasıl yapılır: __analysis_assume Kullanarak Ek Kod Bilgileri Belirtme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Analiz işlemine yardımcı olmak ve Uyarıları azaltmak C/C++ kodu için kod analizi aracı için ipuçları sağlar. Ek bilgi sağlamak için aşağıdaki işlevi kullanın:  
  
 `__analysis_assume(`  `expr`  `)`  
  
 `expr` -herhangi bir ifade doğru olarak değerlendirilebilmesi için kabul edilir.  
  
 Kod Analizi aracı ifade tarafından temsil edilen koşul true işlevi burada görünür ve ifade, örneğin, bir değişkene atama ile değiştirilinceye kadar doğrudur noktada olduğunu varsayar.  
  
> [!NOTE]
> `__analysis_assume` kod iyileştirme etkilemez. Kod Analizi aracı dışında `__analysis_assume` bir İşlemsiz tanımlanır.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod `__analysis_assume` Kod Analizi uyarısı düzeltmek için [C6388](../code-quality/c6388.md):  
  
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
  __analysis_assume(pc == NULL);   
  f(pc);  
}  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [__assume](https://msdn.microsoft.com/library/d8565123-b132-44b1-8235-5a8c8bff85a7)
