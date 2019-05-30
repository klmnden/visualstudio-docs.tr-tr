---
title: Tasarımcıya eklenen nesneler farklı bir veri bağlantısı kullanıyor
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 332ed2f3-3377-4d51-8e3b-fdb98231978e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: c85e0c17eeb4cfbd786faac338c8b908c5a7f363
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66260931"
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

- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
