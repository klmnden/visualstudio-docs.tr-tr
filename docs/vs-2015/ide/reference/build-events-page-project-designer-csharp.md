---
title: Derleme olayları sayfası, Proje Tasarımcısı (C#) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- cs.ProjectPropertiesBuildEvents
helpviewer_keywords:
- build events
- Project Designer, Build Events page
- pre-build events
- post-build events
ms.assetid: 3fff9ae5-213c-46ea-a660-1d70acb6c922
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: dc8fee5a01043a32061bfa711b7ad2009121b216
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63433732"
---
# <a name="build-events-page-project-designer-c"></a>Derleme Olayları Sayfası, Proje Tasarımcısı (C#)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Kullanım **Build Events** sayfasının **Proje Tasarımcısı** yapı yapılandırma yönergeleri belirtmek için. Altında herhangi bir derleme sonrası olayı çalıştığı koşulları belirtebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Derleme olayları belirtme (C#)](../../ide/how-to-specify-build-events-csharp.md)ve [nasıl yapılır: Derleme olayları belirtme (Visual Basic)](../../ide/how-to-specify-build-events-visual-basic.md).  
  
## <a name="uielement-list"></a>UIElement Listesi  
 **Yapılandırma**  
 Bu sayfa, bu denetim düzenlenemez. Bu denetimin açıklaması için bkz [derleme sayfası, Proje Tasarımcısı (C#)](../../ide/reference/build-page-project-designer-csharp.md).  
  
 **Platform**  
 Bu sayfada bu denetim düzenlenemez. Bu denetimin açıklaması için bkz [derleme sayfası, Proje Tasarımcısı (C#)](../../ide/reference/build-page-project-designer-csharp.md).  
  
 **Derleme öncesi olay komut satırı**  
 Oluşturma başlamadan önce yürütülecek herhangi bir komut belirtir. Uzun komutları yazmak için tıklatın **Düzenle derleme öncesi** görüntülenecek [derleme öncesi olay/derleme sonrası olay komut satırı iletişim kutusu](../../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md).  
  
> [!NOTE]
> Derleme öncesi olayları, projenin güncel olduğundan ve hiçbir derlemenin tetiklenmesinin çalıştırmayın.  
  
 **Derleme sonrası olay komut satırı**  
 Oluşturma bittikten sonra yürütülecek herhangi bir komut belirtir. Uzun komutları yazmak için tıklatın **Düzenle derleme sonrası** görüntülenecek **derleme öncesi olay/derleme sonrası olay komut satırı iletişim kutusu**.  
  
> [!NOTE]
> Ekleme bir `call` .bat dosyaları çalıştıran tüm derleme sonrası komutları önce deyimi. Örneğin, `call C:\MyFile.bat` veya `call C:\MyFile.bat call C:\MyFile2.bat`.  
  
 **Derleme sonrası olayı Çalıştır**  
 Aşağıdaki tabloda gösterildiği gibi çalıştırmak derleme sonrası olay için aşağıdaki koşulları belirtir.  
  
|Seçenek|Sonuç|  
|------------|------------|  
|**Her zaman**|Derleme sonrası olay oluşturma işlemi başarılı olup olmadığını bağımsız olarak çalışır.|  
|**Başarıyla derlendiğinde**|Derleme başarılı olursa, derleme sonrası olay çalıştırılır. Bu nedenle, olayı oluşturma işlemi başarılı olduğu sürece, güncel, hatta bir proje için çalışır.|  
|**Derleme proje çıktısı zaman güncelleştirir**|Derleme sonrası olay, yalnızca derleyicinin çıktı dosyası (.exe veya .dll) önceki derleyici çıktı dosyasını farklı olduğunda çalışır. Bu nedenle, bir projenin güncel olması halinde bir derleme sonrası olay çalıştırılmaz.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Derleme olayları belirtme (Visual Basic)](../../ide/how-to-specify-build-events-visual-basic.md)   
 [Nasıl yapılır: Derleme olayları belirtme (C#)](../../ide/how-to-specify-build-events-csharp.md)   
 [Proje Özellikleri başvurusu](../../ide/reference/project-properties-reference.md)   
 [Derleme ve Oluşturma](../../ide/compiling-and-building-in-visual-studio.md)
