---
title: İş Akışı Tasarımcısı ile İş Akışlarında Hata Ayıklama
ms.date: 11/04/2016
ms.topic: conceptual
ms.prod: visual-studio-dev15
helpviewer_keywords:
- Visual Studio Workflow Designer [WFD], debugging workflows
- Workflow Designer [WFD], debugging workflows
ms.assetid: d71308cf-d464-4536-8711-0d0a8eadb255
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 64574156bb1645a3d1f4e84f50a8e322751fd370
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53923437"
---
# <a name="debug-workflows-with-the-workflow-designer"></a>İş Akışı Tasarımcısı ile iş akışlarını hata ayıklama

**İş akışı Tasarımcısı** iş akışları ve özel etkinlikler hata ayıklama olanağı sağlar. İşlem ve davranışı, varsayılan Visual Studio hata ayıklayıcısı benzerdir.

## <a name="invoke-the-workflow-debugger"></a>İş akışı hata ayıklayıcısını çağırma

Genellikle, diğer Visual Studio programlama dillerinde yazılan programlar yalnızca hata ayıklama gibi iş akışı hata ayıklama. İş akışı hata ayıklayıcısını aşağıdaki şekillerde başlayabilirsiniz:

- Seçin **iliştirme** üzerinde **hata ayıklama** menüsünde, iş akışı örneği için çalışan ana bilgisayar işlemi seçin. Bu yordam, yönetilen kod içinde bir ana bilgisayar işlemi ekleme olarak aynıdır.

- Tuşuna **F5** iş akışı örneği çalıştırmaya başlayın ya da bir kesme noktasına isabet sonra çalışmaya devam eder.

- Uzaktan hata ayıklamayı kullanın. Uzaktan hata ayıklama hakkında daha fazla bilgi için bkz. [nasıl yapılır: Uzaktan hata ayıklamayı etkinleştirme](/previous-versions/visualstudio/visual-studio-2010/febz73k0(v=vs.100)).

   > [!NOTE]
   > İş akışı uygulaması x86 hedefliyorsa mimarisi ve uzaktan hata ayıklama uzak makinede Visual Studio yüklü veya uygulama iş akışı hedefi için değiştirildiğindesüreceçalışmazsonrabir64bitişletimsistemiçalıştıranbirmakinedebarındırılıyor **Herhangi bir CPU**.

## <a name="step-through-code"></a>Kodunuz içinde adım adım

- **Adımı**: Bir etkinlik adımla tuşuna basarak **F11**. Hata ayıklama adımlarında içinde tanımlanan herhangi bir işleyici. Hiçbir tutucusu tanımlanmazsa, etkinliğin adım veya diğer etkinlikler içeren bileşik etkinliklerle ilk yürütme etkinliğini adım.

- **Dışına adımla:** Adım dışında bir etkinlik tuşlarına basarak **Shift**+**F11**. Bir etkinlik dışına Adımlama geçerli etkinliği ve tüm eşdüzey tamamlanana kadar etkinlikleri çalıştırır. Hata ayıklayıcı, ardından geçerli etkinliğin üst öğede keser. Bir kod işleyicisinden Adımlama, hata ayıklayıcı işleyici ilişkilendirildiği faaliyete keser.

- **Üzerinden adımla**: Bir etkinlik Adımlama tuşuna basarak **F10**. Bileşik bir etkinlik Adımlama olduğunda hata ayıklayıcı birleşik etkinlik ilk yürütülebilir alt keser. Gibi bir olmayan-bileşik Adımlama olduğunda bir <xref:System.Activities.Statements.Assign> etkinliği, hata ayıklayıcı, üzerinde bir sonraki etkinliğe etkinlik ve ilişkili işleyiciler ve sonları yürütür. Ardından, çalıştırılan etkinlik son alt etkinliğin bileşik bir etkinlik ise, yürütme sonrasında hata ayıklayıcı üst etkinlik keser.

## <a name="debug-with-f5"></a>F5 tuşuna basarak hata ayıklama

Bir iş akışı konsol uygulaması oluşturuyorsanız, tuşuna basmanız yeterlidir **F5** uygulama ve iş akışı hata ayıklamayı başlatmak için. Etkinlik kitaplığı, kendi oluşturuyorsanız, yürütülebilir bir Windows uygulaması başlangıç projesi olarak belirtmeniz gerekir. Başlangıç projesi ayarlama **Çözüm Gezgini**, ana proje adını sağ tıklatın ve seçin **başlangıç projesi olarak ayarla**.