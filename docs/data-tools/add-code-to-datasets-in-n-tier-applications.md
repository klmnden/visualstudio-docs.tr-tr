---
title: N katmanlı uygulamalarda veri kümelerine kod ekleme
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- n-tier applications, extending datasets
ms.assetid: d43c2ccd-4902-43d8-b1a8-d10ca5d3210c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: dbd65c5247a82f2a58a57e50402ecde5d330cc9b
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60111694"
---
# <a name="add-code-to-datasets-in-n-tier-applications"></a>N katmanlı uygulamalarda veri kümelerine kod ekleme
Veri kümesi için bir parçalı sınıf dosyası oluşturma ve kod eklemeyi tarafından bir veri kümesinin işlevselliğini genişletebilirsiniz (kod eklemek yerine *DatasetName*. Dataset.Designer dosyası). Kısmi sınıflar arasında birden çok fiziksel dosyaları Bölünecek belirli bir sınıf için kod etkinleştirin. Daha fazla bilgi için [kısmi](/dotnet/visual-basic/language-reference/modifiers/partial) veya [kısmi sınıflar ve yöntemler](/dotnet/csharp/programming-guide/classes-and-structs/partial-classes-and-methods).

Veri kümesi tanımında (yazılan veri kümesi) için yapılan değişiklikleri her zaman bir veri kümesini tanımlayan bir kod oluşturulur. Bu kod Ayrıca, herhangi bir veri kümesinin yapılandırmasını değiştirir Sihirbazı'nı çalıştırılması sırasında değişiklik yaptığınızda oluşturulur. Kodunuzu bir veri kümesi oluşturma işlemi sırasında silinmesini önlemek için veri kümesinin parçalı sınıf dosyası için kodu ekleyin.

Veri kümesini ve TableAdapter kodunu ayırdıktan sonra varsayılan olarak, her proje bir parçalı sınıf dosyasında sonucudur. Adlı bir dosya özgün proje sahip *DatasetName.Designer.vb* (veya *DatasetName.Designer.cs*), TableAdapter kodunu içerir. İçinde belirtilen projeyi **Dataset projesi** özellik adında bir dosya var *DatasetName.DataSet.Designer.vb* (veya *DatasetName.DataSet.Designer.cs*) . Bu dosya, veri kümesi kodunu içerir.

> [!NOTE]
>  Veri kümelerini ve TableAdapter bağdaştırıcılarını ayırdığınızda (ayarlayarak **DataSet projesi** özelliği), projedeki varolan kısmi veri kümesi sınıfları olmaz taşınması otomatik olarak. Var olan veri kümesi kısmi sınıflarının veri kümesi projesine el ile taşınması gerekir.

> [!NOTE]
>  Doğrulama kodu eklenmesi gerektiğinde, yazılmış veri kümesi oluşturmak için işlevsellik sağlar. <xref:System.Data.DataTable.ColumnChanging> ve <xref:System.Data.DataTable.RowChanging> olay işleyicileri. Daha fazla bilgi için [bir n katmanlı bir veri kümesine doğrulama ekleme](../data-tools/add-validation-to-an-n-tier-dataset.md).

## <a name="to-add-code-to-datasets-in-n-tier-applications"></a>N katmanlı uygulamalarda veri kümelerine kod ekleme

1. İçeren proje bulun *.xsd* dosya.

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

- [N katmanlı veri uygulamalarına genel bakış](../data-tools/n-tier-data-applications-overview.md)
- [N katmanlı uygulamalarda TableAdapter’lara kod ekleme](../data-tools/add-code-to-tableadapters-in-n-tier-applications.md)
- [TableAdapter’lar oluşturma ve yapılandırma](create-and-configure-tableadapters.md)
- [Hiyerarşik güncelleştirmeye genel bakış](hierarchical-update.md)
- [Visual Studio'daki veri kümesi araçları](../data-tools/dataset-tools-in-visual-studio.md)