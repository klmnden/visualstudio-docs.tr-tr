---
title: Bu yöntemi, aşağıdaki varsayılan ekleme, güncelleştirme veya silme yöntemleri için destek yöntemidir ilgili | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
ms.assetid: 62afa6da-97cf-48b9-8de3-33e4d72a0377
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 8229eaa612675f949d716477eda4627840dfca89
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54772119"
---
# <a name="this-related-method-is-the-backing-method-for-the-following-default-insert-update-or-delete-methods"></a>Bu ilgili metot, aşağıdaki varsayılan ekleme, güncelleştirme ve silme metotları için yedek bir metottur
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Bu ilgili metot, aşağıdaki varsayılan ekleme, güncelleştirme veya silme yöntemleri için destek yöntemidir. Silinirse, bu yöntemler de silinir. Devam etmek istiyor musunuz?  
  
 Seçili `DataContext` yöntemi şu anda kullanılan INSERT, Update veya Delete yöntemlerinden biri olarak O/R Tasarımcısı'ndaki varlık sınıflarının biri için. Seçilen yöntemi silme INSERT, Update, gerçekleştirmek için varsayılan çalışma zamanı davranışını geri dönmek için bu yöntemi kullanan varlık sınıfı neden veya güncelleştirme sırasında silin.  
  
### <a name="to-delete-the-selected-method-causing-the-entity-class-to-use-runtime-updates"></a>Çalışma zamanı güncelleştirmeleri kullanacak şekilde varlık sınıfı neden seçilen yöntemi silmek için  
  
-   **Evet**'i tıklayın.  
  
     Seçilen yöntemi silinir ve bu yöntem Güncelleştirme davranışı geçersiz kılma için kullanılan tüm sınıflar SQL çalışma zamanı davranışı için varsayılan LINQ kullanmaya geri alınır.  
  
### <a name="to-close-the-message-box-leaving-the-selected-method-unchanged"></a>İleti kutusunu kapatmak için seçilen yöntemi değişmeden  
  
-   **Hayır**'a tıklayın.  
  
     İleti kutusu kapanır ve hiçbir değişiklik yapılmaz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [DataContext yöntemi (O/R Tasarımcısı)](../data-tools/datacontext-methods-o-r-designer.md)   
 [Nasıl yapılır: Güncelleştirme, ekleme ve silme (O/R Tasarımcısı) gerçekleştirmek için saklı yordamlar atama](../data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer.md)   
 [LINQ to SQL araçlarını Visual Studio'da](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [LINQ to SQL](http://msdn.microsoft.com/library/73d13345-eece-471a-af40-4cc7a2f11655)
