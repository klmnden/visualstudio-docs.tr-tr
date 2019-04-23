---
title: 'Nasıl yapılır: Boş değer atanabilir bir tür (Sınıf Tasarımcısı) oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- nullable types, Class Designer
- Class Designer [Visual Studio], nullable types
ms.assetid: 84673a89-3f6d-4668-919e-1c0f56182fe5
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 3d5e74a4384cff0a68764ffe09a37ab28460d58b
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60058505"
---
# <a name="how-to-create-a-nullable-type-class-designer"></a>Nasıl yapılır: Boş değer atanabilir bir tür (Sınıf Tasarımcısı) oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Belirli değer türleri her zaman sahip (tanımlı bir değer veya gerekir). Burada bazı alanlar herhangi bir değer atanamaz veritabanlarında yaygın yöntem budur. Örneğin, bir null değer, henüz bir değer atanmadı olduğunu belirtmek için bir veritabanı alanı atayabilirsiniz.  
  
 A *boş değer atanabilir tür* türü ve ayrıca bir null değer için tipik değerleri aralığı alır, böylece genişleten bir değer türüdür. Örneğin, bir boş değer atanabilir, `Int32`, null olarak da başlar\<Int32 > herhangi bir değer -2147483648 2147483647 için atanabilir veya bir null değer atanabilir. Bir boş değer\<bool > değerler atanabilir `True`, `False`, ya da null (hiç değer).  
  
 Boş değer atanabilir türler örnekleridir <xref:System.Nullable%601> yapısı. Boş değer atanabilir bir tür örneği her iki genel salt okunur özelliklere sahip `HasValue` ve `Value`:  
  
- `HasValue` tür `bool` ve değişken tanımlı bir değer içerip içermediğini belirtir. `True` değişkeni boş olmayan bir değer içeren anlamına gelir. İçin tanımlı bir değer gibi bir deyim kullanarak test edebilirsiniz `if (x.HasValue)` veya `if (y != null)`.  
  
- `Value` temel alınan aynı türde değil. Varsa `HasValue` olduğu `True`, `Value` anlamlı bir değer içeriyor. Varsa `HasValue` olduğu `False`, erişim `Value` bir geçersiz işlem özel durum oluşturur.  
  
  Varsayılan, boş değer atanabilir bir tür olarak bir değişken bildirdiğinizde tanımlı değer yok sahiptir (`HasValue` olan `False`), kendi temel değer türünün varsayılan değeri diğer.  
  
  Sınıf Tasarımcısı, temelindeki türe görüntüler yalnızca boş değer atanabilir bir tür görüntüler.  
  
  Visual C# içinde boş değer atanabilir türler hakkında daha fazla bilgi için bkz. [boş değer atanabilir türler](http://msdn.microsoft.com/library/e473cb01-28ca-42be-9cea-f717055d72c6). Visual Basic'te boş değer atanabilir türler hakkında daha fazla bilgi için bkz: [boş değer atanabilir değer türleri](http://msdn.microsoft.com/library/9ac3b602-6f96-4e6d-96f7-cd4e81c468a6).  
  
  [!INCLUDE[note_settings_general](../includes/note-settings-general-md.md)]  
  
### <a name="to-add-a-nullable-type-by-using-the-class-designer"></a>Sınıf Tasarımcısı kullanarak boş değer atanabilir bir tür eklemek için  
  
1. Sınıf diyagramında varolan bir sınıfı genişletebilir veya yeni bir sınıf oluşturun.  
  
2. Projeye bir sınıf eklemek için **sınıf diyagramı** menüsünde tıklatın **Ekle**ve ardından **sınıfı Ekle**.  
  
3. Sınıf şeklinin genişletme için **sınıf diyagramı** menüsünde tıklatın **genişletme**.  
  
4. Sınıf şekli seçin. Üzerinde **sınıf diyagramı** menüsünde tıklatın **Ekle**ve ardından **alan**. Varsayılan ada sahip yeni bir alan **alan** sınıf şeklinin ve ayrıca görünür **sınıf ayrıntıları** penceresi.  
  
5. İçinde **adı** sütununun **sınıf ayrıntıları** penceresi (veya kendi sınıfında Şekil), yeni alan adı geçerli ve anlamlı bir adla değiştirin.  
  
6. İçinde **türü** sütununun **sınıf ayrıntıları** penceresinde, aşağıdaki kodda gösterildiği gibi boş değer atanabilir bir tür olarak türü bildirmek:  
  
    ```csharp  
    // Declare a nullable type in Visual C#:  
    class Test  
    {  
       int? building_number = 5;  
    }  
    ```  
  
    ```vb  
    ' Declare a nullable type in Visual Basic:  
    Class Test  
       Dim buildingNumber As Nullable(Of Integer) = 5  
    End Class  
    ```  
  
### <a name="to-add-a-nullable-type-by-using-the-code-editor"></a>Kod Düzenleyicisi'ni kullanarak boş değer atanabilir bir tür eklemek için  
  
1. Projeye bir sınıf ekleyin. İçinde proje düğümünü seçin **Çözüm Gezgini**ve **proje** menüsünde tıklatın **sınıfı Ekle**.  
  
2. Yeni bir sınıf .cs veya .vb dosyasında yeni bir sınıf içinde bir veya daha fazla boş değer atanabilir türler için sınıf bildirimi ekleyin.  
  
3. Sınıf Görünümü'ndeki yeni sınıf simgesi Sınıf Tasarımcısı tasarım yüzeyine sürükleyin. Sınıf diyagramında sınıf şekline görünür.  
  
4. Sınıf şeklinin ayrıntılarını genişletin ve sınıf üyeleri fare işaretçisini taşıyın. Araç İpucu her üyesi bildirimi görüntüler.  
  
5. Sınıf şeklinin sağ tıklatıp **sınıf ayrıntıları**. Görüntüleyebilir veya yeni türün özelliklerinde değişiklik **sınıf ayrıntıları** penceresi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Nullable%601>   
 [Boş değer atanabilir türler](http://msdn.microsoft.com/library/e473cb01-28ca-42be-9cea-f717055d72c6)   
 [Boş değer atanabilir türleri kullanma](http://msdn.microsoft.com/library/0bacbe72-ce15-4b14-83e1-9c14e6380c28)   
 [Nasıl yapılır: Boş değer atanabilir bir tür belirleme](http://msdn.microsoft.com/library/d4b67ee2-66e8-40c1-ae9d-545d32c71387)   
 [Boş Değer Atanabilen Değer Türleri](http://msdn.microsoft.com/library/9ac3b602-6f96-4e6d-96f7-cd4e81c468a6)
