---
title: Erişim İhlalinde Nasıl Hata Ayıklayabilirim? | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.access
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- access violation debugging
- debugging [Visual Studio], access violations
ms.assetid: 9311d754-0ce9-4145-b147-88b6ca77ba63
caps.latest.revision: 21
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 073fc84d15cb31b4f7a4cc635524ab08a724911e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68147835"
---
# <a name="how-can-i-debug-an-access-violation"></a>Erişim İhlalinde Nasıl Hata Ayıklayabilirim?
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Sorun açıklaması  
 Kendi programımı bir erişim ihlali üretir. Bu sorunu nasıl ayıklayabilirim?  
  
## <a name="solution"></a>Çözüm  
 Birden çok işaretçi başvuru kod satırında bir erişim ihlali alırsanız, hangi işaretçi erişim ihlaline neden olduğunu bulmak zor olabilir. Visual Studio 2015 güncelleştirme 1'de başlayarak, özel durum iletişim kutusunda artık açıkça erişim ihlaline neden işaretçi adları.  
  
 Örneğin, aşağıdaki kodu göz önünde bulundurulduğunda, bir erişim ihlali almanız gerekir:  
  
```cpp  
#include <iostream>  
using namespace std;  
  
class ClassB {  
public:  
      ClassC* C;  
      ClassB() {  
            C = new ClassC();  
      }  
     void printHello() {  
            cout << "hello world";  
      }  
};  
  
class ClassA {  
public:  
    ClassB* B;  
    ClassA() {  
            B = nullptr;  
      }  
};  
  
int main() {  
    ClassA* A = new ClassA();  
    A->B->printHello();  
}  
```  
  
 Visual Studio 2015 güncelleştirme 1'de bu kodu çalıştırırsanız, aşağıdaki özel durum iletişim kutusunu görmeniz gerekir:  
  
 ![AccessViolationCPlus](../debugger/media/accessviolationcplus.png "AccessViolationCPlus")  
  
 İşaretçi erişim ihlaline neden neden belirleyemiyorsa, soruna işaretçi doğru şekilde atandığını emin olmak için kod boyunca izleme.  Bir parametre olarak geçirilir, doğru geçirilir ve yanlışlıkla oluşturma olmayan emin bir [yüzeysel kopya](http://stackoverflow.com/questions/184710/what-is-the-difference-between-a-deep-copy-and-a-shallow-copy). Ardından değerlerini istemeden yere programda veri kesme noktası işaretçisi, başka bir yerde programda değiştirilen olmadığından emin olmak için söz konusu oluşturarak değiştirilmekte olan değil olduğunu doğrulayın. Veri kesme noktaları hakkında daha fazla bilgi için bkz: veri kesme noktası bölümünde [kullanılarak kesme noktaları](../debugger/using-breakpoints.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yerel Kodda Hata Ayıklama SSS](../debugger/debugging-native-code-faqs.md)
