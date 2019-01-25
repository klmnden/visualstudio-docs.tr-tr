---
title: Varlıklar arasında ilişkilendirme oluşturma | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.BDC.Association_Dialog
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- BDC [SharePoint development in Visual Studio], create an assocation
- Business Data Connectivity service [SharePoint development in Visual Studio], associations between entities
- BDC [SharePoint development in Visual Studio], associations between entities
- Business Data Connectivity service [SharePoint development in Visual Studio], create an assocation
- Business Data Connectivity service [SharePoint development in Visual Studio], associate external content types
- Business Data Connectivity service [SharePoint development in Visual Studio], relate entities
- BDC [SharePoint development in Visual Studio], relate entities
- BDC [SharePoint development in Visual Studio], associate external content types
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: bf5c914ba998c7690a20d4e1a573f8344f976061
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54870733"
---
# <a name="create-an-association-between-entities"></a>Varlıklar arasında ilişkilendirme oluşturma
  İlişkilendirmeleri oluşturarak iş verileri bağlantısı (BDC) modelinizdeki varlıklar arasında ilişkiler tanımlayabilirsiniz. Visual Studio model tüketicilerinin her ilişkilendirmesi hakkında bilgi sağlayan yöntemler oluşturur. Bu yöntemler, SharePoint web bölümleri, liste veya bir kullanıcı arabirimi (UI) veri ilişkileri görüntülemek için özel uygulamaları tarafından kullanılabilecek.  
  
## <a name="create-an-association"></a>İlişkilendirme oluşturma
 Seçerek ilişkilendirme oluşturun **ilişkilendirme** denetimi Visual Studio'da **araç kutusu**, (kaynak varlık olarak adlandırılır) ilk varlık seçerek ve sonra ikinci bir varlık seçerek (çağırılır Hedef varlık). İlişkilendirmeyi ayrıntılarını tanımlayabilirsiniz **ilişkilendirme Düzenleyicisi**. Daha fazla bilgi için [nasıl yapılır: Varlıklar arasında ilişkilendirme oluşturma](../sharepoint/how-to-create-an-association-between-entities.md).  
  
## <a name="association-methods"></a>İlişkilendirme metotları
 SharePoint iş verileri web bölümlerini gibi uygulamalar, bir varlığın Hizmet sınıfında yöntemleri çağırarak ilişkilerini kullanır. Bunları seçerek bir varlık hizmeti sınıfındaki yöntemleri ekleyebilirsiniz **ilişkilendirme Düzenleyicisi**.  
  
 Varsayılan olarak, **ilişkilendirme Düzenleyicisi** ilişkilendirme Gezinti yöntemi için kaynak ve hedef varlık ekler. Kullanıcıları bir hedef Varlık listesini almak bir kaynak varlık ilişkisi Gezinti yöntemi sağlar. Tüketiciler için bir hedef varlık ilişkili kaynak varlık almak bir hedef varlık ilişkisi Gezinti yöntemi sağlar.  
  
 İlgili bilgileri döndürmek için bu yöntemlerin her biri için kod eklemeniz gerekir. Ayrıca, daha gelişmiş senaryoları desteklemek için yöntemler diğer tür ekleyebilirsiniz. Bu yöntemlerin her biri hakkında daha fazla bilgi için bkz: [desteklenen işlemler](http://go.microsoft.com/fwlink/?LinkId=169286).  
  
## <a name="types-of-associations"></a>Tür ilişkileri
 İki tür ilişkilerini BDC tasarımcısında oluşturabilirsiniz: yabancı anahtar tabanlı ilişkilendirmeleri ve yabancı anahtarsız ilişkileri.  
  
### <a name="foreign-key-based-association"></a>Yabancı anahtar tabanlı ilişkilendirme
 Kaynak varlıktaki tür tanımlayıcıları hedef varlıktaki tanımlanmış tanımlayıcının ilişkilendirilerek bir yabancı anahtar tabanlı ilişkilendirmesi oluşturabilirsiniz. Bu ilişki, kullanıcıları için Gelişmiş bir kullanıcı Arabirimi sağlamak tüketiciler modeli sağlar. Örneğin, kullanıcının açılan listede müşteriler görüntüleyen bir satış siparişi oluşturmasını sağlayan Outlook formunda; veya, bir müşteri için bir profil sayfasını açmak kullanıcıların sağlayan SharePoint satış siparişlerinin listesi.  
  
 Bir yabancı anahtar tabanlı ilişkisi oluşturmak için tanımlayıcılar ilgilidir ve aynı ada ve türe paylaşan tanımlayıcıları yazın. Örneğin, arasında bir yabancı anahtar tabanlı ilişkilendirmesi oluşturabilirsiniz bir `Contact` varlık ve `SalesOrder` varlık. `SalesOrder` Varlık döndürür bir `ContactID` tanımlayıcısı Bulucu veya belirli bir Bulucu yöntemi dönüş parametresinin bir parçası olarak yazın. Her iki tür tanımlayıcısı görünür **ilişkilendirme Düzenleyicisi**. Arasında bir yabancı anahtar tabanlı ilişki oluşturmak için `Contact` varlık ve `SalesOrder` varlığı seçin `ContactID` bu alanların her biri yanındaki tanımlayıcısı.  
  
 Hedef varlık koleksiyonunu döndürür. kaynak varlık ilişkisi Gezgin yöntemine kod ekleyin. Aşağıdaki örnek, bir kişi için satış siparişleri döndürür.  
  
 [!code-csharp[SP_BDC#7](../sharepoint/codesnippet/CSharp/SP_BDC/bdcmodel1/contactservice.cs#7)]
 [!code-vb[SP_BDC#7](../sharepoint/codesnippet/VisualBasic/sp_bdc/bdcmodel1/contactservice.vb#7)]  
  
 Kaynak varlık döndüren bir hedef varlık ilişkisi Gezgin yöntemine kod ekleyin. Aşağıdaki örnek satış siparişi için ilgili kişi döndürür.  
  
 [!code-csharp[SP_BDC#8](../sharepoint/codesnippet/CSharp/SP_BDC/bdcmodel1/salesorderservice.cs#8)]
 [!code-vb[SP_BDC#8](../sharepoint/codesnippet/VisualBasic/sp_bdc/bdcmodel1/salesorderservice.vb#8)]  
  
### <a name="foreign-keyless-association"></a>Yabancı anahtarsız ilişkilendirmesini
 Tanımlayıcıları alanı tür tanımlayıcısı için eşleme olmadan bir ilişki oluşturabilirsiniz. Hedef varlık ile doğrudan bir ilişki kaynak varlık sahip olmadığında bu tür bir ilişki oluşturun. Örneğin, bir `SalesOrderDetail` tablosu birincil anahtarında eşleyen bir yabancı anahtar yok bir `Contact` tablo.  
  
 Bilgileri görüntülenecek istiyorsanız `SalesOrderDetail` ilişkili tablo bir `Contact`, arasındaki bir yabancı anahtarsız ilişkilendirmesini oluşturabilirsiniz `Contact` varlık ve `SalesOrderDetail` varlık.  
  
 İlişkilendirme Gezinti yöntemi içinde `Contact` varlık, dönüş `SalesOrderDetail` varlıkları tabloları birleştirme ya da bir saklı yordamı çağırma.  
  
 Aşağıdaki örnek, tabloları katılarak tüm satış siparişleri ayrıntılarını döndürür.  
  
 [!code-csharp[SP_BDC#9](../sharepoint/codesnippet/CSharp/SP_BDC/bdcmodel1/contactservice.cs#9)]
 [!code-vb[SP_BDC#9](../sharepoint/codesnippet/VisualBasic/sp_bdc/bdcmodel1/contactservice.vb#9)]  
  
 İlişkilendirme Gezinti yöntemi içinde `SalesOrderDetail` varlık, ilgili dönüş `Contact`. Aşağıdaki örnekte bu gösterir.  
  
 [!code-csharp[SP_BDC#10](../sharepoint/codesnippet/CSharp/SP_BDC/bdcmodel1/salesorderdetailservice.cs#10)]
 [!code-vb[SP_BDC#10](../sharepoint/codesnippet/VisualBasic/sp_bdc/bdcmodel1/salesorderdetailservice.vb#10)]  
  
## <a name="see-also"></a>Ayrıca bkz.
 [İş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md)   
 [Nasıl yapılır: Varlıklar arasında ilişkilendirme oluşturma](../sharepoint/how-to-create-an-association-between-entities.md)  
