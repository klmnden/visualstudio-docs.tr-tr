---
title: Yönetilen başvuru (Visual Studio'da Office Geliştirme)
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- reference [Office development in Visual Studio], 2007 Microsoft Office system
- Office development in Visual Studio, reference
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: f8ff9a196fb459359502e4c9f8599fbdeff3e1ce
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63438802"
---
# <a name="managed-reference-office-development-in-visual-studio"></a>Yönetilen başvuru (Visual Studio'da Office Geliştirme)
  Bu bölümde, ad alanları için API başvuru belgeleri bulunur ve Office içinde kullanılan türleri hedefleyen projeleri [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya [!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)]. Visual Studio belgelerinde aşağıdaki başvuru bölümüne .NET Framework 3. 5'i hedefleyen Office projelerinde kullanılan türler ve ad alanları hakkında API başvuru belgeleri için bkz: [ http://go.microsoft.com/fwlink/?LinkId=160658 ](http://go.microsoft.com/fwlink/?LinkId=160658).

> [!NOTE]
> Office deneyiminiz boyunca genişleten çözümleri geliştirme yapmakla mı ilgileniyorsunuz [birden çok platform](https://dev.office.com/add-in-availability)? Yeni kontrol [Office eklentilerini modeli](https://dev.office.com/docs/add-ins/overview/office-add-ins). Office eklentileri, VSTO eklentileri ve çözümlerle karşılaştırıldığında küçük ayak izine sahip ve neredeyse tüm web teknolojisi, HTML5, JavaScript, CSS3 ve XML gibi programlama kullanarak oluşturabilirsiniz.

## <a name="in-this-section"></a>Bu bölümde
 <xref:Microsoft.Office.Tools>

 Office çözümleri programlama için ortak olan sınıflar içerir. Bunlar, VSTO eklentileri, VSTO eklentileri içinde özel görev bölmeleri oluşturma için sınıflar, akıllı etiketler Excel ve Word çözümleri oluşturmak için sınıfları ve Eylemler bölmelerini belge düzeyi özelleştirmelerini oluşturmak için sınıflar için temel sınıfı içerir.

 <xref:Microsoft.Office.Tools.Excel>

 Konak denetimleri ve Excel için çözümlerinde kullanılabilir konak öğeleri içerir.

 <xref:Microsoft.Office.Tools.Excel.Controls>

 Excel denetimleri ve Excel için çözümlerinde kullanılabilir Windows Forms denetimleri içerir.

 <xref:Microsoft.Office.Tools.Outlook>

 Özel form bölgeleri oluşturma için kullanılan sınıflar da dahil olmak üzere Outlook için VSTO eklentileri tarafından kullanılan sınıfları içerir.

 <xref:Microsoft.Office.Tools.Ribbon>

 Şerit Tasarımcısını kullanarak oluşturulan Şerit özelleştirmeleri programlı olarak değiştirmek için kullanılan sınıfları içerir.

 <xref:Microsoft.Office.Tools.Word>

 Konak denetimlerinin ve çözümleri için Word kullanılabilir konak öğeleri içerir.

 <xref:Microsoft.Office.Tools.Word.Controls>

 Word denetimleri ve çözümler Word için kullanılabilen Windows Forms denetimleri içerir.

 <xref:Microsoft.VisualStudio.Tools.Applications>

 İçeren <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> sınıfı ve bir dizi ilgili önbelleğe alınmış veri sınıfları. Bu sınıflar, Microsoft Office yüklü olmayan bilgisayarlarda belge düzeyi özelleştirmeleri bazı yönlerini değiştirmek için kullanılabilir.

 <xref:Microsoft.VisualStudio.Tools.Applications.Deployment>

 İçeren <xref:Microsoft.VisualStudio.Tools.Applications.Deployment.IAddInPostDeploymentAction> arabirimi (oluşturmak için uygulayabileceğiniz bir *dağıtım eylem* bir Office çözümü için), bir Office çözümünü yükleme sırasında oluşturulan özel durumları ve görsel bir parçası olan diğer API'ler Studio altyapı.

 <xref:Microsoft.VisualStudio.Tools.Applications.Runtime>

 Tarafından oluşturulan özel durumları çoğunu içeren [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)], verileri belge düzeyi özelleştirmelerdeki önbelleğe almak için kullanılabilecek çeşitli sınıflar ve Visual Studio altyapısının bir parçası olan diğer API'ler.

 <xref:Microsoft.VisualStudio.Tools.Office.BuildTasks>

 Office projeleri derlemek için kullanılan MSBuild görevi sınıfları içerir.

## <a name="see-also"></a>Ayrıca bkz.
- [Office çalışma zamanına genel bakış için Visual Studio Araçları](../vsto/visual-studio-tools-for-office-runtime-overview.md)
- [Başlama &#40;Visual Studio'da Office geliştirme&#41;](../vsto/getting-started-office-development-in-visual-studio.md)
- [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)
- [Office çözümleri oluşturma ve tasarlama](../vsto/designing-and-creating-office-solutions.md)
