---
title: N katmanlı uygulamalarda veri kümeleriyle çalışma
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- datasets [Visual Basic], n-tier applications
- multi-tier database applications
- DataSet project [VS n-tier applications]
- distributed applications [VS n-tier applications]
- data [Visual Basic], n-tier applications
- TableAdapters, n-tier applications
- n-tier applications
- tiers, n-tier applications
- typed datasets, n-tier applications
- multiple tier applications
ms.assetid: f6ae2ee0-ea5f-4a79-8f4b-e21c115afb20
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: d89c3a5582ef1c84c455801d3766d65246e34dea
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53899645"
---
# <a name="work-with-datasets-in-n-tier-applications"></a>N katmanlı uygulamalarda veri kümeleriyle çalışma

*N katmanlı veri uygulamalarını* birden çok mantıksal katmana ayrılmış veri merkezli uygulamalar (veya *katmanları*). Diğer bir deyişle, bir n katmanlı veri uygulaması birden çok proje, veri erişim katmanında, iş mantığı katmanı ve sunu katmanı her kendi projesi içinde ayrılmış bir uygulamadır. Daha fazla bilgi için [N katmanlı veri uygulamalarına genel bakış](../data-tools/n-tier-data-applications-overview.md).

Türü belirtilmiş datasets ayrı projelere Tableadapter'lar ve veri kümesi sınıfları oluşturulabilir olacak şekilde geliştirilmiştir. Bu hızlı bir şekilde uygulama katmanları ayırmak ve n katmanlı veri uygulamaları oluşturma olanağı sağlar.

N katmanlı destek türü belirtilmiş veri kümelerinde, n katmanlı bir tasarım uygulaması mimarisi yinelemeli geliştirilmesini sağlar. Ayrıca el ile kod birden fazla projeye ayrı gereksinimini ortadan kaldırır. Veri katmanı kullanarak dışarı tasarlamaya başlayabilir **veri kümesi Tasarımcısı**. Uygulama mimarisi, n katmanlı bir tasarım almaya hazır olduğunuzda, ayarlama **DataSet projesi** ayrı bir projeye veri kümesi sınıfı oluşturmak için bir veri kümesi özelliği.

## <a name="reference"></a>Başvuru

- <xref:System.Data.DataSet>
- <xref:System.Data.TypedTableBase%601>

## <a name="see-also"></a>Ayrıca bkz.

- [N katmanlı veri uygulamalarına genel bakış](../data-tools/n-tier-data-applications-overview.md)
- [İzlenecek yol: N katmanlı veri uygulaması oluşturma](../data-tools/walkthrough-creating-an-n-tier-data-application.md)
- [N katmanlı uygulamalarda TableAdapter’lara kod ekleme](../data-tools/add-code-to-tableadapters-in-n-tier-applications.md)
- [N katmanlı uygulamalarda veri kümelerine kod ekleme](../data-tools/add-code-to-datasets-in-n-tier-applications.md)
- [N Katmanlı bir veri kümesine doğrulama ekleme](../data-tools/add-validation-to-an-n-tier-dataset.md)
- [Veri kümeleri ile TableAdapter’ları farklı projelere ayırma](../data-tools/separate-datasets-and-tableadapters-into-different-projects.md)
- [Hiyerarşik güncelleştirme](../data-tools/hierarchical-update.md)
- [Visual Studio'daki veri kümesi araçları](../data-tools/dataset-tools-in-visual-studio.md)
- [Visual Studio'da verilere erişime](../data-tools/accessing-data-in-visual-studio.md)
- [TableAdapter’lar oluşturma ve yapılandırma](../data-tools/create-and-configure-tableadapters.md)
- [N katmanı ve uzak uygulamalarla LINQ-SQL](/dotnet/framework/data/adonet/sql/linq/n-tier-and-remote-applications-with-linq-to-sql)