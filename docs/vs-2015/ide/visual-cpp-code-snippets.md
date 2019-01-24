---
title: Visual C++ kod parçacıkları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: 74e26fd4-e5ca-4611-a816-0a521b4947a0
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: cd24ef7e852d84d3213e024e53e325c0ba1d59fb
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54762085"
---
# <a name="visual-c-code-snippets"></a>Visual C++ kod parçacıkları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio'da kod parçacıkları, kod sık kullanılan C++ kod dosyalarınızı eklemek için kullanabilirsiniz. Genel olarak, çok aynı şekilde olduğu gibi C# kod parçacıkları kullanabilirsiniz, ancak varsayılan kod parçacıkları kümesini farklıdır.  
  
 Bir kod parçacığı belirli bir konumda kodunuza (ekleme) ekleyin veya bir kod parçacığı ile seçilen kod çevreleyen.  
  
## <a name="inserting-a-code-snippet"></a>Kod parçacığını eklemek  
 Kod parçacığı eklemek için bir C++ kod dosyası (.cpp veya .h) açın, içinde dosya bir yere tıklayın ve aşağıdakilerden birini yapın:  
  
- Bağlam menüsü alma ve seçmek için sağ tıklama **kod parçacığı Ekle**  
  
- İçinde **Düzenle / IntelliSense** menüsünde **kod parçacığı Ekle**  
  
- Kısayol tuşlarını kullanın: **CTRL + K + X**  
  
  Sürümünden itibaren seçenekleri listesini görmelisiniz **#if**. Seçtiğinizde, **#if**, dosyaya eklenen aşağıdaki kodu görmeniz gerekir:  
  
```cpp  
#if 0  
  
#endif // 0  
```  
  
 0 ile doğru koşul daha sonra değiştirebilirsiniz.  
  
## <a name="using-a-code-snippet-to-surround-selected-code"></a>Kod kapsamak için kod parçacığını kullanarak seçili  
 Seçili kod kapsamak için kod parçacığı kullanmak için bir satır (veya birden fazla satır) seçin ve aşağıdakilerden birini yapın:  
  
1. Bağlam menüsü alma ve seçmek için sağ tıklama **Surround With**  
  
2. İçinde **Düzenle / IntelliSense** menüsünde **Surround With**  
  
3. Kısayol tuşlarını kullanın: **CTRL + K + S**  
  
   Seçin **#if**. Bunun gibi bir şey görmeniz gerekir:  
  
```cpp  
#if 0  
#include "pch.h"  // or whatever line you had selected  
#endif // 0  
```  
  
 0 ile doğru koşul daha sonra değiştirebilirsiniz.  
  
## <a name="where-can-i-find-a-complete-list-of-the-c-code-snippets"></a>C++ kod parçacıkları tam bir listesini nerede bulabilirim?  
 Sayfasına gidip C++ kod parçacıkları tam listesini bulabilirsiniz **kod parçacıkları Yöneticisi** (üzerinde **Araçları** menüsü) ve ayarı **dil** için **Visual C++** . Penceresinde **Visual C++**. Alfabetik sırada tüm C++ kod parçacıkları adını görmeniz gerekir.  
  
 Çoğu kod parçacıkları adlarını anlamı kolayca anlaşılır ancak bazı adları kafa karıştırıcı.  
  
## <a name="class-vs-classi"></a>Classi sınıfı  
 **Sınıfı** kod parçacığı uygun varsayılan oluşturucu ve yıkıcı, oluşturucu ve yıkıcı tanımlarını sınıfı dışında bulunduğu yere MyClass, adında bir sınıf tanımı sağlar:  
  
```cpp  
class MyClass  
{  
public:  
MyClass();  
~MyClass();  
  
private:  
  
};  
  
MyClass::MyClass()  
{  
}  
  
MyClass::~MyClass()  
{  
}  
```  
  
 Classi kod parçacığı da MyClass adlı bir sınıf tanımı sağlar ancak varsayılan oluşturucu ve yıkıcı sınıf tanımının içinde tanımlanır:  
  
```cpp  
class MyClass  
{  
public:  
MyClass()  
{  
}  
  
~MyClass()  
{  
}  
  
private:  
  
};  
```  
  
## <a name="for-vs-foreach-vs-forr-vs-rfor"></a>İçin foreach forr vs rfor karşılaştırması karşılaştırması  
 Vardır dört farklı sağlayan kod parçacıkları için farklı, döngüler için.  
  
 **İçin** kod parçacığı sağlayan bir `for` Döngü koşulu uzunluğuna dayalıdır (içinde `size_t`) bir nesnenin:  
  
```cpp  
for (size_t i = 0; i < length; i++)  
{  
  
}  
```  
  
 **Foreach** kod parçacığı sağlayan bir `for each` bir koleksiyonun üyelerini yineleme döngüsü:  
  
```cpp  
for each (object var in collection_to_loop)  
{  
  
}  
```  
  
 **Forr** kod parçacığı sağlar ters `for` Döngü koşulu uzunluğu nesnenin üzerinde (tamsayı) dayanır:  
  
```cpp  
for (int i = length - 1; i >= 0; i--)  
{  
  
}  
```  
  
 **Rfor** kod parçacığı sağlayan bir [aralık tabanlı](http://msdn.microsoft.com/library/5750ba1d-ba48-4236-a923-e32de8345c2d) for döngüsü (bağlantı):  
  
```cpp  
for (auto& i : v)  
{  
  
}  
```  
  
## <a name="the-destructor-snippet-"></a>Yıkıcı kod parçacığını (~)  
 Yıkıcı kod parçacığını (**~**) farklı bağlamda farklı bir davranış gösterir. Bu kod parçacığı bir sınıf içinde eklerseniz, o sınıf için yok edici sağlar. Örneğin, aşağıdaki kod verilen:  
  
```cpp  
class SomeClass {  
  
};  
```  
  
 Yıkıcı kod parçacığını eklemek, bir yok edici için SomeClass sağlar:  
  
```cpp  
class SomeClass {  
    ~SomeClass()  
    {  
  
    }  
};  
```  
  
 Sınıf dışındaki yok Edicisi parçacığı eklemeye çalışırsanız, bir yer tutucu adıyla bir yok edici sağlar:  
  
```cpp  
~TypeNamePlaceholder()  
{  
  
```
