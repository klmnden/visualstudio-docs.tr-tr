---
title: Yeniden düzenlemesi (C#) parametreleri yeniden Sırala | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- vs.csharp.refactoring.reorder
dev_langs:
- CSharp
helpviewer_keywords:
- refactoring [C#], Reorder Parameters
- Reorder Parameters refactoring [C#]
ms.assetid: 4dabf21a-a9f0-41e9-b11b-55760cf2bd90
caps.latest.revision: 26
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: daf77a60256e59cabd176990f3642a2206a7f0d8
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63444543"
---
# <a name="reorder-parameters-refactoring-c"></a>Parametreleri Yeniden Sırala (C#) yeniden düzenlemesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

`Reorder Parameters` Visual C# parametreleri yöntemlerden, dizin oluşturucular ve temsilciler sırasını değiştirmek için kolay bir yol sağlayan işlemidir. `Reorder Parameters` bildirimi değiştirir ve burada üyenin çağrıldığı herhangi konumlarda parametreleri yeni sıralamasını yansıtacak şekilde düzenlenir.  
  
 Gerçekleştirilecek `Reorder Parameters` işlemi ya da bir yöntem, dizin oluşturucu veya temsilci yanındaki imleci yerleştirin. İmleç konumda olduğunda, çağırma `Reorder Parameters` klavye kısayol tuşuna basarak veya kısayol menüsünden komut tıklayarak işlemi.  
  
> [!NOTE]
> Genişletme yönteminin ilk parametre sıralayamazsınız.  
  
### <a name="to-reorder-parameters"></a>Parametreleri yeniden sıralamak için  
  
1. Adlı bir sınıf kitaplığı oluşturma `ReorderParameters`ve ardından `Class1` ile aşağıdaki kod örneği.  
  
    ```csharp  
    class ProtoClassA  
    {  
        // Invoke on 'MethodB'.  
        public void MethodB(int i, bool b) { }  
    }  
  
    class ProtoClassC  
    {  
        void D()  
        {  
            ProtoClassA MyClassA = new ProtoClassA();  
  
            // Invoke on 'MethodB'.  
            MyClassA.MethodB(0, false);  
        }  
    }  
    ```  
  
2. İmleci üzerine getirin `MethodB`, yöntem bildiriminde veya yöntem çağrısı.  
  
3. Üzerinde **yeniden düzenleme** menüsünü tıklatın **parametreleri yeniden Sırala**.  
  
     **Parametreleri yeniden Sırala** iletişim kutusu görüntülenir.  
  
4. İçinde **parametreleri yeniden Sırala** iletişim kutusunda `int i` içinde **parametreleri** listelemek ve sonra aşağı düğmesine tıklayın.  
  
     Alternatif olarak, sürükleyebilirsiniz `int i` sonra `bool b` içinde **parametreleri** listesi.  
  
5. İçinde **parametreleri yeniden Sırala** iletişim kutusu, tıklayın **Tamam**.  
  
     Varsa **başvuru değişikliklerini önizle** seçeneği seçildiğinde, **parametreleri yeniden Sırala** iletişim kutusu, **Değişiklikleri Önizle - Parametreleri Yeniden Sırala** iletişim kutusu görüntülenir. Önizleme değişiklikleri için parametre listesinde sağlar `MethodB` imza hem de yöntem çağrısı.  
  
    1. Varsa **Değişiklikleri Önizle - Parametreleri Yeniden Sırala** iletişim kutusu görüntülendikten sonra **Uygula**.  
  
         Bu örnekte, yöntem bildiriminde ve tüm yöntemini çağırma siteleri `MethodB` güncelleştirilir.  
  
## <a name="remarks"></a>Açıklamalar  
 Yöntem bildiriminde veya yöntem çağrısından parametrelerinden sıralayabilirsiniz. İmleci üzerinde veya yöntem veya temsilci bildirimi yanında ancak gövde getirin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yeniden Düzenleme (C#)](../csharp-ide/refactoring-csharp.md)