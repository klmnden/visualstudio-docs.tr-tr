---
title: Bir DataContext yöntemin dönüş türünü değiştirme işlemi geri alınamaz
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 76b161fc-5075-4192-8d94-f15b02e199e9
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: e133a609b8e3a0b8b47d0c2ea7408d7c3e9bd9c3
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53947783"
---
# <a name="changing-the-return-type-of-a-datacontext-method-cannot-be-undone"></a>Bir DataContext yöntemin dönüş türünü değiştirme işlemi geri alınamaz

Bir DataContext yönteminin dönüş türünün değiştirilmesi geri alınamaz bir işlemdir. Otomatik olarak üretilen türe geri dönmek için öğe sürüklemeden **Sunucu Gezgini** veya **veritabanı Gezgini** O/R Tasarımcısı yeniden sürükleyin. Dönüş türünü değiştirmek istediğinizden emin misiniz?

Dönüş türü bir <xref:System.Data.Linq.DataContext> yöntemi öğenin nereden bırakın bağlı olarak farklılık gösterir [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)]. Bir öğeyi doğrudan mevcut bir varlık sınıfı üzerine sürükleyip bıraktığınızda bir <xref:System.Data.Linq.DataContext> varlık sınıfı için dönüş türüne sahip bir yöntem oluşturulur. Boş bir alanının bir öğeyi bırak varsa [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)], <xref:System.Data.Linq.DataContext> otomatik olarak oluşturulan bir tür döndüren yöntem oluşturulur. Dönüş türünü değiştirebilirsiniz bir <xref:System.Data.Linq.DataContext> yöntemleri bölmesine ekledikten sonra yöntemi. İnceleme veya dönüş türünü değiştirmek için bir <xref:System.Data.Linq.DataContext> yöntemi seçin ve **dönüş türü** özelliğinde **özellikleri** penceresi.

## <a name="to-change-the-return-type-of-a-datacontext"></a>Bir DataContext dönüş türünü değiştirmek için

- **Evet**'i tıklayın.

## <a name="to-exit-the-message-box-and-leave-the-return-type-unchanged"></a>İleti kutusu çıkmak ve dönüş türü değiştirmeden bırakmak için

- **Hayır**'a tıklayın.

## <a name="to-revert-to-the-original-return-type-after-changing-the-return-type"></a>Dönüş türü değiştirildikten sonra orijinal dönüş türüne geri almak için

1. Seçin <xref:System.Data.Linq.DataContext> metodunda [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)] ve silin.

2. Öğeyi bulun **Sunucu Gezgini/veritabanı Gezgini** ve sürüklediğinizde [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)].

    A <xref:System.Data.Linq.DataContext> yöntemi, özgün varsayılan dönüş türüyle oluşturulur.

## <a name="see-also"></a>Ayrıca bkz.

- [O/R Tasarımcısı iletileri](../data-tools/o-r-designer-messages.md)
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)