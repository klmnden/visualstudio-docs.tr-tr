---
title: Tasarımcıya eklemekte olduğunuz nesneler, tasarımcının kullanmakta olduğundan farklı bir veri bağlantısı kullanıyor
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 332ed2f3-3377-4d51-8e3b-fdb98231978e
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 23abfbdc1b0bf922e3d15f0181afd7d01aa7ee2f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53935664"
---
# <a name="the-objects-you-are-adding-to-the-designer-use-a-different-data-connection-than-the-designer"></a>Tasarımcıya eklemekte olduğunuz nesneler Tasarımcı değerinden farklı bir veri bağlantısı kullanın.

Tasarımcıya eklemekte olduğunuz nesneler, tasarımcının kullanmakta olduğundan farklı bir veri bağlantısı kullanın. Tasarımcı tarafından kullanılmakta bağlantıyı değiştirmek istiyor musunuz?

Öğeleri eklediğinizde **Object Relational Designer** (**O/R Tasarımcısı**), tüm öğeleri bir paylaşılan veri bağlantısı kullanıyor. (Tasarım yüzeyini temsil eden <xref:System.Data.Linq.DataContext>, çalışma yüzeyinde tüm nesneleri için tek bir bağlantı kullanır.) Bir nesne tasarımcı tarafından kullanılmakta veri bağlantısı farklı bir veri bağlantısı kullanıyor tasarımcıya eklerseniz, bu ileti görünür. Bu hatayı gidermek için var olan bağlantıyı korumak seçebilirsiniz. Bu seçim yapın, seçili nesnenin eklenmeyecek. Alternatif olarak, nesneyi eklemek ve sıfırlamak seçebilirsiniz <xref:System.Data.Linq.DataContext> yeni bağlantı için bağlantı.

> [!NOTE]
> Tıklarsanız **Evet**, tüm varlık sınıfları üzerinde **O/R Tasarımcısı** yeni bağlantı eşlenir.

## <a name="to-replace-the-existing-connection-with-the-connection-used-by-the-selected-object"></a>Seçilen nesne tarafından kullanılan bağlantı var olan bağlantıyı değiştirmek için

- **Evet**'i tıklayın.

    Seçili nesneyi eklenir **O/R Tasarımcısı**ve *DataContext.Connection* yeni bir bağlantı ayarlanmadı.

## <a name="to-continue-to-use-the-existing-connection-and-cancel-adding-the-selected-object"></a>Var olan bağlantıyı kullanın ve seçili nesne eklemeyi iptal etmek devam etmek için

- **Hayır**'a tıklayın.

    Eylemi iptal edildi. *DataContext.Connection* kalır, varolan bağlantı ayarlayın.

## <a name="see-also"></a>Ayrıca bkz.

- [O/R Tasarımcısı iletileri](../data-tools/o-r-designer-messages.md)
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
