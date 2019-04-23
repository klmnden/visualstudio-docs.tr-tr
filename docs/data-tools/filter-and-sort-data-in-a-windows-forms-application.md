---
title: Bir Windows Forms uygulamasındaki verileri filtreleme ve sıralama
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- row states, filtering
- data views, sorting
- row version, filtering
- row states
- data views, filtering
- sorting datasets, using data views
- dataset filtering, using data views
ms.assetid: f4f100f1-776d-46dc-b2fd-5b35b98d9561
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 17416a3b64d6cbb5f01192440a9df735f0b9fb94
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60090335"
---
# <a name="filter-and-sort-data-in-a-windows-forms-application"></a>Bir Windows Forms uygulamasındaki verileri filtreleme ve sıralama

Ayarlayarak verileri filtreleme <xref:System.Windows.Forms.BindingSource.Filter%2A> özelliğini istenen kayıtlar döndüren bir dize ifadesi.

Ayarlayarak verileri sıralamak <xref:System.Windows.Forms.BindingSource.Sort%2A> özelliğini sütun adına göre sıralamak isteyebilirsiniz; ekleme `DESC` azalan düzende sıralamak veya ekleme için `ASC` artan düzende sıralamak için.

> [!NOTE]
> Uygulamanızı kullanmıyorsa <xref:System.Windows.Forms.BindingSource> bileşenleri filtreleyebilirsiniz ve kullanarak verileri sıralama <xref:System.Data.DataView> nesneleri. Daha fazla bilgi için [DataViews](/dotnet/framework/data/adonet/dataset-datatable-dataview/dataviews).

## <a name="to-filter-data-by-using-a-bindingsource-component"></a>BindingSource bileşenini kullanarak verilere filtre uygulamak için

- Ayarlama <xref:System.Windows.Forms.BindingSource.Filter%2A> özelliğini döndürmek istediğiniz ifade. Örneğin, aşağıdaki kod ile müşteriler döndürür bir `CompanyName` "B" ile başlar:

     [!code-csharp[VbRaddataDisplaying#6](../data-tools/codesnippet/CSharp/filter-and-sort-data-in-a-windows-forms-application_1.cs)]
     [!code-vb[VbRaddataDisplaying#6](../data-tools/codesnippet/VisualBasic/filter-and-sort-data-in-a-windows-forms-application_1.vb)]

## <a name="to-sort-data-by-using-a-bindingsource-component"></a>BindingSource bileşenini kullanarak verileri sıralama

- Ayarlama <xref:System.Windows.Forms.BindingSource.Sort%2A> özelliğini sıralamak istediğiniz sütunu. Örneğin, aşağıdaki kod üzerinde müşterileri sıralar `CompanyName` azalan düzende sütun:

     [!code-csharp[VbRaddataDisplaying#7](../data-tools/codesnippet/CSharp/filter-and-sort-data-in-a-windows-forms-application_2.cs)]
     [!code-vb[VbRaddataDisplaying#7](../data-tools/codesnippet/VisualBasic/filter-and-sort-data-in-a-windows-forms-application_2.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da verilere denetimler bağlama](../data-tools/bind-controls-to-data-in-visual-studio.md)