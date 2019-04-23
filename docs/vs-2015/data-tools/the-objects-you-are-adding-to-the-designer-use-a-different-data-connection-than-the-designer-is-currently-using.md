---
title: Tasarımcıya eklemekte olduğunuz nesneler tasarımcının kullanmakta farklı bir veri bağlantısı kullanıyor | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
ms.assetid: 332ed2f3-3377-4d51-8e3b-fdb98231978e
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 960d3123c45e44b2b1cdc64b896b15b82e655bb2
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60102851"
---
# <a name="the-objects-you-are-adding-to-the-designer-use-a-different-data-connection-than-the-designer-is-currently-using"></a>Tasarımcıya eklemekte olduğunuz nesneler, tasarımcının kullanmakta olduğundan farklı bir veri bağlantısı kullanıyor
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Tasarımcıya eklemekte olduğunuz nesneler, tasarımcının kullanmakta olduğundan farklı bir veri bağlantısı kullanın. Tasarımcı tarafından kullanılmakta bağlantıyı değiştirmek istiyor musunuz?  
  
 Öğeleri eklediğinizde [!INCLUDE[vs_ordesigner_long](../includes/vs-ordesigner-long-md.md)] ([!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)]), tüm öğeleri bir paylaşılan veri bağlantısı kullanıyor. (Tasarım yüzeyini temsil eden <xref:System.Data.Linq.DataContext>, çalışma yüzeyinde tüm nesneleri için tek bir bağlantı kullanır.) Bir nesne tasarımcı tarafından kullanılmakta veri bağlantısı farklı bir veri bağlantısı kullanıyor tasarımcıya eklerseniz, bu ileti görünür. Bu hatayı gidermek için var olan bağlantıyı korumak seçebilirsiniz. Bu seçim yapın, seçili nesnenin eklenmeyecek. Alternatif olarak, nesneyi eklemek ve sıfırlamak seçebilirsiniz <xref:System.Data.Linq.DataContext> yeni bağlantı için bağlantı.  
  
> [!NOTE]
>  Tıklarsanız **Evet**, tüm varlık sınıfları üzerinde [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)] yeni bağlantı eşlenir.  
  
### <a name="to-replace-the-existing-connection-with-the-connection-used-by-the-selected-object"></a>Seçilen nesne tarafından kullanılan bağlantı var olan bağlantıyı değiştirmek için  
  
- **Evet**'i tıklayın.  
  
     Seçili nesne için eklenen [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)], ve yeni bağlantı DataContext.Connection ayarlanır.  
  
### <a name="to-continue-to-use-the-existing-connection-and-cancel-adding-the-selected-object"></a>Var olan bağlantıyı kullanın ve seçili nesne eklemeyi iptal etmek devam etmek için  
  
- **Hayır**'a tıklayın.  
  
     Eylemi iptal edildi. Var olan bir bağlantı DataContext.Connection kalır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [LINQ to SQL araçlarını Visual Studio'da](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [LINQ to SQL](http://msdn.microsoft.com/library/73d13345-eece-471a-af40-4cc7a2f11655)   