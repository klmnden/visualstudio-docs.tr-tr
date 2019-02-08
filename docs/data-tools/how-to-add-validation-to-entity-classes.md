---
title: 'Nasıl yapılır: Varlık sınıflarına doğrulama ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
ms.assetid: 61107da9-7fa3-4dba-b101-ae46536f52c4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 5f4f2f5e44ea95137f53019f52de94a5389fa6d8
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55913502"
---
# <a name="how-to-add-validation-to-entity-classes"></a>Nasıl yapılır: Varlık sınıflarına doğrulama ekleme
*Doğrulama* varlık sınıfları olan veri nesnelerine girilen değerlerin bir nesnenin şeması ve ayrıca uygulama için belirlenen kurallara kısıtlamalarıyla uyumlu onaylanması işlemidir. Alttaki veritabanına güncelleştirmeleri göndermeden önce verileri doğrulamak hataları azaltan iyi bir uygulamadır. Ayrıca, bir uygulama ve veritabanı arasındaki gidiş gelişlerin potansiyel sayısını da azaltır.

 [LINQ to SQL araçları Visual Studio'da](../data-tools/linq-to-sql-tools-in-visual-studio2.md) , ekleme, güncelleştirme sırasında çalışan ve tüm varlıkların ve ayrıca sırasında ve sonrasında tek tek sütun siler tasarımcı tarafından oluşturulan kodu genişletme açmasına olanak tanıyan kısmi yöntemler sağlar değiştirir.

> [!NOTE]
>  Bu konuda, kullanarak varlık sınıflarına doğrulama ekleme için temel adımlar sağlanır **O/R Tasarımcısı**. Bir varlığa sınıfa başvuruda bulunmadan genel adımları takip etmek zor olabilir çünkü gerçek verileri kullanan bir kılavuz sağlanır.

## <a name="add-validation-for-changes-to-the-value-in-a-specific-column"></a>Belirli bir sütundaki değer değişiklikleri için doğrulama ekleme
 Bu yordamda, bir sütundaki değeri değiştiğinde verileri doğrulamak gösterilmiştir. Sınıf tanımı içinde doğrulama gerçekleştirildiğinden (yerine kullanıcı arabiriminde), değeri doğrulama başarısız olmasına neden olursa bir özel durum oluşturulur. Hata işleme için sütun değerlerini değiştirmeye çalışırsa, uygulamanızın kodunda uygulayın.

[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]

### <a name="to-validate-data-during-a-columns-value-change"></a>Bir sütunun değeri değişikliği sırasında verileri doğrulamak için

1.  Yeni bir LINQ to SQL sınıfları dosyası oluşturun veya açın (**.dbml** dosya) içinde **O/R Tasarımcısı**. (Çift **.dbml** dosyası **Çözüm Gezgini**.)

2.  İçinde **O/R Tasarımcısı**, doğrulama ekleyin ve ardından istediğiniz sınıfı sağ **kodu görüntüle**.

     Seçilen varlık sınıfı için bir parçalı sınıf Kod Düzenleyicisi açılır.

3.  Kısmi class içinde imleci yerleştirin.

4.  Visual Basic projeleri için:

    1.  Genişletin **yöntem adı** listesi.

    2.  Bulun **OnCOLUMNNAMEChanging** doğrulama eklemek istediğiniz sütun için yöntemi.

    3.  Bir `OnCOLUMNNAMEChanging` yöntemi kısmi sınıfa eklenir.

    4.  İlk girilen değer ve ardından sütun için girilen değer emin olmak için uygulamanız için kabul edilebilir olduğunu doğrulamak için aşağıdaki kodu ekleyin. `value` Bağımsız değişken içeren önerilen değeri, bu nedenle bunun geçerli bir değer olduğunu doğrulamak için mantığı ekleyin:

        ```vb
        If value.HasValue Then
            ' Add code to ensure that the value is acceptable.
            ' If value < 1 Then
            '    Throw New Exception("Invalid data!")
            ' End If
        End If
        ```

    C# projeleri için:

    Çünkü C# projeleri otomatik olarak olay işleyicileri oluşturmaz, IntelliSense sütun değiştirme kısmi yöntemler oluşturmak için kullanabilirsiniz. Tür `partial` ve kullanılabilir kısmi yöntemlerin listesi erişmeye sonra bir boşluk. Doğrulama için eklemek istediğiniz sütunu için sütun değiştirme yöntemi tıklayın. Sütun değiştirme kısmi bir yöntem seçtiğinizde oluşturulan kodu aşağıdaki koda benzer:

    ```csharp
    partial void OnCOLUMNNAMEChanging(COLUMNDATATYPE value)
        {
           throw new System.NotImplementedException();
        }
    ```

## <a name="add-validation-for-updates-to-an-entity-class"></a>Bir varlık sınıfı için güncelleştirmeleri için doğrulama ekleme
 Değerleri değişiklik sırasında denetlemenin yanı sıra, tam varlık sınıfı güncelleştirilecek denemesi yapıldığında veri da doğrulayabilirsiniz. Doğrulama güncelleştirme girişimi sırasında iş kurallarını bu gerekiyorsa birden fazla sütundaki değerleri karşılaştırmak sağlar. Aşağıdaki yordam, tam varlık sınıfı güncelleştirilecek denemesi yapıldığında doğrulamak gösterilmektedir.

> [!NOTE]
>  Doğrulama kodu güncelleştirmelerin varlık sınıfları tamamlamak kısmi yürütüldüğünde <xref:System.Data.Linq.DataContext> sınıfı (yerine bir varlığa sınıfın kısmi sınıftaki).

### <a name="to-validate-data-during-an-update-to-an-entity-class"></a>Bir varlık sınıfı için bir güncelleştirme sırasında verileri doğrulamak için

1.  Yeni bir LINQ to SQL sınıfları dosyası oluşturun veya açın (**.dbml** dosya) içinde **O/R Tasarımcısı**. (Çift **.dbml** dosyası **Çözüm Gezgini**.)

2.  Boş bir alana sağ **O/R Tasarımcısı** tıklatıp **kodu görüntüle**.

     Kısmi bir sınıf için kod düzenleyicisi açılır `DataContext`.

3.  Kısmi sınıf için imleci yerleştirin `DataContext`.

4.  Visual Basic projeleri için:

    1.  Genişletin **yöntem adı** listesi.

    2.  Tıklayın **UpdateENTITYCLASSNAME**.

    3.  Bir `UpdateENTITYCLASSNAME` yöntemi kısmi sınıfa eklenir.

    4.  Kullanarak ayrı ayrı sütun değerlerine erişim `instance` bağımsız değişken, aşağıdaki kodda gösterildiği gibi:

        ```vb
        If (instance.COLUMNNAME = x) And (instance.COLUMNNAME = y) Then
            Dim ErrorMessage As String = "Invalid data!"
            Throw New Exception(ErrorMessage)
        End If
        ```

    C# projeleri için:

    Çünkü C# projeleri otomatik olarak olay işleyicileri oluşturmaz, IntelliSense kısmi oluşturmak için kullanabileceğiniz `UpdateCLASSNAME` yöntemi. Tür `partial` ve kullanılabilir kısmi yöntemlerin listesi erişmeye sonra bir boşluk. Güncelleştirme yöntemi, doğrulama eklemek istediğiniz sınıf için tıklayın. Seçeneğini belirlediğinizde oluşturulan kodu aşağıdaki koda benzer bir `UpdateCLASSNAME` kısmi yöntem:

    ```csharp
    partial void UpdateCLASSNAME(CLASSNAME instance)
    {
        if ((instance.COLUMNNAME == x) && (instance.COLUMNNAME = y))
        {
            string ErrorMessage = "Invalid data!";
            throw new System.Exception(ErrorMessage);
        }
    }
    ```

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [Verileri doğrulama](../data-tools/validate-data-in-datasets.md)
- [LINQ to SQL (.NET Framework)](/dotnet/framework/data/adonet/sql/linq/index)