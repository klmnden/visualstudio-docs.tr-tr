---
title: Workflow Foundation proje oluşturma
ms.date: 06/25/2018
ms.topic: conceptual
helpviewer_keywords:
- Workflow Designer, creating a workflow project
- creating a workflow project
ms.assetid: 235a125e-ebe7-4a98-bf77-86c8558728fb
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 15c02312d5c257f13b9c0394790bc8a2611d7972
ms.sourcegitcommit: 489aca71046fb6e4aafd0a4509cd7dc149d707b1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/25/2019
ms.locfileid: "58414764"
---
# <a name="workflow-project-templates"></a>İş akışı projesi şablonları

Visual Studio Proje şablonları kullanarak iş akışları, Windows Communication Foundation (WCF) iş akışı Hizmetleri, özel etkinlikler ve özel etkinlik tasarımcıları oluşturabilirsiniz. Bu makalede, kitaplıkları ve uygulamaları ile Visual Studio Proje şablonları oluşturma işlemini açıklar.

## <a name="create-a-workflow-project"></a>İş Akışı projesi Oluşturma

Visual Studio, dört farklı iş akışı proje şablonlarını sunar:

- İş akışı konsol uygulaması

- WCF iş akışı hizmeti uygulaması

- Etkinlik kitaplığı

- Etkinlik Tasarımcısı kitaplığı

Bu şablonlar erişmek için ilk yükleme **Windows Workflow Foundation** Visual Studio bileşen. Ayrıntılı yönergeler için bkz. [Windows Workflow Foundation'ı yükleme](developing-applications-with-the-workflow-designer.md#install-windows-workflow-foundation).

1. Yükledikten sonra **Windows Workflow Foundation** bileşeni, select **dosya** > **yeni** > **proje**.

1. Arayın ve örnek bir iş akışı projesi şablonu seçin, **iş akışı konsol uygulaması** şablonu.

1. Aracılığıyla proje oluşturmaya devam edin.

   > [!NOTE]
   > Varolan çözüme yeni bir proje eklemek istiyorsanız, bu çözüm, Visual Studio'da açın, çözüme sağ **Çözüm Gezgini**seçip **Ekle** > **yeni Proje**.

## <a name="workflow-console-app"></a>İş akışı konsol uygulaması

Seçerseniz **iş akışı konsol uygulaması** şablon, Visual Studio, XAML içinde bir iş akışı tanımı oluşturur. İş Akışı Tasarımcısı açılır ve oluşturduğunuz iş akışı için tuvalde görüntüler. Bir iş akışı oluşturmak için etkinlikler veya diğer iş akışı öğeleri sürükleyin **araç kutusu** tasarım yüzeyine bırakın.

## <a name="wcf-workflow-service-app"></a>WCF iş akışı hizmeti uygulaması

Seçerseniz **WCF iş akışı hizmeti uygulaması** şablon, Visual Studio, bir hizmet tanımı XAML olarak oluşturur. İş Akışı Tasarımcısı ile Tasarım görünümü açılır bir <xref:System.Activities.Statements.Sequence> içeren bir dizi etkinlik <xref:System.ServiceModel.Activities.Receive> ve <xref:System.ServiceModel.Activities.SendReply> etkinlikler.

## <a name="activity-library"></a>Etkinlik kitaplığı

Seçerseniz **etkinlik Kitaplığı** şablon, Visual Studio, XAML içinde bir etkinlik tanımı oluşturur. İş Akışı Tasarımcısı açılır ve özel etkinliğinizin tuval görüntüler. Etkinliği sürükleyin **araç kutusu** özel etkinliklerinizi içerecek şekilde tasarım yüzeyine bırakın.

> [!NOTE]
> Yalnızca bir alt etkinlik özel etkinliğinizin gövdesinde izin verilir. Ancak, bu alt etkinlik bileşik bir etkinlik gibi olabilir bir <xref:System.Activities.Statements.Sequence> etkinlik veya <xref:System.Activities.Statements.Flowchart> etkinlik.

## <a name="activity-designer-library"></a>Etkinlik Tasarımcısı kitaplığı

Seçerseniz **etkinlik Tasarımcısı Kitaplığı** şablon, Visual Studio, XAML ve arka plan kod uygulama dosyasında bir etkinlik tasarımcısının tanımı oluşturur. İş Akışı Tasarımcısı açılır ve tuval, etkinlik Tasarımcısı için görüntüler. Sürükle Windows Presentation Foundation (WPF) denetimleri gelen **araç kutusu** özel etkinlik Tasarımcısı'nda kullanılacak tasarım yüzeyine bırakın.

Özel Etkinlik Tasarımcısı uygulamak nasıl bir örnek için bkz [nasıl yapılır: Özel Etkinlik Tasarımcısı oluşturma](/dotnet/framework/windows-workflow-foundation/how-to-create-a-custom-activity-designer).

> [!NOTE]
> Özel Etkinlik tasarımcıları, varsayılan .NET Framework etkinlikler ve özel etkinlikler için kullanılabilir.

## <a name="see-also"></a>Ayrıca bkz.

- [İş akışı Tasarımcısını kullanma](developing-applications-with-the-workflow-designer.md)
- [(.NET Framework) iş akışları tasarlama](/dotnet/framework/windows-workflow-foundation/designing-workflows)