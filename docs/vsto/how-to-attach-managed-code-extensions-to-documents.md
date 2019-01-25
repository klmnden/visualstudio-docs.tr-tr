---
title: 'Nasıl yapılır: Belgelere yönetilen kod uzantıları ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- managed code extensions [Office development in Visual Studio], attaching
- documents [Office development in Visual Studio], managed code extensions
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 5a2c218453edfa29d79ae4acb8dcf4ccd0010eab
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54865651"
---
# <a name="how-to-attach-managed-code-extensions-to-documents"></a>Nasıl yapılır: Belgelere yönetilen kod uzantıları ekleme
  Bir mevcut Microsoft Office Word belgesi veya Microsoft Office Excel çalışma kitabını özelleştirme bütünleştirilmiş kodu ekleyebilirsiniz. Belge veya çalışma kitabı Microsoft Office projeleri ve Visual Studio geliştirme araçları tarafından desteklenen herhangi bir dosya biçiminde olabilir. Daha fazla bilgi için [belge düzeyi özelleştirmeler mimarisi](../vsto/architecture-of-document-level-customizations.md).  
  
 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]  
  
 Bir Word veya Excel belgesi için bir özelleştirme eklemek için kullanın <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.AddCustomization%2A> yöntemi <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> sınıfı. Çünkü <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> sınıfı Microsoft Office'in yüklü olmayan bir bilgisayarda çalıştırılması için tasarlanmıştır, bu yöntem doğrudan Microsoft Office geliştirme (örneğin, bir konsolu veya Windows Forms uygulaması) için ilgili olmayan çözümleri kullanabilirsiniz.  
  
> [!NOTE]  
>  Özelleştirme kodunu belirtilen belgeyi sahip olmayan denetimleri bekliyorsa yüklenmesi başarısız olur.  
  
 ![video bağlantı](../vsto/media/playvideo.gif "video bağlantı") ilgili video gösterimi için bkz. [nasıl yaparım? Ekleme veya bir Word belgesi VSTO derlemesinden ayırma? ](http://go.microsoft.com/fwlink/?LinkId=136782).  
  
### <a name="to-attach-managed-code-extensions-to-a-document"></a>Yönetilen kod uzantıları belgeye eklemek için  
  
1.  Bir konsol uygulaması veya Windows Forms projesi gibi Microsoft Office gerektirmeyen bir proje başvurusu Ekle *Microsoft.VisualStudio.Tools.Applications.ServerDocument.dll* ve  *Microsoft.VisualStudio.Tools.Applications.Runtime.dll* derlemeler.  
  
2.  Aşağıdaki **içeri aktarmalar** veya **kullanarak** kod dosyanızın üstüne deyimleri.  
  
     [!code-csharp[Trin_VstcoreDeployment#4](../vsto/codesnippet/CSharp/Trin_VstcoreDeploymentCS/Program.cs#4)]
     [!code-vb[Trin_VstcoreDeployment#4](../vsto/codesnippet/VisualBasic/Trin_VstcoreDeploymentVB/Program.vb#4)]  
  
3.  Statik çağrı <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.AddCustomization%2A> yöntemi.  
  
     Aşağıdaki kod örneğinde <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.AddCustomization%2A> aşırı yükleme. Bu aşırı yükleme belgenin tam yolunu alır ve bir <xref:System.Uri> özelleştirmeleri için belgenin iliştirmek istediğiniz dağıtım bildiriminin konumunu belirtir. Bu örnek, bir Word belgesi adlı olduğunu varsayar **WordDocument1.docx** Masaüstü ve dağıtım bildirimini adlı bir klasörde bulunan **Yayımla** olan da masaüstünde.  
  
     [!code-csharp[Trin_VstcoreDeployment#3](../vsto/codesnippet/CSharp/Trin_VstcoreDeploymentCS/Program.cs#3)]
     [!code-vb[Trin_VstcoreDeployment#3](../vsto/codesnippet/VisualBasic/Trin_VstcoreDeploymentVB/Program.vb#3)]  
  
4.  Projeyi oluşturmak ve uygulamayı özelleştirme iliştirmek istediğiniz bilgisayarda çalıştırın. Bilgisayarda Office yüklü çalışma zamanı için Visual Studio 2010 Araçları yüklü olmalıdır.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [ServerDocument sınıfını kullanarak bir sunucu üzerinde belgeleri yönetme](../vsto/managing-documents-on-a-server-by-using-the-serverdocument-class.md)   
 [Nasıl yapılır: Belgelerden yönetilen kod uzantılarını kaldırma](../vsto/how-to-remove-managed-code-extensions-from-documents.md)   
 [Office çözümlerinde uygulama ve dağıtım bildirimleri](../vsto/application-and-deployment-manifests-in-office-solutions.md)  
