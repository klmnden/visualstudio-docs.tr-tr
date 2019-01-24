---
title: 'Nasıl yapılır: WCF iş akışı hizmeti uygulaması oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
ms.assetid: 12d675ac-27d8-4d86-ba16-6f7688f8c841
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 0e7bf54f527a82bb59a8dc9248d3d9294a07aa59
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54756788"
---
# <a name="how-to-create-a-wcf-workflow-service-application"></a>Nasıl yapılır: WCF İş Akışı Hizmeti Uygulaması Oluşturma
[!INCLUDE[indigo1](../includes/indigo1-md.md)] İş akışı hizmeti uygulamaları iletileri istemcileri ile kendisi arasında işlem sınırları arasında geçen dağıtılmış iletişimleri hizmetleridir. Hizmet tarafında hizmet sözleşmesinin uygulamasını bildirimli olarak iş akışı etkinliklerinde aracılığıyla gerçekleştirilir [!INCLUDE[netfx40_short](../includes/netfx40-short-md.md)] .NET Framework 3.5 eski iş akışı hizmetlerine benzer şekilde.  
  
### <a name="to-create-a-wcf-workflow-service-application"></a>WCF iş akışı hizmeti uygulaması oluşturmak için  
  
1.  Başlangıç [!INCLUDE[vs2010](../includes/vs2010-md.md)].  
  
2.  Üzerinde **dosya** menüsünde **yeni**ve ardından **proje...** .  
  
     **Yeni proje** iletişim kutusu açılır.  
  
3.  İçinde **yüklü şablonlar** bölmesinde **WCF** veya **iş akışı** da **Visual C#** veya **VisualBasic** gruplandırmaları tercih ettiğiniz dilde bağlı olarak.  
  
4.  Orta bölmede seçin **WCF iş akışı hizmeti uygulaması**.  
  
5.  İçinde **adı** kutusunda, tanımlamakta kolaylaştırmak, projeniz için açıklayıcı bir ad girin.  
  
6.  İçinde **konumu** kutusunda, projeyi kaydedin veya istediğiniz dizin girin **Gözat** gitmek için.  
  
7.  İçinde **çözüm** kutusunda, yeni bir çözüm oluşturup ardından seçin **Tamam**.  
  
    > [!NOTE]
    >  Varolan bir çözüm için bir iş akışı konsol uygulaması eklemek istiyorsanız, bu çözümde açık [!INCLUDE[vs2010](../includes/vs2010-md.md)], çözüme sağ tıklayın **Çözüm Gezgini**seçip **Ekle**, ardından  **Yeni proje...** açmak için **yeni proje** iletişim kutusu. Bu yordamda yukarıda açıklanan şekilde devam edin.  
  
8.  Proje şablonunu bir hizmet tanımı XAML olarak oluşturur. [!INCLUDE[wfd1](../includes/wfd1-md.md)] Tasarım görünümü ile açılır bir <xref:System.Activities.Statements.Sequence> içeren bir dizi etkinlik <xref:System.ServiceModel.Activities.Receive> ve <xref:System.ServiceModel.Activities.SendReply> etkinlikler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Bir etkinlik oluşturma](http://msdn.microsoft.com/library/c09b1e99-21b5-4d96-9c04-ec31db3f4436)   
 [İş Akışı Projesi Oluşturma](../workflow-designer/creating-a-workflow-project.md)