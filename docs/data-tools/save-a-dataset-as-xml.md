---
title: Bir veri kümesini XML olarak kaydetme
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- XML [Visual Basic], datasets
- data [Visual Studio], saving as XML
- datasets [Visual Basic], saving as XML
- saving data
ms.assetid: 68b8327c-ae05-49ff-b9ba-99183e70b52c
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: fbcacfbb44bb9f5ed4d34637a5aee5f9d014be46
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53894054"
---
# <a name="save-a-dataset-as-xml"></a>Bir veri kümesini XML olarak kaydetme

XML veri kümesindeki veri kümesinde kullanılabilir XML yöntemleri çağırarak erişin. XML biçiminde verileri kaydetmek için ya da çağırabileceğiniz <xref:System.Data.DataSet.GetXml%2A> yöntemi veya <xref:System.Data.DataSet.WriteXml%2A> yöntemi bir <xref:System.Data.DataSet>.

Çağırma <xref:System.Data.DataSet.GetXml%2A> yöntemi XML olarak biçimlendirilmiş veri kümesindeki tüm veri tablolardaki verileri içeren bir dize döndürür.

Çağırma <xref:System.Data.DataSet.WriteXml%2A> yöntemi, belirttiğiniz bir dosyaya XML biçimli verileri gönderir.

## <a name="to-save-the-data-in-a-dataset-as-xml-to-a-variable"></a>Verileri bir dataset içinde XML olarak bir değişkene kaydetmek için

- <xref:System.Data.DataSet.GetXml%2A> Yöntemi döndürür bir <xref:System.String>. Türünde bir değişken bildirmek <xref:System.String> ve sonuçları atama <xref:System.Data.DataSet.GetXml%2A> yöntemi.

     [!code-vb[VbRaddataSaving#12](../data-tools/codesnippet/VisualBasic/save-a-dataset-as-xml_1.vb)]
     [!code-csharp[VbRaddataSaving#12](../data-tools/codesnippet/CSharp/save-a-dataset-as-xml_1.cs)]

## <a name="to-save-the-data-in-a-dataset-as-xml-to-a-file"></a>Verileri bir dataset içinde XML olarak bir dosyaya kaydetmek için

- <xref:System.Data.DataSet.WriteXml%2A> Yöntemi olan çeşitli aşırı yükler. Bir değişken bildirmek ve bir dosyaya kaydetmek için geçerli bir yol atayın. Aşağıdaki kod, verileri bir dosyaya kaydetmek gösterilmektedir:

     [!code-vb[VbRaddataSaving#13](../data-tools/codesnippet/VisualBasic/save-a-dataset-as-xml_2.vb)]
     [!code-csharp[VbRaddataSaving#13](../data-tools/codesnippet/CSharp/save-a-dataset-as-xml_2.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- [Verileri yeniden veritabanına kaydetme](../data-tools/save-data-back-to-the-database.md)