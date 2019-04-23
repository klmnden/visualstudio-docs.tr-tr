---
title: Eski iş akışlarında hata ayıklama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
helpviewer_keywords:
- workflows, debugging
- debugging, workflows
- debugging workflows
ms.assetid: e6097b47-760a-4b30-a92c-ae70cdbda49f
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: b98c520dc96b6f3c6467bbcaf8e48d9cff8791d2
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60048742"
---
# <a name="debugging-legacy-workflows"></a>Eski İş Akışlarında Hata Ayıklama
Eski kullanıyorsanız [!INCLUDE[wfd1](../includes/wfd1-md.md)] içinde [!INCLUDE[vs_current_long](../includes/vs-current-long-md.md)] oluşturmak için [!INCLUDE[wf](../includes/wf-md.md)] target.NET Framework 3.0 veya 3.5, başka bir programı gibi iş akışlarınızı kesme noktaları ayarlama işlemlere ekleme ve iş parçacığı İnceleme ayıklanabilmesi, uygulamaları ve çağrı yığını. Uzaktan hata ayıklama seçeneğiniz de vardır.  
  
> [!NOTE]
>  Visual Studio'nun birden çok sürümünü yüklediyseniz ve makinenizde kaldırılması WF3 hata ayıklama iki aşağıdaki olasılıkları biriyle başarısız olabilir:  
> 
> - Kesme noktalarınız ulaşılmıyor.  
>   - Aşağıdaki ileti görüntülenir:  
> 
>   **Web sunucusunda hata ayıklama başlatılamadı. Hata ayıklayıcı düzgün yüklenmemiş.  İstenen türde kod hata ayıklaması yapılamıyor.  Yüklemek veya hata ayıklayıcı onarmak için Kurulumu çalıştırın.**  
> 
>   .NET Framework 3.0 veya 3.5 iş akışı hata ayıklama sırasında ya da bu senaryo ortaya çıkarsa sürümünü Visual Studio yüklemesi onarıp gerçekleştirin.  
  
 [!INCLUDE[wf2](../includes/wf2-md.md)] Aşağıdaki standart ile tümleştirilir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] windows hata ayıklama:  
  
- **Kesme noktası**: Beklendiği gibi çalışır, ancak bir etkinlik için işlev adı belirtin.  
  
- **Çağrı yığını**: Bir iş akışı örneğinde yürüttünüz etkinliklerinin bir özetini sağlamak üzere değiştirildi. Girdileri **çağrı yığını** etkinlikleri yürütmenin bir Derinlik ilk arama penceresi açılır. Seçili etkinlik odak moduna giriş dosyasına çift tıklayabilirsiniz.  
  
- **İş parçacığı**: Hatası ayıklanmakta olan iş akışı örneğinin örnek kimliği sağlar.  
  
  Visual Studio için Windows Workflow Foundation, aşağıdaki hata ayıklama özellikleri desteklemez:  
  
- Koşullu kesme noktalarını Tasarımcı yüzeyinde.  
  
- QuickWatch.  
  
- Sonraki deyimi ayarlayın.  
  
- İmlece kadar Çalıştır.  
  
- Düzenle ve devam et.  
  
- Just-ın-time hata ayıklama.  
  
- Karışık mod hata ayıklama.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Windows Workflow Foundation için Visual Studio Hata Ayıklayıcısını Çağırma (Eski)](../workflow-designer/invoking-the-visual-studio-debugger-for-windows-workflow-foundation-legacy.md)  
  
 [Windows Workflow Foundation için Visual Studio Hata Ayıklayıcısını Devre Dışı Bırakma (Eski)](../workflow-designer/disabling-the-visual-studio-debugger-for-windows-workflow-foundation-legacy.md)  
  
 [Nasıl yapılır: ASP.NET Tabanlı İş Akışlarında Hata Ayıklama (Eski)](../workflow-designer/how-to-debug-aspnet-based-workflows-legacy.md)  
  
 [Nasıl yapılır: İş Akışlarında Kesme Noktası Ayarlama (Eski)](../workflow-designer/how-to-set-breakpoints-in-workflows-legacy.md)  
  
 [Uzak Bir Bilgisayardan İş Akışlarında Hata Ayıklama (Eski)](../workflow-designer/debugging-workflows-from-a-remote-computer-legacy.md)  
  
 [Hata Ayıklama Adımlama Seçenekleri (Eski)](../workflow-designer/debug-stepping-options-legacy.md)  
  
 [Nasıl yapılır: Hata Ayıklama Adımlama Seçeneğini Değiştirme (Eski)](../workflow-designer/how-to-change-the-debug-stepping-option-legacy.md)