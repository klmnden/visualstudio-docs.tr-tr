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
ms.openlocfilehash: c79492c69f10d97c246d0d56b013fba5af17ec54
ms.sourcegitcommit: 5a65ca6688a2ebb36564657d2d73c4b4f2d15c34
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54204011"
---
# <a name="this-related-method-is-the-backing-method-for-the-following-default-insert-update-or-delete-methods"></a>Bu ilgili metot, aşağıdaki varsayılan ekleme, güncelleştirme ve silme metotları için yedek bir metottur

Bu yöntem için aşağıdaki varsayılan yedekleme yöntemidir ilgili `Insert`, `Update`, veya `Delete` yöntemleri. Silinirse, bu yöntemler de silinir. Devam etmek istiyor musunuz?

Seçili `DataContext` yöntemi şu anda kullanılan biri olarak `Insert`, `Update`, veya `Delete` yöntemleri üzerinde varlık sınıflarının biri için **O/R Tasarımcısı**. Seçili yöntemi nedenlerini silme INSERT işleminin gerçekleştirilmesi için varsayılan çalışma zamanı davranışını geri dönmek için bu yöntemi kullanan varlık sınıfı, güncelleştirme veya silme güncelleştirme sırasında.

## <a name="selected-method-options"></a>Seçili yöntem seçenekleri

- Çalışma zamanı güncelleştirmeleri kullanacak şekilde varlık sınıfı neden seçilen yöntemi silmek için tıklayın **Evet**.

   Seçilen yöntemi silinir ve bu yöntem Güncelleştirme davranışı geçersiz kılma için kullanılan tüm sınıflar SQL çalışma zamanı davranışı için varsayılan LINQ kullanmaya geri alınır.

- Değişmedi, seçilen yöntemi bırakarak ileti kutusunu kapatmak için **Hayır**.

   İleti kutusu kapanır ve hiçbir değişiklik yapılmaz.

## <a name="see-also"></a>Ayrıca bkz.

- [O/R Tasarımcısı iletileri](../data-tools/o-r-designer-messages.md)
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)