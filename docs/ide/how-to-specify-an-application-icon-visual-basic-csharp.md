---
title: 'Nasıl yapılır: Uygulama simgesi belirtme (Visual Basic, C#)'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- icons [Visual Studio], application
- application properties [Visual Studio], icons
- application icons [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: f2903821c0e0843de43f68d67cc64c344ab95e02
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62547786"
---
# <a name="how-to-specify-an-application-icon-visual-basic-c"></a>Nasıl yapılır: Uygulama simgesi belirtme (Visual Basic, C#)

`Icon` Özelliği bir proje için simge dosyasını belirtir (*.ico*) derlenmiş uygulama için gösterilecek **dosya Gezgini** ve Windows görev çubuğunda.

`Icon` Özelliği erişilebilir **uygulama** bölmesinde **Proje Tasarımcısı**; bir projeye kaynaklar veya içerik dosyaları olarak eklenen simge listesi içerir.

> [!NOTE]
> Bir uygulama için bir Icon özelliği ayarlandıktan sonra ayrıca ayarlayabilirsiniz `Icon` her özellik **penceresi** veya **Form** uygulama. Windows Presentation Foundation (WPF) tek başına uygulamalar için pencere simgeleri hakkında daha fazla bilgi için bkz. <xref:System.Windows.Window.Icon%2A> özelliği.

## <a name="to-specify-an-application-icon"></a>Uygulama simgesi belirtmek için

1. İçinde **Çözüm Gezgini**, bir proje düğümü seçin (değil **çözüm** düğümü).

1. Menü çubuğunda, **proje** > **özellikleri**.

1. Zaman **Proje Tasarımcısı** görüntülenirse, seçin **uygulama** sekmesi.

1. **(Visual Basic)**  &mdash;İçinde **simgesi** listesinde, bir simge seçin (*.ico*) dosyası.

    **C#**&mdash;Neredeyse **simgesi** listesinde  **\<Gözat … >** düğmesini ve ardından istediğiniz simge dosyasının konumuna göz atın.

## <a name="see-also"></a>Ayrıca bkz.

- [Uygulama sayfası, Proje Tasarımcısı (Visual Basic)](../ide/reference/application-page-project-designer-visual-basic.md)
- [Uygulama sayfası, Proje Tasarımcısı (C#)](../ide/reference/application-page-project-designer-csharp.md)