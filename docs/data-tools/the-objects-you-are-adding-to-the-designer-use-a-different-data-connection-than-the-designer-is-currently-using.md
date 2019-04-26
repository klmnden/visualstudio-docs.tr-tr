---
title: Tasarımcıya eklemekte olduğunuz nesneler, tasarımcının kullanmakta olduğundan farklı bir veri bağlantısı kullanıyor
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 332ed2f3-3377-4d51-8e3b-fdb98231978e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 9e0864ec07250ed5886f864d4233aeb902ecf5ae
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62565628"
---
# <a name="the-objects-you-are-adding-to-the-designer-use-a-different-data-connection-than-the-designer"></a>Tasarımcıya eklemekte olduğunuz nesneler Tasarımcı değerinden farklı bir veri bağlantısı kullanın.

Tasarımcıya eklemekte olduğunuz nesneler, tasarımcının kullanmakta olduğundan farklı bir veri bağlantısı kullanın. Tasarımcı tarafından kullanılmakta bağlantıyı değiştirmek istiyor musunuz?

Öğeleri eklediğinizde **Object Relational Designer** (**O/R Tasarımcısı**), tüm öğeleri bir paylaşılan veri bağlantısı kullanıyor. (Tasarım yüzeyini temsil eden <xref:System.Data.Linq.DataContext>, çalışma yüzeyinde tüm nesneleri için tek bir bağlantı kullanır.) Bir nesne tasarımcı tarafından kullanılmakta veri bağlantısı farklı bir veri bağlantısı kullanıyor tasarımcıya eklerseniz, bu ileti görünür. Bu hatayı gidermek için var olan bağlantıyı korumak seçebilirsiniz. Bu seçim yapın, seçili nesnenin eklenmeyecek. Alternatif olarak, nesneyi eklemek ve sıfırlamak seçebilirsiniz <xref:System.Data.Linq.DataContext> yeni bağlantı için bağlantı.

## <a name="connection-options"></a>Bağlantı seçenekleri

- Seçilen nesne tarafından kullanılan bağlantı ile var olan bağlantıyı değiştirmek için tıklayın **Evet**.

   Seçili nesneyi eklenir **O/R Tasarımcısı**ve *DataContext.Connection* yeni bir bağlantı ayarlanmadı.

   > [!NOTE]
   > Tıklarsanız **Evet**, tüm varlık sınıfları üzerinde **O/R Tasarımcısı** yeni bağlantı eşlenir.

- Seçili nesne eklemeyi iptal ve varolan bir bağlantıyı kullanmaya devam etmek için tıklayın **Hayır**.

   Eylemi iptal edildi. *DataContext.Connection* kalır, varolan bağlantı ayarlayın.

## <a name="see-also"></a>Ayrıca bkz.

- [O/R Tasarımcısı iletileri](../data-tools/o-r-designer-messages.md)
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
