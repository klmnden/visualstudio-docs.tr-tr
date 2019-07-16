---
title: 'CA1062: Genel yöntemlerin bağımsız değişkenlerini doğrulayın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1062
- ValidateArgumentsOfPublicMethods
- Validate arguments of public methods
helpviewer_keywords:
- CA1062
- ValidateArgumentsOfPublicMethods
ms.assetid: db1f69ca-68f7-477e-94f3-d135cc5dfcbc
caps.latest.revision: 29
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 13ea687ea9ca68693af7e2aa5c22881a36207d2e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68200441"
---
# <a name="ca1062-validate-arguments-of-public-methods"></a>CA1062: Genel metotların bağımsız değişkenlerini doğrulayın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|ValidateArgumentsOfPublicMethods|
|CheckId|CA1062|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Dışarıdan görünen bir yöntem başvuru bağımsız değişkenlerinden biri, bağımsız değişkenin olup olmadığını doğrulamadan başvurusunu `null` (`Nothing` Visual Basic'te).

## <a name="rule-description"></a>Kural Tanımı
 Dışarıdan görünen yöntemlere geçirilen tüm başvuru bağımsız değişkenleri karşı denetlenmesi `null`. Uygunsa, throw bir <xref:System.ArgumentNullException> bağımsız değişken olduğunda `null`.

 Ortak veya korumalı olarak bildirildiğinden, bilinmeyen bir derlemeden bir yöntem çağrılabilir, yöntemin tüm parametreleri doğrulamalıdır. Yalnızca bilinen derlemeler tarafından çağrılacak yöntem tasarlanmışsa, yöntemin iç yapmanız ve uygulama gerekir <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> yöntemi içeren derlemeye özniteliği.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için her başvuru bağımsız değişkeni karşı doğrulama `null`.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Başvurusu kaldırılmış parametresi işlevdeki başka bir yöntem çağrısı tarafından doğrulanmıştır eminseniz bu kuraldan bir uyarıyı gösterilmemesini sağlayabilirsiniz.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, kuralını ihlal eden bir yöntem ve kural karşılayan bir yöntemi gösterir.

 [!code-csharp[FxCop.Design.ValidateArguments#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.ValidateArguments/cs/fxcop.design.validatearguments.copyctors.cs#1)]
 [!code-csharp[FxCop.Design.ValidateArguments#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.ValidateArguments/cs/FxCop.Design.ValidateArguments.cs#1)]
 [!code-vb[FxCop.Design.ValidateArguments#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.ValidateArguments/vb/FxCop.Design.ValidateArguments.vb#1)]

## <a name="example"></a>Örnek
 İçinde [!INCLUDE[vsprvslong](../includes/vsprvslong-md.md)], bu kural parametre doğrulama yapan başka bir yönteme geçirilen algılamaz.

 [!code-csharp[FxCop.Design.ValidateArguments#2](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.ValidateArguments/cs/fxcop.design.validatearguments.copyctors.cs#2)]
 [!code-csharp[FxCop.Design.ValidateArguments#2](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.ValidateArguments/cs/FxCop.Design.ValidateArguments.cs#2)]
 [!code-vb[FxCop.Design.ValidateArguments#2](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.ValidateArguments/vb/FxCop.Design.ValidateArguments.vb#2)]

## <a name="example"></a>Örnek
 Kopya oluşturucuları, alan veya başvuru nesneleri olan özellikleri de CA1062 kuralı ihlal edebilir. Kopya oluşturucuya geçirilen kopyalanan nesne olabileceğinden ihlali meydana `null` (`Nothing` Visual Basic'te). İhlali gidermek için kopyalanan nesnenin null olup olmadığını denetleyin için bir statik (Visual Basic'te Shared) yöntemi kullanın.

 Aşağıdaki `Person` sınıfı örneği `other` geçirilen nesne `Person` kopya Oluşturucu olabilir `null`.

```

public class Person
{
    public string Name { get; private set; }
    public int Age { get; private set; }

    public Person(string name, int age)
    {
        Name = name;
        Age = age;
    }

    // Copy constructor CA1062 fires because other is dereferenced
    // without being checked for null
    public Person(Person other)
        : this(other.Name, other.Age)
    {
    }
}
```

## <a name="example"></a>Örnek
 Aşağıdaki düzenlendi `Person` örnek, `other` kopya oluşturucusuna geçirilen nesne null işaretli ilk `PassThroughNonNull` yöntemi.

```
public class Person
{
    public string Name { get; private set; }
    public int Age { get; private set; }

    public Person(string name, int age)
    {
        Name = name;
        Age = age;
    }

    // Copy constructor
    public Person(Person other)
        : this(PassThroughNonNull(other).Name,
          PassThroughNonNull(other).Age)
    {
    }

    // Null check method
    private static Person PassThroughNonNull(Person person)
    {
        if (person == null)
            throw new ArgumentNullException("person");
        return person;
    }
}
```
