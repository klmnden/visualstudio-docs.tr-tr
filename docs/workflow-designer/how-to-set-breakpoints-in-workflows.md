---
title: 'İş Akışı Tasarımcısı - nasıl yapılır: İş Akışlarında Kesme Noktası Ayarlama'
ms.date: 11/04/2016
ms.topic: conceptual
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
ms.assetid: e41b21c9-c061-4358-8e2f-eb5e412864a8
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 96db38e8a69d0b8b9ee042420647851aa1fbf0c0
ms.sourcegitcommit: 935e341a02dba1c2aa3b6e89469388aa6e626f7f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53684255"
---
# <a name="how-to-set-breakpoints-in-workflows"></a>Nasıl Yapılır: İş Akışlarında Kesme Noktası Ayarlama

İş Akışı Tasarımcısı kullandığınızda, grafik akışlarınızı Visual Basic'te yaptığınız şekilde kesme noktalarını ayarlayabilir veya C# kod. Beklendiği gibi iş akışı yürütme ayarladığınız her bir kesme noktasında durur.

Bir kesme noktası üç durumu vardır: *Bekleyen*, *bağlı*, ve *hata*. Bir kesme noktası ayarlarsanız, bekleyen ve düz kırmızı bir simge ile temsil edilir. Çalışma zamanı iş akışı türü yüklendiğinde bağlı olur. Geçerli olmayan bir etkinliği adı gibi kesme noktası için yanlış biçim belirtirseniz bir hata penceresinde görünür. Kesme noktası hala kesme noktası penceresine eklenir, ancak küçük "x" ile işaretlenir.

> [!NOTE]
> Çağrılan iş akışlarında kesme noktaları ayarlama desteklenmiyor.

> [!NOTE]
> Seçeneğini belirlediğinizden emin olun **yalnızca benim kodumu etkinleştir (sadece yönetilen)** gelen **Araçları** > **seçenekleri** > **hata ayıklama**  hata ayıklama önce menüsü. İlk iç dizisi üzerinde bir kesme noktası ayarlama seçeneği seçili değilse ve başka bir dizi içinde iç içe iki sıranın sahip tuşuna basarak **F11** ikinci iç sıra hata ayıklama değil.

> [!NOTE]
> XAML dosya özelliği tam yolu doğru değilse, bir iş akışında kesme noktaları ulaşılmıyor. Proje veya çözümü başka bir klasöre veya başka bir makineye taşıdıktan sonra özelliği XAML dosyasının tam yolu doğru değil. Seçin **Ctrl**+**S** kaydedin ve tam yolunu özelliğini güncelleştirin.

## <a name="to-set-a-breakpoint-on-an-activity-in-the-design-view"></a>Tasarım görünümünde bir etkinlikte bir kesme noktası ayarlamak için

1. Hata ayıklayıcı kesmek istediğiniz etkinliği seçin.

2. Üzerinde **hata ayıklama** menüsünde **iki durumlu kesme noktası**. Etkinlik sol üst kenarına kırmızı bir simge görünür.

   Alternatif olarak, basabilirsiniz **F9** etkinlik veya seçme etkinliğe sağ tıklayın ve da seçin sonra **kesme noktası** > **kesme noktası Ekle** bağlam menüsünden.

## <a name="see-also"></a>Ayrıca bkz.

- [İş Akışı Tasarımcısı ile İş Akışlarında Hata Ayıklama](../workflow-designer/debugging-workflows-with-the-workflow-designer.md)
- [Nasıl yapılır: İş Akışı Tasarımcısı ile XAML hatalarını ayıklama](../workflow-designer/how-to-debug-xaml-with-the-workflow-designer.md)