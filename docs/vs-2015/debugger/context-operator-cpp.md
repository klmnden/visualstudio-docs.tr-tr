---
title: Bağlam işleci (C++) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.operators
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- expressions [C++], native debugger
- evaluation
- format specifiers, expressions
- context operator, in expressions
- debugging [C++], expressions
- native expression evaluator
ms.assetid: 73cc9afe-f4a4-474e-bb89-5a33fb5e570c
caps.latest.revision: 29
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: f6351dd9db7e6f8f29bdd15f376f84511c64bfe7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68161532"
---
# <a name="context-operator-c"></a>Bağlam İşleci (C++)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir kesme noktası konumu, değişken adı veya ifade nitelemek için C++'da şu içerik işlecini kullanabilirsiniz. Bağlam işleci, aksi takdirde yerel bir ad tarafından gizlenen bir dış kapsam adı belirtmek için kullanışlıdır.  
  
## <a name="BKMK_Using_context_operators_to_specify_a_symbol"></a> Söz dizimi  
 Bağlam belirtmenin iki yolu vardır:  
  
1. {, [*Modülü*]} *ifadesi*  
  
     Küme ayraçları iki virgül ve modül içermelidir (yürütülebilir veya DLL) adını veya tam yolu.  
  
     Örneğin, bir kesme noktasında ayarlanacak `SomeFunction` EXAMPLE.dll işlevi:  
  
    ```cpp  
    {,,EXAMPLE.dll}SomeFunction  
    ```  
  
2. *Modül*! *ifade*  
  
    ```cpp  
    EXAMPLE.dll!SomeFunction  
    ```  
  
- *Modül* bir modül adı. Aynı ada sahip modüller arasında ayırt etmek için bir tam yol kullanabilirsiniz.  
  
   Varsa *Modülü* yolu, virgül, katıştırılmış bir boşluk veya bir küme ayracı içerir, bağlam ayrıştırıcının dizesi düzgün tanıyabilmesi, yolu tırnak kullanmanız gerekir. Tek tırnak işaretleri çift tırnak işareti kullanmalısınız bir Windows dosya adının parçası olarak kabul edilir. Örneğin,  
  
  ```cpp  
  {,,"a long, long, library name.dll"} g_Var  
  ```  
  
- *ifade* işlev adı, değişken adı veya işaretçi adresi gibi geçerli bir hedef çözümler herhangi geçerli bir C++ ifadesi *Modülü*.  
  
  İfade değerlendirici bir ifadede bir sembol karşılaştığında sembolünün şu sırayla arar:  
  
1. Sözcük kapsamı geçerli blok küme ayraçları içine alındığına ve dışa doğru kapsayan bir blok ile devam bir deyimler serisini başlayarak dışa doğru. Geçerli blok yönerge işaretçisi adresi geçerli konumu içeren kodudur.  
  
2. İşlev kapsamı. Geçerli işlev.  
  
3. C++ üye işlevinin içerisinde geçerli konumu ise sınıf kapsamı. Sınıf kapsamı, tüm temel sınıflar içerir. İfade değerlendirici, normal baskınlık kurallarını kullanır.  
  
4. Genel semboller geçerli modül içinde.  
  
5. Ortak semboller geçerli programı.
