---
title: Bir TableAdapter’ın işlevselliğini genişletme
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- data [Visual Studio], TableAdapters
- data [Visual Studio], extending TableAdapters
- TableAdapters, adding functionality
ms.assetid: 418249c8-c7f3-47ef-a94c-744cb6fe6aaf
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: d0ec905670c72ff7c2c5f5d94c9f5189241daebb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62567438"
---
# <a name="extend-the-functionality-of-a-tableadapter"></a>Bir TableAdapter’ın işlevselliğini genişletme

TableAdapter bağdaştırıcısının kısmi sınıf dosyası için kod ekleyerek bir TableAdapter işlevselliğini genişletebilirsiniz.

Düzenleyici içindeki TableAdapter herhangi bir değişiklik yapıldığında bir TableAdapter tanımlayan kod yeniden oluşturulursa **veri kümesi Tasarımcısı**, veya ne zaman bir sihirbaz bir TableAdapter yapılandırmasını değiştirir. Kodunuzu bir TableAdapter oluşturma işlemi sırasında silinmesini önlemek için TableAdapter bağdaştırıcısının kısmi sınıf dosyası için kodu ekleyin.

Kısmi sınıflar arasında birden çok fiziksel dosyaları Bölünecek belirli bir sınıf için kod sağlar. Daha fazla bilgi için [kısmi](/dotnet/visual-basic/language-reference/modifiers/partial) veya [partial (tür)](/dotnet/csharp/language-reference/keywords/partial-type).

## <a name="locate-tableadapters-in-code"></a>TableAdapters kod içinde bulun

TableAdapter'ları ile tasarlandığında **veri kümesi Tasarımcısı**, oluşturulan TableAdapter sınıfları, iç içe sınıfları olmayan <xref:System.Data.DataSet>. TableAdapter'ları, TableAdapter bağdaştırıcısının ilişkili veri kümesinin adına dayalı bir ad alanında bulunur. Örneğin, uygulamanız adlı bir veri içeriyorsa `HRDataSet`, TableAdapter'ları bulunması `HRDataSetTableAdapters` ad alanı. (Bu deseni adlandırma kuralını izler: *DatasetName* + `TableAdapters`).

Aşağıdaki örnekte adlı bir TableAdapter varsayılır `CustomersTableAdapter`içeren bir proje içinde `NorthwindDataSet`.

### <a name="to-create-a-partial-class-for-a-tableadapter"></a>Kısmi bir sınıf için bir TableAdapter oluşturmak için

1. Yeni bir sınıf giderek projenize ekleyin. **proje** menü ve seçerek **sınıfı Ekle**.

2. Sınıf adını `CustomersTableAdapterExtended`.

3. **Add (Ekle)** seçeneğini belirleyin.

4. Kod aşağıdaki gibi doğru ad alanını ve projeniz için kısmi sınıf adı ile değiştirin:

     [!code-csharp[VbRaddataTableAdapters#2](../data-tools/codesnippet/CSharp/extend-the-functionality-of-a-tableadapter_1.cs)]
     [!code-vb[VbRaddataTableAdapters#2](../data-tools/codesnippet/VisualBasic/extend-the-functionality-of-a-tableadapter_1.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- [TableAdapter'ları kullanarak veri kümelerini doldurma](../data-tools/fill-datasets-by-using-tableadapters.md)