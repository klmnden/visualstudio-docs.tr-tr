---
title: Bir Windows Forms uygulamasındaki verileri filtreleme ve sıralama | Microsoft Docs
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
- row states, filtering
- data views, sorting
- row version, filtering
- row states
- data views, filtering
- sorting datasets, using data views
- dataset filtering, using data views
ms.assetid: f4f100f1-776d-46dc-b2fd-5b35b98d9561
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 5592a488788c61af7ad6875de239fca62746857c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54754907"
---
# <a name="filter-and-sort-data-in-a-windows-forms-application"></a>Bir Windows Forms uygulamasındaki verileri filtreleme ve sıralama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Ayarlayarak verileri filtreleme <xref:System.Windows.Forms.BindingSource.Filter%2A> özelliğini istenen kayıtlar döndüren bir dize ifadesi.  
  
 Ayarlayarak verileri sıralamak <xref:System.Windows.Forms.BindingSource.Sort%2A> özelliğini sütun adı, sıralama yapmak istediğiniz; ekleme `DESC` azalan düzende sıralamak veya ekleme için `ASC` artan düzende sıralamak için.  
  
> [!NOTE]
>  Uygulamanızı kullanmıyorsa <xref:System.Windows.Forms.BindingSource> bileşenleri filtreleyebilirsiniz ve kullanarak verileri sıralama <xref:System.Data.DataView> nesneleri. Daha fazla bilgi için [DataViews](http://msdn.microsoft.com/library/0fe5dfa2-c1cd-435f-90b6-b4dd2e3ef34b).  
  
## <a name="to-filter-data-by-using-a-bindingsource-component"></a>BindingSource bileşenini kullanarak verilere filtre uygulamak için  
  
-   Ayarlama <xref:System.Windows.Forms.BindingSource.Filter%2A> özelliğini döndürmek istediğiniz ifade. Örneğin, aşağıdaki kod ile müşteriler döndürür bir `CompanyName` "B" ile başlar:  
  
     [!code-csharp[VbRaddataDisplaying#6](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataDisplaying/CS/Form1.cs#6)]
     [!code-vb[VbRaddataDisplaying#6](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataDisplaying/VB/Form1.vb#6)]  
  
## <a name="to-sort-data-by-using-a-bindingsource-component"></a>BindingSource bileşenini kullanarak verileri sıralama  
  
-   Ayarlama <xref:System.Windows.Forms.BindingSource.Sort%2A> özelliğini sıralamak istediğiniz sütunu. Örneğin, aşağıdaki kod üzerinde müşterileri sıralar `CompanyName` azalan düzende sütun:  
  
     [!code-csharp[VbRaddataDisplaying#7](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataDisplaying/CS/Form1.cs#7)]
     [!code-vb[VbRaddataDisplaying#7](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataDisplaying/VB/Form1.vb#7)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio'da verilere denetimler bağlama](../data-tools/bind-controls-to-data-in-visual-studio.md)
