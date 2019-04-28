---
title: Veritabanına yeni kayıtlar ekleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
- aspx
helpviewer_keywords:
- TableAdapters, inserting new records into
- data [Visual Studio], saving
- databases, inserting new records into
- records, inserting
- saving data
ms.assetid: ea118fff-69b1-4675-b79a-e33374377f04
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: bd5074af8f0a9ca172d04b4cd5bb1d9057ad4bb5
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63384072"
---
# <a name="insert-new-records-into-a-database"></a>Veritabanına yeni kayıtlar ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Veritabanına yeni kayıtlar eklemek için kullanabileceğiniz `TableAdapter.Update` yöntemi veya TableAdapter bağdaştırıcısının DBDirect yöntemleri birini (özellikle `TableAdapter.Insert` yöntemi).
  
 Uygulamanızı TableAdapters kullanmıyorsa, komut nesneleri kullanabilirsiniz (örneğin, <xref:System.Data.SqlClient.SqlCommand>) veritabanınızdaki yeni kayıtları eklemek için.  
  
 Uygulama verilerini depolamak için veri kümelerini kullanan kullanırsanız `TableAdapter.Update` yöntemi. `Update` Yöntemi veritabanına (güncelleştirmeler, ekler ve siler) tüm değişiklikleri gönderir.  
  
 Uygulamanızın veri depolama ya da hassas denetime veritabanına yeni kayıtlar oluşturmak istiyorsanız kullanın nesneleri kullanıp kullanmadığını `TableAdapter.Insert` yöntemi.  
  
 TableAdapter yoksa bir `Insert` yöntemi geldiğini TableAdapter ya da saklı yordamları kullanmak için yapılandırıldığını veya kendi `GenerateDBDirectMethods` özelliği `false`. TableAdapter bağdaştırıcısının yapmayı deneyin `GenerateDBDirectMethods` özelliğini `true` gelen veri kümesi Tasarımcısı içinde ve veri kümesi kaydedin. Bu, TableAdapter yeniden oluşturacak. TableAdapter hala yoksa bir `Insert` yöntemi daha sonra tablonun büyük olasılıkla sağlamaz arasında bireysel satırları ayırt etmek için yeterli şema bilgileri (örneğin, olabilir tablosunda birincil anahtar ayarlanmadı).  
  
## <a name="insert-new-records-by-using-tableadapters"></a>TableAdapter'ı kullanarak yeni kayıtlar ekleme  
 TableAdapters uygulamanızın gereksinimlerine bağlı olarak bir veritabanına yeni kayıtlar eklemek için farklı yollar sunar.  
  
 Uygulama verilerini depolamak için veri kümelerini kullanan sonra yalnızca yeni kayıtlar için istenen ekleyebileceğiniz <xref:System.Data.DataTable> veri kümesini ve sonra çağrı `TableAdapter.Update` yöntemi. `TableAdapter.Update` Yöntemi tüm değişiklikleri gönderir <xref:System.Data.DataTable> (değiştirilen ve silinen kayıtlar da dahil) veritabanı.  
  
#### <a name="to-insert-new-records-into-a-database-by-using-the-tableadapterupdate-method"></a>TableAdapter.Update yöntemini kullanarak bir veritabanına yeni kayıtlar eklemek için  
  
1. Yeni kayıtlar için istenen ekleme <xref:System.Data.DataTable> yeni bir oluşturarak <xref:System.Data.DataRow> ve eklemeyi <xref:System.Data.DataTable.Rows%2A> koleksiyonu. Daha fazla bilgi için [nasıl yapılır: Bir DataTable tablosuna satır ekleme](http://msdn.microsoft.com/library/78ebbb43-c402-49cf-81da-0715289487bf).  
  
2. Yeni satırlar eklendikten sonra <xref:System.Data.DataTable>, çağrı `TableAdapter.Update` yöntemi. Tüm geçirerek ya da güncelleştirmek için veri miktarını denetleyebilirsiniz <xref:System.Data.DataSet>, <xref:System.Data.DataTable>, bir dizi <xref:System.Data.DataRow>s ya da tek bir <xref:System.Data.DataRow>.  
  
    Aşağıdaki kod, yeni bir kayıt eklemek gösterilmektedir bir <xref:System.Data.DataTable> ve sonra çağrı `TableAdapter.Update` yeni satır veritabanına kaydetmek için yöntemi. (Bu örnekte `Region` Northwind veritabanındaki tabloda.)  
  
    [!code-csharp[VbRaddataSaving#14](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataSaving/CS/Form5.cs#14)]
    [!code-vb[VbRaddataSaving#14](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataSaving/VB/Form5.vb#14)]  
  
   Uygulama verilerini depolamak için nesneleri kullanıyorsa, kullanabileceğiniz `TableAdapter.Insert` yöntemini doğrudan veritabanında yeni satırlar. `Insert` Yöntemi, her bir sütunun değerlerini ayrı ayrı parametre olarak kabul eder. Yeni bir kayıt yöntemini çağırarak geçirilen parametre değerleri ile veritabanına ekler.  
  
   Aşağıdaki yordam kullanır `Region` örnek olarak Northwind veritabanındaki tablo.  
  
#### <a name="to-insert-new-records-into-a-database-by-using-the-tableadapterinsert-method"></a>TableAdapter.INSERT yöntemi kullanarak bir veritabanına yeni kayıtlar eklemek için  
  
- TableAdapter bağdaştırıcısının çağrı `Insert` değerler her sütun için parametre olarak geçirmeyi yöntemi.  
  
    > [!NOTE]
    > Kullanmak istediğiniz TableAdapter kullanılabilir bir örnek yoksa örneği.  
  
     [!code-csharp[VbRaddataSaving#15](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataSaving/CS/Class1.cs#15)]
     [!code-vb[VbRaddataSaving#15](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataSaving/VB/Class1.vb#15)]  
  
## <a name="insert-new-records-by-using-command-objects"></a>Komut nesneleri kullanarak yeni kayıtlar ekleme  
 Aşağıdaki örnek, doğrudan komut nesneleri kullanarak bir veritabanına yeni kayıtlar ekler.
  
 Aşağıdaki yordam kullanır `Region` örnek olarak Northwind veritabanındaki tablo.  
  
#### <a name="to-insert-new-records-into-a-database-by-using-command-objects"></a>Komut nesneleri kullanarak bir veritabanına yeni kayıtlar eklemek için  
  
- Yeni bir komut nesnesi oluşturur ve ardından kendi `Connection`, `CommandType`, ve `CommandText` özellikleri.  
  
     [!code-csharp[VbRaddataSaving#16](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataSaving/CS/Class1.cs#16)]
     [!code-vb[VbRaddataSaving#16](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataSaving/VB/Class1.vb#16)]  
  
## <a name="net-framework-security"></a>.NET Framework Güvenliği  
 İstenen tabloya ekler gerçekleştirme izni yanı sıra, bağlanmaya çalıştığınız veritabanı erişimi olmalıdır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Verileri yeniden veritabanına kaydetme](../data-tools/save-data-back-to-the-database.md)
