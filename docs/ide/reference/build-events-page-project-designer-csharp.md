---
title: Derleme Olayları Sayfası, Proje Tasarımcısı (C#)
ms.date: 11/04/2016
ms.technology: vs-ide-compile
ms.topic: reference
f1_keywords:
- cs.ProjectPropertiesBuildEvents
helpviewer_keywords:
- build events
- Project Designer, Build Events page
- pre-build events
- post-build events
ms.assetid: 3fff9ae5-213c-46ea-a660-1d70acb6c922
author: ghogen
ms.author: ghogen
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: ba429c116d44a5d79d935fe3a1ad07b6d5f36f79
ms.sourcegitcommit: 85d66dc9fea3fa49018263064876b15aeb6f9584
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/24/2019
ms.locfileid: "68461846"
---
# <a name="build-events-page-project-designer-c"></a>Derleme Olayları Sayfası, Proje Tasarımcısı (C#)

Yapı yapılandırma yönergelerini belirtmek için **Proje Tasarımcısı** ' nın **Olayları oluştur** sayfasını kullanın. Ayrıca, herhangi bir oluşturma sonrası olayının çalıştırıldığı koşulları belirtebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Derleme olaylarını (C#)](../../ide/how-to-specify-build-events-csharp.md)ve [nasıl yapılacağını belirtin: Derleme olaylarını belirtin (Visual Basic)](../../ide/how-to-specify-build-events-visual-basic.md).

## <a name="uielement-list"></a>UIElement Listesi

**Yapılandırma**

Bu denetim bu sayfada düzenlenebilir değildir. Bu denetimin açıklaması için bkz. [derleme sayfası, proje Tasarımcısı (C#)](../../ide/reference/build-page-project-designer-csharp.md).

**Platformunun**

Bu denetim bu sayfada düzenlenemez. Bu denetimin açıklaması için bkz. [derleme sayfası, proje Tasarımcısı (C#)](../../ide/reference/build-page-project-designer-csharp.md).

**Oluşturma öncesi olay komut satırı**

Yapı başlamadan önce yürütülecek komutları belirtir. Uzun komutları yazmak için, oluşturma öncesi [olay/oluşturma sonrası olay komut satırı Iletişim kutusunu](../../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md)göstermek Için **derleme ön yapısını Düzenle** ' ye tıklayın.

> [!NOTE]
> Proje güncel değilse ve derleme tetikleniyorsa, ön derleme olayları çalışmaz.

**Oluşturma sonrası olay komut satırı**

Yapı bittikten sonra yürütülecek komutları belirtir. Uzun komutları yazmak için derleme sonrası **olay/oluşturma sonrası olay komut satırı Iletişim kutusunu**göstermek üzere **derlemeyi Düzenle** ' ye tıklayın.

> [!NOTE]
> . Bat `call` dosyalarını çalıştıran tüm derleme sonrası komutlarının önüne bir ifade ekleyin. Örneğin, `call C:\MyFile.bat` veya `call C:\MyFile.bat call C:\MyFile2.bat`.

**Oluşturma sonrası olayını Çalıştır**

Aşağıdaki tabloda gösterildiği gibi, oluşturma sonrası olayının çalışması için aşağıdaki koşulları belirtir.

|Seçenek|Sonuç|
|------------|------------|
|**Her zaman**|Oluşturma sonrası olay, yapılandırmanın başarılı olup olmamasına bakılmaksızın çalışacaktır.|
|**Başarılı derleme üzerinde**|Oluşturma sonrası olay, derleme başarılı olursa çalışır. Bu nedenle, derleme başarılı olduğu sürece olay, güncel olan bir proje için de çalışır.|
|**Derleme proje çıkışını güncelleştirdiğinde**|Oluşturma sonrası olay, yalnızca derleyicinin çıkış dosyası (. exe veya. dll) önceki derleyici çıkış dosyasından farklı olduğunda çalışır. Bu nedenle, bir proje güncel ise, derleme sonrası bir olay çalıştırılmaz.|

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Derleme Olayları Belirtme (Visual Basic)](../../ide/how-to-specify-build-events-visual-basic.md)
- [Nasıl yapılır: Derleme Olayları Belirtme (C#)](../../ide/how-to-specify-build-events-csharp.md)
- [Proje Özellikleri Başvurusu](../../ide/reference/project-properties-reference.md)
- [Derleme ve Oluşturma](../../ide/compiling-and-building-in-visual-studio.md)