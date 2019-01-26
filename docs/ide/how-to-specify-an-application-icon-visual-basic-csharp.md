---
title: 'Nasıl yapılır: Uygulama simgesi belirtme (Visual Basic, C#)'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: a1e2502d2844b32f6f5e1c22c7fcddf7d6287c8d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55039351"
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