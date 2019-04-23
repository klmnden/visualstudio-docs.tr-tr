---
title: N katmanlı uygulamalarda Tableadapter'lara kod ekleyin | Microsoft Docs
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
- TableAdapters, n-tier applications
- n-tier applications, extending TableAdapters
ms.assetid: dafac00e-df9d-4d4a-95a6-e34b4d099425
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 3c3ddcb99163fe3548f020094647566c1779f5d9
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60115373"
---
# <a name="add-code-to-tableadapters-in-n-tier-applications"></a>N katmanlı uygulamalarda TableAdapter’lara kod ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İşlevlerini genişletmek bir `TableAdapter` için bir parçalı sınıf dosyası oluşturarak `TableAdapter` ve kod eklemeyi (kod eklemek yerine *DatasetName*. DataSet.Designer dosyası). Kısmi sınıflar arasında birden çok fiziksel dosyaları Bölünecek belirli bir sınıf için kod etkinleştirin. Daha fazla bilgi için [kısmi](http://msdn.microsoft.com/library/7adaef80-f435-46e1-970a-269fff63b448) veya [partial (tür)](http://msdn.microsoft.com/library/27320743-a22e-4c7b-b0b3-53afe3607334).  
  
 Kodu tanımlayan bir `TableAdapter` değişiklik her zaman oluşturulan `TableAdapter`. Her sihirbazın yapılandırmasını değiştirir çalışması sırasında değişiklik yapıldığında bu kod ayrıca oluşturulur `TableAdapter`. Kodunuzu anahtarınızın yeniden oluşturulması sırasında silinmesini önlemek için bir `TableAdapter`, kısmi sınıf dosyaya kod eklemek `TableAdapter`.  
  
 Veri kümesi ayırdıktan sonra varsayılan olarak ve `TableAdapter` kod sonucu olan her proje bir parçalı sınıf dosyasında. Adlı bir dosya özgün proje sahip *DatasetName*. Designer.vb olarak adlandırılır (veya *DatasetName*. Designer.cs) içeren `TableAdapter` kod. İçinde belirtilen projeyi **Dataset projesi** özelliği adlı bir dosya var *DatasetName*. DataSet.Designer.vb (veya *DatasetName*. DataSet.Designer.cs), veri kümesi kodunu içerir.  
  
> [!NOTE]
> Veri kümelerini ve `TableAdapter`s (ayarlayarak **DataSet projesi** özelliği), projedeki varolan kısmi veri kümesi sınıfları taşınmaz otomatik olarak. Var olan veri kümesi kısmi sınıflarının veri kümesi projesine el ile taşınması gerekir.  
  
> [!NOTE]
> Veri kümesi Tasarımcısı oluşturmak için işlevsellik sağlar <xref:System.Data.DataTable.ColumnChanging> ve <xref:System.Data.DataTable.RowChanging> doğrulama gerektiğinde olay işleyicileri. Daha fazla bilgi için [bir n katmanlı bir veri kümesine doğrulama ekleme](../data-tools/add-validation-to-an-n-tier-dataset.md).  
  
 [!INCLUDE[note_settings_general](../includes/note-settings-general-md.md)]  
  
### <a name="to-add-user-code-to-a-tableadapter-in-an-n-tier-application"></a>Bir TableAdapter n katmanlı bir uygulama içinde kullanıcı kodu eklemek için  
  
1. (Veri kümesi) .xsd dosyasını içeren proje bulun.  
  
2. Çift tıklayarak **.xsd** dosyayı veri kümesini açın.  
  
3. Sağ `TableAdapter` kodu ekleyin ve ardından istediğiniz**kodu görüntüle**.  
  
     Kısmi sınıf oluşturulur ve Kod Düzenleyicisi'nde açılır.  
  
4. Kısmi sınıf bildirimi içinde kod ekleyin.  
  
5. Aşağıdaki örnek için kodunun nereye ekleneceğini gösterir `CustomersTableAdapter` içinde `NorthwindDataSet`:  
  
    ```vb  
    Partial Public Class CustomersTableAdapter  
        ' Add code here to add functionality   
        ' to the CustomersTableAdapter.  
    End Class  
    ```  
  
    ```csharp  
    public partial class CustomersTableAdapter  
    {  
        // Add code here to add functionality  
        // to the CustomersTableAdapter.  
    }  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [N katmanlı veri uygulamalarına genel bakış](../data-tools/n-tier-data-applications-overview.md)   
 [N katmanlı uygulamalarda veri kümelerine kod ekleme](../data-tools/add-code-to-datasets-in-n-tier-applications.md)   
 [TableAdapter'ları](http://msdn.microsoft.com/library/09416de9-134c-4dc7-8262-6c8d81e3f364)   
 [TableAdapterManager genel bakış](http://msdn.microsoft.com/library/33076d42-6b41-491a-ac11-6c6339aea650)   
 [Hiyerarşik güncelleştirmeye genel bakış](http://msdn.microsoft.com/library/c4f8e8b9-e4a5-4a02-8462-d03d1e8222d6)