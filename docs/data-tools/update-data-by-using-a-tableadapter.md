---
title: TableAdapter kullanarak verileri güncelleştirme
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- data [Visual Studio], saving
- data [Visual Studio], TableAdapters
- updating data, TableAdapters
- TableAdapters, updating data
- data [Visual Studio], updating
- saving data
ms.assetid: 5e32e10e-9bac-4969-9bdd-b8f6919d3516
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: ca5161d0ddb73a72b88f36e85bda9206839aec3d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62565866"
---
# <a name="update-data-by-using-a-tableadapter"></a>TableAdapter kullanarak verileri güncelleştirme

Veri kümenizdeki verileri değiştiren ve doğrulanmış sonra güncelleştirilen verileri bir veritabanına geri çağırarak gönderebilirsiniz `Update` yöntemi bir [TableAdapter](../data-tools/create-and-configure-tableadapters.md). `Update` Yöntemi tek bir veri tablosunu güncelleştirir ve göre doğru komutu (INSERT, UPDATE veya DELETE) çalıştıran <xref:System.Data.DataRow.RowState%2A> tablodaki her veri satırının. Bir veri kümesi ilişkili tabloları, Visual Studio güncelleştirmeleri yapmak için kullandığınız bir TableAdapterManager sınıfı oluşturur. TableAdapterManager sınıfı veritabanında tanımlanan yabancı anahtar kısıtlamaları göre doğru sırada güncelleştirmeler yapılmasını sağlar. Verilere bağlı denetimler kullandığınızda, veri bağlama mimarisi tableAdapterManager adlı TableAdapterManager sınıfın üye değişkeni oluşturur.

> [!NOTE]
> Bir veri kümesi içeriği ile bir veri kaynağını güncelleştirmek çalıştığınızda hatalar alabilirsiniz. Hataları önlemek için bağdaştırıcının çağıran kodu koymanızı öneririz `Update` yöntem içinde bir `try` / `catch` blok.

 Tam bir veri kaynağını güncelleştirme yordamı, iş gereksinimlerinize bağlı olarak farklılık gösterebilir, ancak aşağıdaki adımları içerir:

1. Bağdaştırıcının çağrı `Update` yönteminde bir `try` / `catch` blok.

2. Bir özel durum yakalandığında, hataya neden olan veri satırı bulun.

3. Sorun verilerinde mutabakat (program aracılığıyla yapabilirsiniz veya kullanıcıya değiştirilmesi için geçersiz satır sunarak) öğesini ve ardından güncelleştirmeyi yeniden deneyin (<xref:System.Data.DataRow.HasErrors%2A>, <xref:System.Data.DataTable.GetErrors%2A>).

## <a name="save-data-to-a-database"></a>Verileri bir veritabanına kaydetme

Çağrı `Update` TableAdapter bağdaştırıcısının yöntemi. Veritabanına yazılmak için değerleri içeren veri tablosunun adı geçirin.

### <a name="to-update-a-database-by-using-a-tableadapter"></a>Bir TableAdapter'ı kullanarak bir veritabanını güncelleştirmek için

- TableAdapter bağdaştırıcısının içine`Update` yönteminde bir `try` / `catch` blok. Aşağıdaki örnek, içeriği güncelleştirmek gösterilmektedir `Customers` tablosundaki `NorthwindDataSet` içinden bir `try` / `catch` blok.

     [!code-csharp[VbRaddataSaving#9](../data-tools/codesnippet/CSharp/update-data-by-using-a-tableadapter_1.cs)]
     [!code-vb[VbRaddataSaving#9](../data-tools/codesnippet/VisualBasic/update-data-by-using-a-tableadapter_1.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- [Verileri yeniden veritabanına kaydetme](../data-tools/save-data-back-to-the-database.md)