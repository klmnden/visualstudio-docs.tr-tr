---
title: TableAdapter kullanarak verileri güncelleştirmek | Microsoft Docs
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
- data [Visual Studio], saving
- data [Visual Studio], TableAdapters
- updating data, TableAdapters
- TableAdapters, updating data
- data [Visual Studio], updating
- saving data
ms.assetid: 5e32e10e-9bac-4969-9bdd-b8f6919d3516
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 30d1fd3ee211d6b30f435104a2e2f9b42ed100c0
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65692341"
---
# <a name="update-data-by-using-a-tableadapter"></a>TableAdapter kullanarak verileri güncelleştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Veri kümenizdeki verileri değiştiren ve doğrulandı sonra güncelleştirilen verileri bir databaseby çağırmaya gönderebilirsiniz `Update` TableAdapter bağdaştırıcısının yöntemi. `Update` Yöntemi tek bir veri tablosunu güncelleştirir ve göre doğru komutu (INSERT, UPDATE veya DELETE) çalıştıran <xref:System.Data.DataRow.RowState%2A> tablodaki her veri satırının. Bir veri kümesi ilişkili tabloları, Visual Studio güncelleştirmeleri yapmak için kullandığınız bir TableAdapterManager sınıfı oluşturur. TableAdapterManager sınıfı veritabanında tanımlanan yabancı anahtar kısıtlamaları göre doğru sırada güncelleştirmeler yapılmasını sağlar. Verilere bağlı denetimler kullandığınızda, veri bağlama mimarisi tableAdapterManager adlı TableAdapterManager sınıfın üye değişkeni oluşturur. Daha fazla bilgi için [hiyerarşik güncelleştirme genel bakış](https://msdn.microsoft.com/library/c4f8e8b9-e4a5-4a02-8462-d03d1e8222d6).  
  
> [!NOTE]
> Bir veri kümesi içeriği ile bir veri kaynağını güncelleştirmek çalıştığınızda hatalar alabilirsiniz. Hataları önlemek için kutusu yerleştirin bağdaştırıcının çağıran kodu öneririz `Update` yöntem içinde bir `try` / `catch` blok.  
  
 Tam bir veri kaynağını güncelleştirme yordamı, iş gereksinimlerinize bağlı olarak farklılık gösterebilir, ancak aşağıdaki adımları içerir:  
  
1. Bağdaştırıcının çağrı `Update` yönteminde bir `try` / `catch` blok.  
  
2. Bir özel durum yakalandığında, hataya neden olan veri satırı bulun. Daha fazla bilgi için [nasıl yapılır: Hatalar içeren satırların bulun](https://msdn.microsoft.com/library/1fa907c5-fe66-4f29-a253-2b97b900050c).  
  
3. Sorun verilerinde mutabakat (program aracılığıyla yapabilirsiniz veya kullanıcıya değiştirilmesi için geçersiz satır sunarak) öğesini ve ardından güncelleştirmeyi yeniden deneyin (<xref:System.Data.DataRow.HasErrors%2A>, <xref:System.Data.DataTable.GetErrors%2A>).  
  
## <a name="savedata-to-a-database"></a>Bir veritabanına SaveData  
 Çağrı `Update` TableAdapter bağdaştırıcısının yöntemi. Veritabanına yazılmak için değerleri içeren veri tablosunun adı geçirin.  
  
#### <a name="to-update-a-database-by-using-a-tableadapter"></a>Bir TableAdapter'ı kullanarak bir veritabanını güncelleştirmek için  
  
- TableAdapter bağdaştırıcısının içine`Update` yönteminde bir `try` / `catch` blok. Aşağıdaki örnek, içeriği güncelleştirmek gösterilmektedir `Customers` tablosundaki `NorthwindDataSet` içinden bir `try` / `catch` blok.  
  
     [!code-csharp[VbRaddataSaving#9](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataSaving/CS/Form3.cs#9)]
     [!code-vb[VbRaddataSaving#9](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataSaving/VB/Form3.vb#9)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Verileri yeniden veritabanına kaydetme](../data-tools/save-data-back-to-the-database.md)
