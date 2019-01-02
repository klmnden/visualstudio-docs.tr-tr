---
title: Desteklenmeyen bir veritabanı sağlayıcısından bir veritabanı nesnesi seçtiniz
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: c0f1298e-31aa-471e-ae19-1bafffd2ae40
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 4efaf92c9f4688d6870c1152be27eb4c8f4ed933
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53894447"
---
# <a name="you-have-selected-a-database-object-from-an-unsupported-database-provider"></a>Desteklenmeyen bir veritabanı sağlayıcısından bir veritabanı nesnesi seçtiniz

**O/R Tasarımcısı** yalnızca .NET Framework veri sağlayıcısı için SQL Server destekler (<xref:System.Data.SqlClient>). Tıklayabilirsiniz ancak **Tamam** ve desteklenmeyen bir veritabanı sağlayıcısından nesnelerle çalışmaya devam etmek için çalışma zamanında beklenmeyen davranışlarla karşılaşabilirsiniz.

> [!NOTE]
> SQL Server için .NET Framework veri sağlayıcısı kullanan veri bağlantıları desteklenir.

## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

- **Tamam**'ı tıklatın.

   Desteklenmeyen veritabanı sağlayıcısı kullanan bağlantı harita varlık sınıfları tasarlama devam edebilirsiniz. Desteklenmeyen veritabanı sağlayıcıları kullandığınızda beklenmeyen davranışlarla karşılaşabilirsiniz.

    -veya-

- Tıklayın **iptal**.

   İşlem durduruldu. Oluşturun veya SQL Server için .NET Framework sağlayıcısı kullanan bir veri bağlantısı kullanıyor.

## <a name="see-also"></a>Ayrıca bkz.

- [O/R Tasarımcısı iletileri](../data-tools/o-r-designer-messages.md)
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)