---
title: 'Nasıl Yapılır: Yazdırırken çalışma sayfası denetimlerini gizleme'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
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
manager: douge
ms.workload:
- office
ms.openlocfilehash: 322c314a768545996f343526367de44c667ce89b
ms.sourcegitcommit: a205ff1b389fba1803acd32c54df7feb0ef7a203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53646805"
---
# <a name="how-to-hide-controls-on-worksheets-when-printing"></a>Nasıl Yapılır: Yazdırırken çalışma sayfası denetimlerini gizleme
  Windows Forms denetimleri içeren bir Microsoft Office Excel belge yazdırma sırasında denetimleri yazdırılan çalışma sayfalarında görünür. Bir çalışma sayfası yazdırma sırasında denetimleri gizleyebilirsiniz.  
  
 [!INCLUDE[appliesto_xlalldoc](../vsto/includes/appliesto-xlalldoc-md.md)]  
  
> [!NOTE]  
>  Verileri görüntüleyen denetimler gizlerseniz bir <xref:Microsoft.Office.Tools.Excel.Controls.TextBox>, denetiminde verileri yazdırılan çalışma sayfalarında görünür olmaz.  
  
> [!NOTE]  
>  Bilgisayarınız, aşağıdaki yönergelerde yer alan Visual Studio kullanıcı arabirimi öğelerinden bazıları için farklı adlar veya konumlar gösterebilir. Sahip olduğunuz Visual Studio sürümü ve kullandığınız ayarlar bu öğeleri belirler. Daha fazla bilgi için [Visual Studio IDE'yi kişiselleştirme](../ide/personalizing-the-visual-studio-ide.md).  
  
## <a name="to-hide-controls-when-a-worksheet-is-printed"></a>Bir çalışma sayfası denetimlerini gizle yazdırıldığında  
  
1.  Oluşturun veya Excel projenizi Visual Studio'da açın ve doğrulayın **Sayfa1** Tasarımcısı'nda görülebilir. Proje oluşturma hakkında daha fazla bilgi için bkz: [nasıl yapılır: Visual Studio'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md).  
  
2.  Gelen **ortak denetimleri** sekmesinde **araç kutusu**, sürükleyin bir <xref:Microsoft.Office.Tools.Excel.Controls.Button> denetlemek için bir hücre `Sheet1`.  
  
3.  İçinde **özellikleri** penceresinde <xref:Microsoft.Office.Tools.Excel.Controls.Button.PrintObject%2A> özelliğini **False**.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)   
 [Windows Forms denetimlerine Office belgeleri genel bakış](../vsto/windows-forms-controls-on-office-documents-overview.md)   
 [Nasıl yapılır: Office belgelerine Windows Forms denetimleri ekleme](../vsto/how-to-add-windows-forms-controls-to-office-documents.md)   
 [Nasıl yapılır: Çalışma sayfası hücreleri içinde denetimleri yeniden boyutlandırma](../vsto/how-to-resize-controls-within-worksheet-cells.md)  
  
  