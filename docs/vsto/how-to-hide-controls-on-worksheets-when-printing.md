---
title: 'Nasıl yapılır: Yazdırırken çalışma sayfası denetimlerini gizleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- printing [Office development in Visual Studio], worksheets
- controls [Office development in Visual Studio], hiding while printing
- printing [Office development in Visual Studio], hiding controls
- worksheets, hiding controls when printing
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: a236b30552007112663ad9f985ddc94995fe1ef8
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60050030"
---
# <a name="how-to-hide-controls-on-worksheets-when-printing"></a>Nasıl yapılır: Yazdırırken çalışma sayfası denetimlerini gizleme
  Windows Forms denetimleri içeren bir Microsoft Office Excel belge yazdırma sırasında denetimleri yazdırılan çalışma sayfalarında görünür. Bir çalışma sayfası yazdırma sırasında denetimleri gizleyebilirsiniz.

 [!INCLUDE[appliesto_xlalldoc](../vsto/includes/appliesto-xlalldoc-md.md)]

> [!NOTE]
>  Verileri görüntüleyen denetimler gizlerseniz bir <xref:Microsoft.Office.Tools.Excel.Controls.TextBox>, denetiminde verileri yazdırılan çalışma sayfalarında görünür olmaz.

> [!NOTE]
>  Bilgisayarınız, aşağıdaki yönergelerde yer alan Visual Studio kullanıcı arabirimi öğelerinden bazıları için farklı adlar veya konumlar gösterebilir. Sahip olduğunuz Visual Studio sürümü ve kullandığınız ayarlar bu öğeleri belirler. Daha fazla bilgi için [Visual Studio IDE'yi kişiselleştirme](../ide/personalizing-the-visual-studio-ide.md).

## <a name="to-hide-controls-when-a-worksheet-is-printed"></a>Bir çalışma sayfası denetimlerini gizle yazdırıldığında

1. Oluşturun veya Excel projenizi Visual Studio'da açın ve doğrulayın **Sayfa1** Tasarımcısı'nda görülebilir. Proje oluşturma hakkında daha fazla bilgi için bkz: [nasıl yapılır: Visual Studio'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md).

2. Gelen **ortak denetimleri** sekmesinde **araç kutusu**, sürükleyin bir <xref:Microsoft.Office.Tools.Excel.Controls.Button> denetlemek için bir hücre `Sheet1`.

3. İçinde **özellikleri** penceresinde <xref:Microsoft.Office.Tools.Excel.Controls.Button.PrintObject%2A> özelliğini **False**.

## <a name="see-also"></a>Ayrıca bkz.
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Windows Forms denetimlerine Office belgeleri genel bakış](../vsto/windows-forms-controls-on-office-documents-overview.md)
- [Nasıl yapılır: Office belgelerine Windows Forms denetimleri ekleme](../vsto/how-to-add-windows-forms-controls-to-office-documents.md)
- [Nasıl yapılır: Çalışma sayfası hücreleri içinde denetimleri yeniden boyutlandırma](../vsto/how-to-resize-controls-within-worksheet-cells.md)
