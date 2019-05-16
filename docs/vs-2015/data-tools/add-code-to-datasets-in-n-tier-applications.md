---
title: N katmanlı uygulamalarda veri kümelerine kod ekleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- n-tier applications, extending datasets
ms.assetid: d43c2ccd-4902-43d8-b1a8-d10ca5d3210c
caps.latest.revision: 23
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 6c788e422ea8613b77d7d0c0460d7c026916baa3
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65697149"
---
# <a name="add-code-to-datasets-in-n-tier-applications"></a>N katmanlı uygulamalarda veri kümelerine kod ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Veri kümesi için bir parçalı sınıf dosyası oluşturma ve kod eklemeyi tarafından bir veri kümesinin işlevselliğini genişletebilirsiniz (kod eklemek yerine *DatasetName*. Dataset.Designer dosyası). Kısmi sınıflar arasında birden çok fiziksel dosyaları Bölünecek belirli bir sınıf için kod etkinleştirin. Daha fazla bilgi için [kısmi](https://msdn.microsoft.com/library/7adaef80-f435-46e1-970a-269fff63b448) veya [kısmi sınıflar ve yöntemler](https://msdn.microsoft.com/library/804cecb7-62db-4f97-a99f-60975bd59fa1).

Veri kümesi tanımı için yapılan değişiklikler her zaman bir veri kümesini tanımlayan bir kod oluşturulur. Bu kod Ayrıca, herhangi bir veri kümesinin yapılandırmasını değiştirir Sihirbazı'nı çalıştırılması sırasında değişiklik yaptığınızda oluşturulur. Kodunuzu bir veri kümesi oluşturma işlemi sırasında silinmesini önlemek için veri kümesinin parçalı sınıf dosyası için kodu ekleyin.

Veri kümesi ayırdıktan sonra varsayılan olarak ve `TableAdapter` kod sonucu olan her proje bir parçalı sınıf dosyasında. Özgün proje sahip bir filenamed *DatasetName*. Designer.vb olarak adlandırılır (veya *DatasetName*. Designer.cs) içeren `TableAdapter` kod. İçinde belirtilen projeyi **Dataset projesi** özellik adında bir dosya var *DatasetName*. DataSet.Designer.vb (veya *DatasetName*. DataSet.Designer.cs). Bu dosya, veri kümesi kodunu içerir.

> [!NOTE]
> Veri kümelerini ve `TableAdapter`s (ayarlayarak **DataSet projesi** özelliği), projedeki varolan kısmi veri kümesi sınıfları olmaz taşınması otomatik olarak. Var olan veri kümesi kısmi sınıflarının veri kümesi projesine el ile taşınması gerekir.

> [!NOTE]
> Doğrulama kodu eklenmesi gerektiğinde, veri kümesi Tasarımcısı oluşturmak için işlevsellik sağlar. <xref:System.Data.DataTable.ColumnChanging> ve <xref:System.Data.DataTable.RowChanging> olay işleyicileri. Daha fazla bilgi için [bir n katmanlı bir veri kümesine doğrulama ekleme](../data-tools/add-validation-to-an-n-tier-dataset.md).

## <a name="add-code-to-datasets-in-n-tier-applications"></a>N katmanlı uygulamalarda veri kümelerine kod ekleme

1. (Veri kümesi) .xsd dosyasını içeren proje bulun.

2. Seçin **.xsd** dosyayı veri kümesini açın.

3. Kod (başlık çubuğundaki tablo adı) ekleyin ve ardından istediğiniz veri tablosuna sağ **kodu görüntüle**.

     Kısmi sınıf oluşturulur ve Kod Düzenleyicisi'nde açılır.

4. Kısmi sınıf bildirimi içinde kod ekleyin.

     Aşağıdaki örnek, NorthwindDataSet'teki CustomersDataTable kod ekleme yeri gösterir:

    ```vb
    Partial Public Class CustomersDataTable
        ' Add code here to add functionality
        ' to the CustomersDataTable.
    End Class
    ```

    ```csharp
    partial class CustomersDataTable
    {
        // Add code here to add functionality
        // to the CustomersDataTable.
    }
    ```

## <a name="see-also"></a>Ayrıca bkz.

- [N Katmanlı Veri Uygulamalarına Genel Bakış](../data-tools/n-tier-data-applications-overview.md)
- [N katmanlı uygulamalarda TableAdapter’lara kod ekleme](../data-tools/add-code-to-tableadapters-in-n-tier-applications.md)
- [TableAdapter'ları](https://msdn.microsoft.com/library/09416de9-134c-4dc7-8262-6c8d81e3f364)
- [TableAdapterManager genel bakış](https://msdn.microsoft.com/library/33076d42-6b41-491a-ac11-6c6339aea650)
- [Hiyerarşik güncelleştirmeye genel bakış](https://msdn.microsoft.com/library/c4f8e8b9-e4a5-4a02-8462-d03d1e8222d6)
- [Visual Studio'daki veri kümesi araçları](../data-tools/dataset-tools-in-visual-studio.md)