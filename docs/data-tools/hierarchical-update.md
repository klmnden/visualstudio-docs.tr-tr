---
title: Hiyerarşik güncelleştirme
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- saving data, changed data
- data [Visual Basic], hierarchical update
- saving updated data
- datasets [Visual Basic], hierarchical update
- hierarchical update
- saving data, hierarchical update
- modified data saving
- updated data saving
- related tables, saving
ms.assetid: 68bae3f6-ec9b-45ee-a33a-69395029f54c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: a15daaf5ac98bc2efc4ce83bb2370b94e9f59123
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66745457"
---
# <a name="hierarchical-update"></a>Hiyerarşik güncelleştirme

*Hiyerarşik güncelleştirme* tutarlılığı korurken (bir veri kümesinden iki veya daha fazla ilgili tablo ile) güncelleştirilmiş verileri bir veritabanına geri kaydediliyor işlemini ifade eder. *Bilgi tutarlılığını* veritabanında ve ekleme, güncelleştirme ve ilgili kayıt silme davranışını kontrol kısıtlamaları tarafından sağlanan tutarlık kuralları ifade eder. Örneğin, o müşteri için oluşturulacak siparişler izin vermeden önce bir müşteri kaydı oluşturulmasını zorlar tutarlılığı olur.  Veri kümelerindeki ilişkiler hakkında daha fazla bilgi için bkz: [veri kümelerindeki ilişkiler](../data-tools/relationships-in-datasets.md).

Hiyerarşik güncelleştirme özelliğini kullanan bir `TableAdapterManager` yönetmek için `TableAdapter`s'te bir türü belirtilmiş veri kümesi. `TableAdapterManager` .NET türü bir Visual Studio tarafından oluşturulan sınıf, bir bileşendir. Bir tablodan sürüklediğinizde **veri kaynakları** penceresini bir Windows Form ya da WPF sayfasına Visual Studio, belirli bir form veya sayfadaki TableAdapterManager türünde bir değişken ekler ve bileşen tepsisinde Tasarımcısı'nda bkz. İlgili ayrıntılı bilgi için `TableAdapterManager` TableAdapterManager başvuru bölümüne bakın, sınıf [TableAdapters](../data-tools/create-and-configure-tableadapters.md).

Varsayılan olarak, bir veri kümesi ilişkili tablolar "yalnızca ilişkileri" yabancı anahtar kısıtlamaları zorunlu değildir, yani değerlendirir. Tasarım zamanında bu ayarı kullanarak değiştirebilirsiniz **veri kümesi Tasarımcısı**. Ortaya çıkarmak için iki tablo arasında ilişki satırı **ilişkisi** iletişim kutusu. Burada yaptığınız değişiklikler belirleyecek nasıl `TableAdapterManager` ne zaman davranışını göndermeden değişiklikleri ilişkili tabloların veritabanına geri.

## <a name="enable-hierarchical-update-in-a-dataset"></a>Bir veri kümesi hiyerarşik güncelleştirmeyi etkinleştirme

Varsayılan olarak, hiyerarşik güncelleştirme eklenen ya da bir projede oluşturulan tüm yeni veri kümeleri için etkinleştirilir. Hiyerarşik güncelleştirme Aç veya kapat ayarlayarak **hiyerarşik güncelleştirme** bir türü belirtilmiş veri kümesi için veri kümesinde özelliği **True** veya **False**:

![Hiyerarşik güncelleştirme ayarı](../data-tools/media/hierarchical-update-setting.png)

## <a name="create-a-new-relation-between-tables"></a>Yeni tablolar arasında ilişki oluşturma

İki tablo arasında yeni bir ilişki oluşturmak için veri kümesi Tasarımcısı'nda, her tablonun başlık çubuğunu seçin, sonra sağ tıklayıp **ilişkisi ekleme**.

![Hiyerarşik güncelleştirme ilişkisi menü ekleme](../data-tools/media/hierarchical-update-add-relation-menu.png)

## <a name="understand-foreign-key-constraints-cascading-updates-and-deletes"></a>Yabancı anahtar kısıtlamaları, geçişli güncelleştirme ve silme anlama

Nasıl FOREIGN key kısıtlamalarını anlamak önemlidir ve davranışı veritabanındaki geçişli üretilen veri kümesi kod oluşturulur.

Varsayılan olarak, bir veri kümesindeki veri tablolarının ilişkilerle oluşturulur (<xref:System.Data.DataRelation>) ilişkileri veritabanında eşleşen. Ancak, ilişki veri kümesinde yabancı anahtar kısıtlama olarak oluşturulmaz. <xref:System.Data.DataRelation> Olarak yapılandırılmış **ilişkisi yalnızca** olmadan <xref:System.Data.ForeignKeyConstraint.UpdateRule%2A> veya <xref:System.Data.ForeignKeyConstraint.DeleteRule%2A> etkin.

Varsayılan olarak, geçişli güncelleştirmeler ve silmeleri basamaklı güncelleştirmeleriyle veritabanı ilişkisi ve/veya silmenin açık olsa bile devre dışı bırakılmıştır. Örneğin, yeni bir müşteri ve yeni bir sipariş oluşturmak ve ardından veri kaydetmeye çalışırken bir çakışma veritabanında tanımlanan yabancı anahtar kısıtlamalarıyla neden olabilir. Daha fazla bilgi için [bir veri kümesini doldururken kısıtlamaları kapatma kapatma](turn-off-constraints-while-filling-a-dataset.md).

## <a name="set-the-order-to-perform-updates"></a>Güncelleştirmeleri gerçekleştirmek için sırasını ayarlama

Güncelleştirmeleri gerçekleştirmek için sırasını ayarlama ekler, güncelleştirir ve silme işlemlerini ayrı ayrı sırasını ayarlar tüm değiştirilmiş verileri bir veri kümesinin tüm tablolarda kaydetmek için gereklidir. Hiyerarşik güncelleştirme etkinleştirildiğinde, ekler önce gerçekleştirilir sonra güncelleştirir ve siler. `TableAdapterManager` Sağlayan bir `UpdateOrder` özelliği, ilk olarak, güncelleştirmeleri gerçekleştirmek üzere sonra ekler ve siler.

> [!NOTE]
> Güncelleştirme sırası her şey dahil olduğunu anlamak önemlidir. Güncelleştirme yapıldığında, diğer bir deyişle, ekler ve ardından silmeleri kümesindeki tüm tabloların gerçekleştirilir.

Ayarlanacak `UpdateOrder` sürüklemeye sonra özelliği [veri kaynakları penceresi](add-new-data-sources.md#data-sources-window) bir forma seçin `TableAdapterManager` bileşeni Tepsi ve ardından `UpdateOrder` özelliğinde **özellikleri** penceresi.

## <a name="create-a-backup-copy-of-a-dataset-before-performing-a-hierarchical-update"></a>Hiyerarşik güncelleştirme gerçekleştirmeden önce yedek bir kopyası, bir veri kümesi oluşturma

Veri kaydettiğinizde (çağırarak `TableAdapterManager.UpdateAll()` yöntemi), `TableAdapterManager` tek bir işlemde her tablo için verileri güncelleştirmek çalışır. Herhangi bir bölümünü herhangi bir tabloda güncelleştirmesi başarısız olursa, tüm işlem geri alınır. Çoğu durumda, uygulamanızı özgün durumuna geri döndürür.

Ancak, bazen dataset yedek kopyadan geri yüklemek isteyebilirsiniz. Otomatik artış değerlerini kullanırken bu gerçekleşebilir. Örneğin, kaydetme işlemi başarılı değil, otomatik artış değerleri kümesinde sıfırlanır ve veri kümesini otomatik artan değerleri oluşturmak devam eder. Bu, uygulamanızda kabul edilebilir olmayabilir, numaralandırma, boşluk bırakır. Durumlarda bu bir sorun olduğu `TableAdapterManager` sağlayan bir `BackupDataSetBeforeUpdate` özelliği, işlem başarısız olursa mevcut veri kümesini bir yedek kopyasıyla değiştirir.

> [!NOTE]
> Yedekleme sırasında bellekte yalnızca kopyasıdır `TableAdapterManager.UpdateAll` yöntemi çalışıyor. Bu nedenle, programlı erişimi yoktur yedekleme bu veri kümesine özgün veri kümesinden değiştirir ya kapsamın dışına çıkıncaya çünkü hemen sonra `TableAdapterManager.UpdateAll` yöntemi tamamlandıktan çalışıyor.

## <a name="modify-the-generated-save-code-to-perform-the-hierarchical-update"></a>Oluşturulan kodu hiyerarşik güncelleştirmeyi gerçekleştirmek için ' değiştirin

Değişiklik kümesindeki ilgili veri tablolarında veritabanına çağırarak kaydetmek `TableAdapterManager.UpdateAll` yöntemi ve ilişkili tabloları içeren bir veri kümesi adını geçirerek. Örneğin, `TableAdapterManager.UpdateAll(NorthwindDataset)` NorthwindDataset tüm tablolardaki için arka uç veritabanı güncelleştirmeleri göndermek için yöntemi.

Öğeleri bırak sonra **veri kaynakları** penceresinde kodu otomatik olarak eklenir `Form_Load` her tabloyu doldurmak için olay ( `TableAdapter.Fill` yöntemleri). Kodu da eklenir **Kaydet** düğme tıklatma olayını, <xref:System.Windows.Forms.BindingNavigator> veri kümesinden veritabanına geri kaydedin ( `TableAdapterManager.UpdateAll` yöntemi).

Oluşturulan kodu kaydetmek bir çağıran kod satırı içerecek `CustomersBindingSource.EndEdit` yöntemi. Özellikle, çağıran <xref:System.Windows.Forms.BindingSource.EndEdit%2A> yöntemi ilk <xref:System.Windows.Forms.BindingSource>formuna eklenir. Diğer bir deyişle, bu kod yalnızca gelen sürüklediğiniz ilk tablo için oluşturulan **veri kaynakları** forma penceresi. <xref:System.Windows.Forms.BindingSource.EndEdit%2A> Çağrısı şu anda düzenlenmekte olan herhangi bir veriye bağlı denetim işleminde değişiklikleri kaydeder. Odak ve bu nedenle, bir veri bağlı denetim hala varsa tıklayın **Kaydet** denetim kaydedilir, gerçek kaydetme önce tüm bekleyen düzenlemeler düğmesine ( `TableAdapterManager.UpdateAll` yöntemi).

> [!NOTE]
> **Veri kümesi Tasarımcısı** yalnızca ekler `BindingSource.EndEdit` forma bırakılan ilk tablo için kod. Bu nedenle, bir çağırmak için kod satırı eklemeniz gerekir `BindingSource.EndEdit` formunda ilgili her tablo için yöntemi. Bu kılavuz için bu çağrı eklemek sahip olduğunuz anlamına gelir `OrdersBindingSource.EndEdit` yöntemi.

### <a name="to-update-the-code-to-commit-changes-to-the-related-tables-before-saving"></a>Kod değişiklikleri kaydetmeden önce ilişkili tabloları için güncelleştirmek için

1. Çift **Kaydet** düğmesini <xref:System.Windows.Forms.BindingNavigator> açmak için **Form1** Kod Düzenleyicisi'nde.

2. Çağırmak için kod satırını ekleyin `OrdersBindingSource.EndEdit` yöntemi çağıran satırdan `CustomersBindingSource.EndEdit` yöntemi. Kodda **Kaydet** düğmesi tıklamasından olay aşağıdaki benzemesi gerekir:

     [!code-vb[VSProDataOrcasHierarchicalUpdate#1](../data-tools/codesnippet/VisualBasic/hierarchical-update_1.vb)]
     [!code-csharp[VSProDataOrcasHierarchicalUpdate#1](../data-tools/codesnippet/CSharp/hierarchical-update_1.cs)]

Verileri bir veritabanına kaydetme önce ilgili alt tablo üzerinde değişiklikler işleniyor ek olarak, bir veri kümesi için yeni alt kayıtları eklemeden önce yeni oluşturulan işleme üst kayıtlar için de olabilir. Diğer bir deyişle, yeni ana kayıt eklemeniz gerekebilir (`Customer`) yeni alt kayıtları yabancı anahtar kısıtlamalarını etkinleştirmeden önce veri kümesine (`Orders`) kümesine eklenecek. Bunu yapmak için alt kullanabilirsiniz `BindingSource.AddingNew` olay.

> [!NOTE]
> Yeni üst kayıtlar işleme gerekip gerekmediğini, veri kaynağına bağlamak için kullanılan denetim türünü bağlıdır. Bu kılavuzda, üst tabloya bağlamak için tek tek denetimleri kullanın. Bu, yürütme yeni üst kaydı için ek kod gerektirir. Bunun yerine üst kayıtlar Karmaşık bağlama denetimde görüntülenen hoşlanıyorsanız <xref:System.Windows.Forms.DataGridView>, bu ek <xref:System.Windows.Forms.BindingSource.EndEdit%2A> ana kayıt gerekli olmaz için çağırın. Temel alınan veri bağlama denetimi işlevlerini yürüten yeni kayıtları işleme olmasıdır.

### <a name="to-add-code-to-commit-parent-records-in-the-dataset-before-adding-new-child-records"></a>Yeni alt kayıtları eklemeden önce üst kayıtlar veri kümesini yürütmek için kodu eklemek için

1. İçin bir olay işleyicisi oluşturun `OrdersBindingSource.AddingNew` olay.

    - Açık **Form1** Tasarım görünümünde seçin **OrdersBindingSource** bileşen tepsisinde seçin **olayları** içinde **özellikleri** penceresinde ve ardından çift **AddingNew** olay.

2. Çağıran olay işleyicisine kod satırını ekleyin `CustomersBindingSource.EndEdit` yöntemi. Kodda `OrdersBindingSource_AddingNew` olay işleyicisi aşağıdaki benzemesi gerekir:

     [!code-vb[VSProDataOrcasHierarchicalUpdate#2](../data-tools/codesnippet/VisualBasic/hierarchical-update_2.vb)]
     [!code-csharp[VSProDataOrcasHierarchicalUpdate#2](../data-tools/codesnippet/CSharp/hierarchical-update_2.cs)]

## <a name="tableadaptermanager-reference"></a>TableAdapterManager başvurusu

Varsayılan olarak, bir `TableAdapterManager` sınıfı ilişkili tabloları içeren bir veri kümesi oluşturduğunuzda oluşturulur. Sınıf oluşturulmasını önlemek için değerini değiştirmek `Hierarchical Update` özelliği false kümesi. WPF sayfası ya da Windows Form Tasarım yüzeyine bir ilişkisi olan bir tabloda sürüklediğinizde, Visual Studio sınıfının bir üye değişkeni bildirir. Veri bağlama kullanmazsanız, el ile değişkenini tanımlamak zorunda.

`TableAdapterManager` Sınıfı .NET türü değil. Bu nedenle, bu belgelerde bakarak olamaz. Tasarım zamanında veri kümesi oluşturma işleminin bir parçası olarak oluşturulur.

Sık kullanılan yöntemleri ve özellikleri verilmiştir `TableAdapterManager` sınıfı:

|Üye|Açıklama|
|------------|-----------------|
|`UpdateAll` Yöntemi|Tüm veriler, tüm veri tablolarından kaydeder.|
|`BackUpDataSetBeforeUpdate` Özelliği|Yürütmeden önce yedek bir kopyası, veri kümesinin oluşturulup oluşturulmayacağını belirler `TableAdapterManager.UpdateAll` yöntemi. Boole değeri.|
|*tableName* `TableAdapter` özelliği|Temsil eden bir `TableAdapter`. Oluşturulan `TableAdapterManager` her biri için bir özellik içeriyor `TableAdapter` yönettiği. Örneğin, müşteriler ve siparişler bir tablo olan bir veri kümesi ile oluşturulan bir `TableAdapterManager` içeren `CustomersTableAdapter` ve `OrdersTableAdapter` özellikleri.|
|`UpdateOrder` Özelliği|Ayrı ayrı INSERT, update ve delete komutlarını sırasını denetler. Bu değerler birine `TableAdapterManager.UpdateOrderOption` sabit listesi.<br /><br /> Varsayılan olarak, `UpdateOrder` ayarlanır **InsertUpdateDelete**. Ekler, sonra güncelleştirir ve siler Bunun anlamı, veri kümesindeki tüm tabloların gerçekleştirilir.|

## <a name="see-also"></a>Ayrıca bkz.

- [Verileri yeniden veritabanına kaydetme](../data-tools/save-data-back-to-the-database.md)
