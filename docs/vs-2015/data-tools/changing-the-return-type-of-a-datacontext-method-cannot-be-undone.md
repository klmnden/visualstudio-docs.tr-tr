---
title: Bir DataContext yönteminin dönüş türünün değiştirilmesi geri alınamaz | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
ms.assetid: 76b161fc-5075-4192-8d94-f15b02e199e9
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: d3b94b70db49903e41d26ac0f1382eaa2826e31a
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60059763"
---
# <a name="changing-the-return-type-of-a-datacontext-method-cannot-be-undone"></a>Bir DataContext yöntemin dönüş türünü değiştirme işlemi geri alınamaz
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir DataContext yönteminin dönüş türünün değiştirilmesi geri alınamaz bir işlemdir. Otomatik olarak üretilen türe geri dönmek için öğenin Sunucu Gezgini/veritabanı Gezgini O/R Tasarımcısı üzerine yeniden sürüklemeniz gerekir. Dönüş türünü değiştirmek istediğinizden emin misiniz?  
  
 Dönüş türü bir <xref:System.Data.Linq.DataContext> yöntemi öğenin nereden bırakın bağlı olarak farklılık gösterir [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)]. Bir öğeyi doğrudan mevcut bir varlık sınıfı üzerine sürükleyip bıraktığınızda bir <xref:System.Data.Linq.DataContext> varlık sınıfı için dönüş türüne sahip bir yöntem oluşturulur. Boş bir alanının bir öğeyi bırak varsa [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)], <xref:System.Data.Linq.DataContext> otomatik olarak oluşturulan bir tür döndüren yöntem oluşturulur. Dönüş türünü değiştirebilirsiniz bir <xref:System.Data.Linq.DataContext> yöntemleri bölmesine ekledikten sonra yöntemi. İnceleme veya dönüş türünü değiştirmek için bir <xref:System.Data.Linq.DataContext> yöntemi seçin ve **dönüş türü** özelliğinde **özellikleri** penceresi.  
  
### <a name="to-change-the-return-type-of-a-datacontext"></a>Bir DataContext dönüş türünü değiştirmek için  
  
- **Evet**'i tıklayın.  
  
### <a name="to-exit-the-message-box-and-leave-the-return-type-unchanged"></a>İleti kutusu çıkmak ve dönüş türü değiştirmeden bırakmak için  
  
- **Hayır**'a tıklayın.  
  
### <a name="to-revert-to-the-original-return-type-after-changing-the-return-type"></a>Dönüş türü değiştirildikten sonra orijinal dönüş türüne geri almak için  
  
1. Seçin <xref:System.Data.Linq.DataContext> metodunda [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)] ve silin.  
  
2. Öğeyi bulun **Sunucu Gezgini/veritabanı Gezgini** ve sürüklediğinizde [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)].  
  
     A <xref:System.Data.Linq.DataContext> yöntemi, özgün varsayılan dönüş türüyle oluşturulur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [LINQ to SQL araçlarını Visual Studio'da](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [DataContext yöntemi (O/R Tasarımcısı)](../data-tools/datacontext-methods-o-r-designer.md)   
 [Nasıl yapılır: Saklı yordamları ve işlevleri (O/R Tasarımcısı) için eşlenen DataContext-metotları oluşturma](../data-tools/how-to-create-datacontext-methods-mapped-to-stored-procedures-and-functions-o-r-designer.md)   
 [LINQ to SQL](http://msdn.microsoft.com/library/73d13345-eece-471a-af40-4cc7a2f11655)
