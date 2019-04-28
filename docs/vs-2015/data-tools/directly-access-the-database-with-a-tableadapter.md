---
title: Bir TableAdapter ile veritabanına doğrudan erişme | Microsoft Docs
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
- databases [Visual Basic], accessing with a TableAdapter
- DBDirect methods
- datasets [Visual Basic], adding to projects
- data [Visual Studio], saving
- TableAdapter.Delete method
- GenerateDbDirectMethods property
- TableAdapter.Insert method
- TableAdapter.GenerateDBDirectMethods property
- TableAdapter.Update method
- saving data
- TableAdapters
ms.assetid: 012c5924-91f7-4790-b2a6-f51402b7014b
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 924a14cc3938420f32a1a2c25265ebe94e261b15
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63431957"
---
# <a name="directly-access-the-database-with-a-tableadapter"></a>Bir TableAdapter ile veritabanına doğrudan erişme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Ek olarak `InsertCommand`, `UpdateCommand`, ve `DeleteCommand`, TableAdapter'ları doğrudan veritabanında çalıştırılabilen yöntemleri ile oluşturulur. Bu yöntemler (`TableAdapter.Insert`, `TableAdapter.Update`, ve `TableAdapter.Delete`) doğrudan veritabanındaki verileri işlemek için çağrılabilir.  
  
 Bu doğrudan yöntemleri oluşturmak istemiyorsanız TableAdapter bağdaştırıcısının ayarlamak `GenerateDbDirectMethods` özelliğini `false` içinde **özellikleri** penceresi. TableAdapter bağdaştırıcısının ana sorgusunda yanı sıra bir TableAdapter sorguları eklenir, bu DbDirect yöntemleri üretme tek başına sorgulardır değildirler.  
  
## <a name="sendcommandsdirectly-to-a-database"></a>Bir veritabanına Sendcommandsdirectly  
 Gerçekleştirmeye çalıştığınız görevi gerçekleştirir TableAdapter DbDirect yöntemini çağırın.  
  
#### <a name="to-insert-new-records-directly-into-a-database"></a>Doğrudan veritabanına yeni kayıtlar eklemek için  
  
- TableAdapter bağdaştırıcısının çağrı `Insert` değerler her sütun için parametre olarak geçirmeyi yöntemi. Aşağıdaki yordam kullanır `Region` örneği Northwind databaseas tablo.  
  
    > [!NOTE]
    > Kullanmak istediğiniz TableAdapter kullanılabilir bir örnek yoksa örneği.  
  
     [!code-csharp[VbRaddataSaving#15](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataSaving/CS/Class1.cs#15)]
     [!code-vb[VbRaddataSaving#15](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataSaving/VB/Class1.vb#15)]  
  
#### <a name="to-update-records-directly-in-a-database"></a>Doğrudan veritabanındaki kayıtları güncelleştirmek için  
  
- TableAdapter bağdaştırıcısının çağrı `Update` yöntemi, yeni ve orijinal değerleri her sütun için parametre olarak geçirerek.  
  
    > [!NOTE]
    > Kullanmak istediğiniz TableAdapter kullanılabilir bir örnek yoksa örneği.  
  
     [!code-csharp[VbRaddataSaving#18](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataSaving/CS/Class1.cs#18)]
     [!code-vb[VbRaddataSaving#18](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataSaving/VB/Class1.vb#18)]  
  
#### <a name="to-delete-records-directly-from-a-database"></a>Kayıtları doğrudan veritabanından silmek için  
  
- TableAdapter bağdaştırıcısının çağrı `Delete` değerleri her sütun için parametre olarak geçirerek yöntemini `Delete` yöntemi. Aşağıdaki yordam kullanır `Region` örneği Northwind databaseas tablo.  
  
    > [!NOTE]
    > Kullanmak istediğiniz TableAdapter kullanılabilir bir örnek yoksa örneği.  
  
     [!code-csharp[VbRaddataSaving#21](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataSaving/CS/Class1.cs#21)]
     [!code-vb[VbRaddataSaving#21](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataSaving/VB/Class1.vb#21)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [TableAdapter'ları kullanarak veri kümelerini doldurma](../data-tools/fill-datasets-by-using-tableadapters.md)
