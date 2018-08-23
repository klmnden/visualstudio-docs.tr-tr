---
title: 'CA1024: uygun yerlerde özellikler kullan | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- UsePropertiesWhereAppropriate
- CA1024
helpviewer_keywords:
- CA1024
- UsePropertiesWhereAppropriate
ms.assetid: 3a04f765-af7c-4872-87ad-9cc29e8e657f
caps.latest.revision: 23
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: f6aeca146fe7611d789ff08c1eda84687d691e5b
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42686129"
---
# <a name="ca1024-use-properties-where-appropriate"></a>CA1024: Uygun yerlerde özellikler kullan
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu konuda en son sürümünü şu yolda bulunabilir: [CA1024: uygun yerlerde özellikler kullan](https://docs.microsoft.com/visualstudio/code-quality/ca1024-use-properties-where-appropriate).  
  
TypeName | UsePropertiesWhereAppropriate |  
| Checkıd | CA1024 |  
| Kategori | Microsoft.Design|  
| Yeni değişiklik | Bozucu |  
  
## <a name="cause"></a>Sebep  
 Ortak veya korumalı yöntem ile başlayan bir ada sahip `Get`hiçbir parametre almaz ve dizi olmayan bir değer döndürür.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Çoğu durumda veri özelliklerini temsil eder ve yöntemleri eylemleri gerçekleştirebilirsiniz. Özellikler, bunları kullanmayı kolaylaştırır alanları gibi erişilir. Bir yöntem, Bu koşullardan biri varsa özellik olmak için iyi bir adaydır:  
  
-   Hiçbir bağımsız değişkeni alır ve bir nesnenin durum bilgilerini döndürür.  
  
-   Bir nesnenin durumu kısmı ayarlamak için tek bir bağımsız değişken kabul eder.  
  
 Özellikleri, alanları ise olarak hareket etmesi gerektiğini; yöntem çözemezseniz, bir özelliğe değiştirilmemelidir. Aşağıdaki durumlarda özelliklerini daha iyi yöntemler şunlardır:  
  
-   Yöntem, zaman alıcı bir işlem gerçekleştirir. Yöntemi, perceivably ayarlamak veya bir alanın değerini almak için gereken süreden daha yavaştır.  
  
-   Bir dönüştürme yöntemi gerçekleştirir. Bir alana erişim depoladığı verilerin dönüştürülmüş bir sürümünü döndürmez.  
  
-   Get yöntemi gözlemlenebilir bir yan etkisi vardır. Bir alanın değerini alma yan etkileri üretmez.  
  
-   Yürütme sırası önemlidir. Bir alanın değerini ayarlama, diğer işlemleri oluşması bağımlı kalmayacak.  
  
-   Yöntemi, art arda iki kez çağırmak farklı sonuçlar oluşturur.  
  
-   Yöntem statik olsa da arayan tarafından değiştirilebilen bir nesne döndürür. Bir alanın değerini alma alanı tarafından depolanan verileri değiştirmek çağıranın izin vermez.  
  
-   Yöntemi, bir dizi döndürür.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Bu kural ihlalini düzeltmek için yöntem bir özelliğini değiştirin.  
  
## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında  
 Yöntem en az bir tanesi yukarıda listelenen ölçütlerini karşılıyorsa bu kuraldan bir uyarıyı gizler.  
  
## <a name="controlling-property-expansion-in-the-debugger"></a>Hata ayıklayıcısı özellik genişletme denetleme  
 Programcıların bir özelliğini kullanmaktan nedenlerinden biri, otomatik-genişletmek için hata ayıklayıcı istemediğiniz olmasıdır. Örneğin, özellik, büyük nesne ayırma veya P/Invoke çağırma gerektirebilir, ancak gözlemlenebilir bir yan etkileri gerçekten olmayabilir.  
  
 Hata ayıklayıcı otomatik-aşmasını önlemek özellikler uygulayarak <xref:System.Diagnostics.DebuggerBrowsableAttribute?displayProperty=fullName>. Aşağıdaki örnek, bir örnek özelliğine uygulanan bu özniteliği gösterir.  
  
```vb  
Imports System   
Imports System.Diagnostics   
  
Namespace Microsoft.Samples   
  
    Public Class TestClass   
  
        ' [...]   
  
        <DebuggerBrowsable(DebuggerBrowsableState.Never)> _   
        Public ReadOnly Property LargeObject() As LargeObject   
            Get   
                ' Allocate large object   
                ' [...]   
            End Get   
        End Property   
  
    End Class   
  
End Namespace  
```  
  
```csharp  
  
      using System;   
using System.Diagnostics;   
  
namespace Microsoft.Samples   
{   
    publicclass TestClass   
    {   
        // [...]   
  
        [DebuggerBrowsable(DebuggerBrowsableState.Never)]   
        public LargeObject LargeObject   
        {   
            get   
            {   
                // Allocate large object   
                // [...]   
  
        }  
    }  
}  
```  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, özelliklerine dönüştürülmesi gerektiğini ve değil gibi alanlarını davranmayabilir olduğundan, birkaç gereken çeşitli yöntemler içerir.  
  
 [!code-csharp[FxCop.Design.MethodsProperties#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.MethodsProperties/cs/FxCop.Design.MethodsProperties.cs#1)]


