---
title: Bir veri kümesini XML olarak kaydetme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
- aspx
helpviewer_keywords:
- XML [Visual Basic], datasets
- data [Visual Studio], saving as XML
- datasets [Visual Basic], saving as XML
- saving data
ms.assetid: 68b8327c-ae05-49ff-b9ba-99183e70b52c
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 2e4331b59c532e681c7e10ab8e43b953e9f72b18
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60059701"
---
# <a name="save-a-dataset-as-xml"></a>Bir veri kümesini XML olarak kaydetme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

XML veri kümesindeki veri kümesinde kullanılabilir XML yöntemleri çağırarak erişilebilir. XML biçiminde verileri kaydetmek için ya da çağırabileceğiniz <xref:System.Data.DataSet.GetXml%2A> yöntemi veya <xref:System.Data.DataSet.WriteXml%2A> yöntemi bir <xref:System.Data.DataSet>.  
  
 Çağırma <xref:System.Data.DataSet.GetXml%2A> yöntemi XML olarak biçimlendirilmiş veri kümesindeki tüm veri tablolardaki verileri içeren bir dize döndürür.  
  
 Çağırma <xref:System.Data.DataSet.WriteXml%2A> yöntemi, belirttiğiniz bir dosyaya XML biçimli verileri gönderir.  
  
### <a name="to-save-the-data-in-a-dataset-as-xml-to-a-variable"></a>Verileri bir dataset içinde XML olarak bir değişkene kaydetmek için  
  
- <xref:System.Data.DataSet.GetXml%2A> Yöntemi döndürür bir <xref:System.String>. Bu türde bir değişken bildirmek anlamına gelir <xref:System.String> ve sonuçları atama <xref:System.Data.DataSet.GetXml%2A> yöntemi.  
  
     [!code-csharp[VbRaddataSaving#12](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataSaving/CS/Class1.cs#12)]
     [!code-vb[VbRaddataSaving#12](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataSaving/VB/Class1.vb#12)]  
  
### <a name="to-save-the-data-in-a-dataset-as-xml-to-a-file"></a>Verileri bir dataset içinde XML olarak bir dosyaya kaydetmek için  
  
- <xref:System.Data.DataSet.WriteXml%2A> Yöntemi olan çeşitli aşırı yükler. Aşağıdaki kod, verileri bir dosyaya kaydetmek gösterilmektedir. Bir değişken bildirmek ve bir dosyaya kaydetmek için geçerli bir yol atayın.  
  
     [!code-csharp[VbRaddataSaving#13](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataSaving/CS/Class1.cs#13)]
     [!code-vb[VbRaddataSaving#13](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataSaving/VB/Class1.vb#13)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Verileri yeniden veritabanına kaydetme](../data-tools/save-data-back-to-the-database.md)
