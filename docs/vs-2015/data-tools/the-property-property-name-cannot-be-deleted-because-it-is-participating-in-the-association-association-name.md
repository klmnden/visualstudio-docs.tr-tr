---
title: Özellik &lt;özellik adı&gt; ilişkilendirmesine katıldığından silinemiyor &lt;ilişkilendirme adı&gt; | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
ms.assetid: 389873cc-92dd-48da-bfca-0f6c8e0ae3c2
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 52dc1d42ab8fff879bd290fe1a9c9aa2ca0a08c0
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65700313"
---
# <a name="the-property-ltproperty-namegt-cannot-be-deleted-because-it-is-participating-in-the-association-ltassociation-namegt"></a>Özellik &lt;özellik adı&gt; ilişkilendirmesine katıldığından silinemiyor &lt;ilişkilendirme adı&gt;
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Seçilen özellik olarak ayarlandığından **ilişkilendirme** hata iletisinde belirtilen sınıfları arasında ilişkilendirme için. Veri sınıfları arasında ilişkilendirme katılan varsa özellikleri silinemez.  
  
 Ayarlama **ilişkilendirme** başarılı silinmesini istenen özelliği etkinleştirmek için veri sınıfın farklı bir özellik için.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1. Hata iletisinde belirtilen veri sınıfları bağlanan O/R Tasarımcısı'ndaki ilişkilendirme çizgisi seçin.  
  
2. Satırı açmak için çift tıklatın **ilişkilendirme Düzenleyicisi** iletişim kutusu.  
  
3. Özelliğinden kaldırılacak **ilişkilendirme özellikleri**.  
  
4. Özelliği yeniden silmeyi deneyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [LINQ to SQL araçlarını Visual Studio'da](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [Nasıl yapılır: LINQ to SQL sınıfları (O/R Tasarımcısı) arasındaki ilişkiyi (ilişki) oluşturma](../data-tools/how-to-create-an-association-relationship-between-linq-to-sql-classes-o-r-designer.md)   
 [İzlenecek yol: LINQ to SQL sınıfları (O R Designer) oluşturma](https://msdn.microsoft.com/library/35aad4a4-2e8a-46e2-ae09-5fbfd333c233)   
 [LINQ to SQL](https://msdn.microsoft.com/library/73d13345-eece-471a-af40-4cc7a2f11655)
