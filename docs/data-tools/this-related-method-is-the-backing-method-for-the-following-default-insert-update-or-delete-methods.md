---
title: Bu ilgili metot, aşağıdaki varsayılan ekleme, güncelleştirme ve silme metotları için yedek bir metottur
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 62afa6da-97cf-48b9-8de3-33e4d72a0377
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 1b5579c8916e81e3c49e9d6e24bf37ed85039c03
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53851829"
---
# <a name="this-related-method-is-the-backing-method-for-the-following-default-insert-update-or-delete-methods"></a>Bu ilgili metot, aşağıdaki varsayılan ekleme, güncelleştirme ve silme metotları için yedek bir metottur

Bu yöntem için aşağıdaki varsayılan yedekleme yöntemidir ilgili `Insert`, `Update`, veya `Delete` yöntemleri. Silinirse, bu yöntemler de silinir. Devam etmek istiyor musunuz?

Seçili `DataContext` yöntemi şu anda kullanılan biri olarak `Insert`, `Update`, veya `Delete` yöntemleri üzerinde varlık sınıflarının biri için **O/R Tasarımcısı**. Seçili yöntemi nedenlerini silme INSERT işleminin gerçekleştirilmesi için varsayılan çalışma zamanı davranışını geri dönmek için bu yöntemi kullanan varlık sınıfı, güncelleştirme veya silme güncelleştirme sırasında.

## <a name="to-delete-the-selected-method-causing-the-entity-class-to-use-runtime-updates"></a>Çalışma zamanı güncelleştirmeleri kullanacak şekilde varlık sınıfı neden seçilen yöntemi silmek için

- **Evet**'i tıklayın.

    Seçilen yöntemi silinir ve bu yöntem Güncelleştirme davranışı geçersiz kılma için kullanılan tüm sınıflar SQL çalışma zamanı davranışı için varsayılan LINQ kullanmaya geri alınır.

## <a name="to-close-the-message-box-leaving-the-selected-method-unchanged"></a>İleti kutusunu kapatmak için seçilen yöntemi değişmeden

- **Hayır**'a tıklayın.

    İleti kutusu kapanır ve hiçbir değişiklik yapılmaz.

## <a name="see-also"></a>Ayrıca bkz.

- [O/R Tasarımcısı iletileri](../data-tools/o-r-designer-messages.md)
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)