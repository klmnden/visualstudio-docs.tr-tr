---
title: Seçilen sınıf bir veya birden çok DataContext yöntemi için bir dönüş türü olarak kullanıldığından silinemiyor
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: d68254a0-f3a1-47e2-aed3-a83471e1d711
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 36ad2afe48b5af06bf7ee59fa3043221bc787ba6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53988981"
---
# <a name="the-selected-class-cannot-be-deleted-because-it-is-used-as-a-return-type-for-one-or-more-datacontext-methods"></a>Seçilen sınıf bir veya birden çok DataContext yöntemi için bir dönüş türü olarak kullanıldığından silinemiyor

Dönüş türü bir veya daha fazla <xref:System.Data.Linq.DataContext> yöntemleri, seçilen varlığın sınıftır. Silme için dönüş türü olarak kullanılacak bir varlık sınıfı bir <xref:System.Data.Linq.DataContext> yöntemi derleme projenin başarısız olmasına neden olur. Seçilen varlık sınıfını silmek için tanımlamak <xref:System.Data.Linq.DataContext> yöntemleri kullanmak ve dönüş türleri farklı varlık sınıfa ayarlayın.

Geri dönüş türleri <xref:System.Data.Linq.DataContext> kendi özgün otomatik olarak oluşturulan türler, yöntemlere silin <xref:System.Data.Linq.DataContext> yönteminden **yöntemleri** bölmesi ve sonra nesneyi sürükleyin **Sunucu Gezgini** / **Veritabanı Gezgini** üzerine **O/R Tasarımcısı** yeniden.

## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

1. Tanımlamak <xref:System.Data.Linq.DataContext> varlık sınıfı seçerek bir dönüş türü olarak kullanan yöntemleri bir <xref:System.Data.Linq.DataContext> yönteminde **yöntemleri** bölmesi ve İnceleme **dönüş türü** özelliğinde**Özellikleri** penceresi.

2. Ayarlama **dönüş türü** farklı varlık sınıfı ya da silme <xref:System.Data.Linq.DataContext> yöntemleri bölmesinden yöntemi.

## <a name="see-also"></a>Ayrıca bkz.

- [O/R Tasarımcısı iletileri](../data-tools/o-r-designer-messages.md)
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)