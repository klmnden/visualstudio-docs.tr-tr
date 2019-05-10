---
title: Seçili bağlantı desteklenmeyen bir veritabanı sağlayıcısı kullanıyor
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 4d25dfa1-8fa4-4529-9b90-973bc2ec2993
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 5fab6be50a9b4c273a7bb911d8afde5cf65d7676
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65460580"
---
# <a name="the-selected-connection-uses-an-unsupported-database-provider"></a>Seçili bağlantı desteklenmeyen bir veritabanı sağlayıcısı kullanıyor

Bu ileti, SQL Server için .NET Framework veri sağlayıcısı kullanmayan öğelerini sürükleyip bırakırken görünür **Sunucu Gezgini** veya **veritabanı Gezgini** üzerine [görselde LINQ to SQL araçları Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md).

**O/R Tasarımcısı** SQL Server için .NET Framework sağlayıcısını kullanan veri bağlantılarını destekler. Microsoft SQL Server veya Microsoft SQL Server veritabanı dosyası yalnızca bağlantıları geçerli değil.

Bu hatayı düzeltmek için SQL Server için .NET Framework veri sağlayıcısı kullanan veri bağlantıları yalnızca öğeleri ekleyin **O/R Tasarımcısı**.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Data.SqlClient>
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
