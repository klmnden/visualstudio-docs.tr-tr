---
title: Bir veri kümesini doldururken kısıtlamaları kapatma
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- DataRow.BeginEdit
- DataRow.EndEdit
- DataRow.CancelEdit
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- updating datasets, constraints
- constraints [Visual Basic], datasets
- datasets [Visual Basic], constraints
- constraints [Visual Basic], suspending during dataset update
ms.assetid: 553f7d0c-2faa-4c17-b226-dd02855bf1dc
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 9aca29de7e9c5a01e0c2caad2c42015cd31b3f75
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62565192"
---
# <a name="turn-off-constraints-while-filling-a-dataset"></a>Bir veri kümesini doldururken kısıtlamaları kapatma

Bir veri kümesi (örneğin, yabancı anahtar kısıtlamaları) kısıtlamaları içeriyorsa, bunlar sıra veri kümesinde gerçekleştirilen işlemleri ilgili hataları yükseltebilirsiniz. Örneğin, alt kayıtları yüklemeden önce yükleme üst kayıtlar bir kısıtlamayı ihlal ve hataya neden ilgili. Alt kayıt yük hemen sonra kısıtlaması ilgili üst kaydını denetler ve bir hata oluşturur.

Geçici kısıtlaması askıya alma izin vermek için bir mekanizma bulunmadığından varsa, alt tabloya bir kayıt yüklemeye çalıştığınız her zaman bir hata oluşturulması. Bir veri kümesindeki tüm kısıtlamalar askıya almak için başka bir yöntem, <xref:System.Data.DataRow.BeginEdit%2A>, ve <xref:System.Data.DataRow.EndEdit%2A> özellikleri.

> [!NOTE]
> Doğrulama olayları (örneğin, <xref:System.Data.DataTable.ColumnChanging> ve <xref:System.Data.DataTable.RowChanging>) kısıtlamaları devre dışı bırakıldığında oluşturulmaz.

## <a name="to-suspend-update-constraints-programmatically"></a>Güncelleştirme kısıtlamaları programlı olarak askıya alma

- Aşağıdaki örnek, bir veri kümesinde denetleme kısıtlaması geçici olarak kapatmak gösterilmektedir:

     [!code-csharp[VbRaddataEditing#10](../data-tools/codesnippet/CSharp/turn-off-constraints-while-filling-a-dataset_1.cs)]
     [!code-vb[VbRaddataEditing#10](../data-tools/codesnippet/VisualBasic/turn-off-constraints-while-filling-a-dataset_1.vb)]

## <a name="to-suspend-update-constraints-using-the-dataset-designer"></a>Veri kümesi Tasarımcısı'nı kullanarak güncelleştirme kısıtlamaları askıya alma

1. Kümenizde açın **veri kümesi Tasarımcısı**. Daha fazla bilgi için [izlenecek yol: Veri kümesi Tasarımcısı'nda bir veri kümesi oluşturma](walkthrough-creating-a-dataset-with-the-dataset-designer.md).

2. İçinde **özellikleri** penceresinde <xref:System.Data.DataSet.EnforceConstraints%2A> özelliğini `false`.

## <a name="see-also"></a>Ayrıca bkz.

- [TableAdapter'ları kullanarak veri kümelerini doldurma](../data-tools/fill-datasets-by-using-tableadapters.md)
- [Veri kümelerindeki ilişkiler](../data-tools/relationships-in-datasets.md)