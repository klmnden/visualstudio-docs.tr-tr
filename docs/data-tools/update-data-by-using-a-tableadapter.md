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
ms.openlocfilehash: 61ebcd6c833b55f0769365b89274e35136c914f9
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68925342"
---
# <a name="update-data-by-using-a-tableadapter"></a>TableAdapter kullanarak verileri güncelleştirme

Veri kümenizdeki veriler değiştirildikten ve doğrulandıktan sonra, bir `Update` [TableAdapter](../data-tools/create-and-configure-tableadapters.md)metodunu çağırarak güncelleştirilmiş verileri bir veritabanına geri gönderebilirsiniz. Yöntemi, tek bir veri tablosunu güncelleştirir ve tablodaki her bir veri satırının temelinde <xref:System.Data.DataRow.RowState%2A> doğru komutu (INSERT, Update veya delete) çalıştırır. `Update` Bir veri kümesinde ilgili tablolar olduğunda Visual Studio, güncelleştirmeleri yapmak için kullandığınız bir TableAdapterManager sınıfı oluşturur. TableAdapterManager sınıfı, güncelleştirmelerin veritabanında tanımlanan yabancı anahtar kısıtlamalarına göre doğru sırada yapılmasını sağlar. Veriye dayalı denetimleri kullandığınızda, veri bağlama mimarisi tableAdapterManager adlı TableAdapterManager sınıfının bir üye değişkenini oluşturur.

> [!NOTE]
> Bir veri kaynağını bir veri kümesinin içeriğiyle güncelleştirmeyi denediğinizde, hata alabilirsiniz. Hataları önlemek için, `Update` bağdaştırıcının yöntemini çağıran kodu bir `try` / `catch` blok içinde koymanız önerilir.

Bir veri kaynağını güncelleştirmeye yönelik tam yordam, iş ihtiyaçlarına bağlı olarak farklılık gösterebilir, ancak aşağıdaki adımları içerir:

1. Bir `Update` bloktabağdaştırıcının`try`yönteminiçağırın. / `catch`

2. Bir özel durum yakalanmışsa, hataya neden olan veri satırını bulun.

3. Veri satırındaki sorunu uzlaştırır (veya mümkünse, Kullanıcı tarafından değişiklik için geçersiz satırı sunarak) ve sonra güncelleştirmeyi yeniden deneyin (<xref:System.Data.DataRow.HasErrors%2A>, <xref:System.Data.DataTable.GetErrors%2A>).

## <a name="save-data-to-a-database"></a>Verileri bir veritabanına kaydetme

`Update` TableAdapter metodunu çağırın. Veritabanına yazılacak değerleri içeren veri tablosunun adını geçirin.

### <a name="to-update-a-database-by-using-a-tableadapter"></a>TableAdapter kullanarak bir veritabanını güncelleştirmek için

- TableAdapter`Update` metodunu bir `try` bloktaçevrelemek`catch` . / Aşağıdaki örnek `Customers` , içindeki `NorthwindDataSet` tablosunun içeriğini bir `try` / blokiçindennasılgüncelleşleyeceğinizigösterir`catch` .

     [!code-csharp[VbRaddataSaving#9](../data-tools/codesnippet/CSharp/update-data-by-using-a-tableadapter_1.cs)]
     [!code-vb[VbRaddataSaving#9](../data-tools/codesnippet/VisualBasic/update-data-by-using-a-tableadapter_1.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- [Verileri yeniden veritabanına kaydetme](../data-tools/save-data-back-to-the-database.md)