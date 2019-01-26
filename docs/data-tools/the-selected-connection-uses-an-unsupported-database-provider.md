---
title: Seçili bağlantı desteklenmeyen bir veritabanı sağlayıcısı kullanıyor
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 4d25dfa1-8fa4-4529-9b90-973bc2ec2993
author: gewarren
ms.author: gewarren
manager: jillfra
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: c59716342a26607842adca1e896177de2eb3facc
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55000191"
---
# <a name="the-selected-connection-uses-an-unsupported-database-provider"></a>Seçili bağlantı desteklenmeyen bir veritabanı sağlayıcısı kullanıyor

Bu ileti, SQL Server için .NET Framework veri sağlayıcısı kullanmayan öğelerini sürükleyip bırakırken görünür **Sunucu Gezgini** veya **veritabanı Gezgini** üzerine [görselde LINQ to SQL araçları Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md).

**O/R Tasarımcısı** SQL Server için .NET Framework sağlayıcısını kullanan veri bağlantılarını destekler. Microsoft SQL Server veya Microsoft SQL Server veritabanı dosyası yalnızca bağlantıları geçerli değil.

Bu hatayı düzeltmek için SQL Server için .NET Framework veri sağlayıcısı kullanan veri bağlantıları yalnızca öğeleri ekleyin **O/R Tasarımcısı**.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Data.SqlClient>
- [O/R Tasarımcısı iletileri](../data-tools/o-r-designer-messages.md)
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
