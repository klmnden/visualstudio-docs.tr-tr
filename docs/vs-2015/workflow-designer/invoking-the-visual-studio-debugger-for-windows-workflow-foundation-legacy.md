---
title: Windows Workflow Foundation (eski) için hata ayıklayıcıyı çalıştırmak | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
helpviewer_keywords:
- stepping
- Step Over command
- stepping, commands
- debugging, using workflow debugger
- workflows, debugger
- workflow debugger, starting
- Step In command
- debugger, workflow
- Step Out command
- debugging workflows, starting the debugger
ms.assetid: d6f58e35-5cce-4ff2-9afc-b2d9d0f819cf
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 82532fc2864bcb4c19b0cf122e60fd9a64b2dbf9
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60113072"
---
# <a name="invoking-the-visual-studio-debugger-for-windows-workflow-foundation-legacy"></a>Windows Workflow Foundation için Visual Studio Hata Ayıklayıcısını Çağırma (Eski)
Bu konu açıklar nasıl [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] hata ayıklamak için hata ayıklayıcı [!INCLUDE[wf](../includes/wf-md.md)] eski uygulamalarda [!INCLUDE[wfd1](../includes/wfd1-md.md)]. Eski kullanın [!INCLUDE[wfd2](../includes/wfd2-md.md)] hedeflemek gerektiğinde [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] veya [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)].

 Genellikle, diğer Visual Studio programlama dillerinde yazılan programlar yalnızca hata ayıklama gibi eski iş akışı hata ayıklama. Başlatabilirsiniz [!INCLUDE[vs_current_long](../includes/vs-current-long-md.md)] hata ayıklayıcı için Windows Workflow Foundation aşağıdaki yollarla:

- Seçin **iliştirme** üzerinde **hata ayıklama** menüsünde kullanılabilir işlemleri çalışan bir iş akışı örneği seçin.

- Tuşuna **F5** iş akışı örneği çalıştırmaya başlayın ya da bir kesme noktasına isabet sonra çalışmaya devam eder.

## <a name="stepping-through-code"></a>Kod boyunca ilerleme
 Hata ayıklayıcı, kodu satır satır aynı anda yürütülmekte olan bir Adımlama, en yaygın hata ayıklama yordamları destekler. Kod içerisinde ilerlemeye yönelik üç komutlar şunlardır:

- **Adımı**: Bir etkinlik kullanarak adım **F11**. Hata ayıklama adımlarında içinde tanımlanan herhangi bir işleyici. Hiçbir tutucusu tanımlanmazsa, etkinliğin adım veya diğer etkinlikler içeren bileşik etkinliklerle ilk yürütme etkinliğini adım. Kod işleyicisi Adımlama Tasarımcısı'ndan aşağıdaki etkinlikler için desteklenmez: **IfElseActivity**, **WhileActivity**, **ConditionedActivityGroup**, veya **ReplicatorActivity**. Bu etkinlikler ile ilişkili işleyiciler hata ayıklamak için kod açık kesme noktaları yerleştirmeniz gerekir.

- **Dışına adımla**: Bir etkinlik kullanıldığında dışında adım **Shift-F11**. Bir etkinlik dışına Adımlama geçerli etkinliği ve tüm eşdüzey tamamlanana kadar etkinlikleri çalıştırır. Hata ayıklayıcı, ardından geçerli etkinliğin üst öğede keser. Bir kod işleyicisinden Adımlama, hata ayıklayıcı işleyici ilişkilendirildiği faaliyete keser.

- **Üzerinden adımla**: Bir etkinlik kullanıldığında üzerinden adım **F10**. Bileşik bir etkinlik Adımlama olduğunda. hata ayıklayıcı birleşik etkinlik ilk yürütülebilir alt keser. Gibi bir olmayan-bileşik Adımlama olduğunda bir **CodeActivity** etkinliği, hata ayıklayıcı, üzerinde bir sonraki etkinliğe etkinlik ve ilişkili işleyiciler ve sonları yürütür. Çalıştırılan etkinlik son alt etkinliğin bileşik bir etkinlik ise, yürütme sonrasında hata ayıklayıcı üst etkinlik keser.

## <a name="attaching-to-a-process"></a>Bir işleme ekleme
 Bir işleme ekleyerek bir iş akışı hata ayıklamak için kullanılabilir işlemden seçin **kullanılabilir işlemler** liste kutusunda **iliştirme** iletişim kutusu. Varsa **otomatik: İş akışı kodu** görüntülenmiyorsa **ekleme** metin kutusunu işaretleyip tıklayın **seçin**. İçinde **kod türünü seç** iletişim kutusu, tıklayın **bu tür kodlarda hata ayıklama** seçip **iş akışı**. Ardından **Tamam** tıklatıp **iliştirme**.

## <a name="debugging-with-f5"></a>F5 tuşuna basarak hata ayıklama
 Bir iş akışı etkinlik Kitaplığı kullanıldığında farklı Visual Studio projelerinde, bir iş akışı konak uygulama ve iş akışı DLL gibi bulunuyorsa, iş akışı DLL projesi iş akışının hata ayıklamak için Visual Studio çözüm başlangıç projesi olarak ayarlamanız gerekir kullanarak **F5**. Ana uygulama iş akışı DLL projenin yolu ayarlamalısınız **harici program Başlat** özelliği.

 Çözüm Gezgini'nde bir başlangıç projesi ayarlamak için proje adını sağ tıklatın ve seçin **başlangıç projesi olarak ayarla**. Ana yolunu ayarlamak için **harici program Başlat** özelliği, iş akışı projenin çift **özellikleri** düğümünü seçip Çözüm Gezgini **hata ayıklama** sekmesi. Altında **başlatma eylemi**seçin **harici program Başlat** ve ayıklamak istediğiniz iş akışı barındırma .exe dosyasının yolunu girin.

 Ana bilgisayar uygulaması başlangıç projesi olarak ayarlanırsa, yalnızca Visual Studio hata ayıklayıcı hata ayıklama için çağrılır; [!INCLUDE[vs_current_long](../includes/vs-current-long-md.md)] Windows Workflow Foundation için hata ayıklayıcı çağrılamaz. Visual Studio hata ayıklayıcısını kullandıysanız, yalnızca C# veya Visual Basic kod kesme noktaları isabet; İş Akışı Tasarımcısı'nda ayarlanan kesme noktaları isabet değil. Örneğin, ayarladığınız bir kesme noktası bir <xref:System.Workflow.Activities.ParallelActivity> etkinlik Tasarımcısı'nda, isabet [!INCLUDE[vs_current_long](../includes/vs-current-long-md.md)] Windows Workflow Foundation için hata ayıklayıcı kullanılır, ancak değil kullandığınızda, Visual Studio hata ayıklayıcısını.

## <a name="see-also"></a>Ayrıca Bkz.
 [Nasıl yapılır: (Eski) akışlarında kesme noktası ayarlama](../workflow-designer/how-to-set-breakpoints-in-workflows-legacy.md) [eski iş akışlarında hata ayıklama](../workflow-designer/debugging-legacy-workflows.md)