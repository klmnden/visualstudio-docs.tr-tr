---
title: 'Nasıl yapılır: Belgelerden yönetilen kod uzantılarını kaldırma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- managed code extensions [Office development in Visual Studio], removing
- documents [Office development in Visual Studio], managed code extensions
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 83bd57c8ffdcb268a560431c74806ddb6544d4e8
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71252165"
---
# <a name="how-to-remove-managed-code-extensions-from-documents"></a>Nasıl yapılır: Belgelerden yönetilen kod uzantılarını kaldırma
  Özelleştirme derlemesini, Microsoft Office Word veya Microsoft Office Excel için belge düzeyi özelleştirmenin parçası olan bir belge veya çalışma kitabından programlı bir şekilde kaldırabilirsiniz. Kullanıcılar daha sonra belgeleri açabilir ve içeriği görüntüleyebilir, ancak belgelere eklediğiniz herhangi bir özel kullanıcı arabirimi (UI) görünmez ve kodunuz çalışmaz.

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

 Özelleştirme derlemesini, `RemoveCustomization` [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]tarafından sunulan yöntemlerden birini kullanarak kaldırabilirsiniz. Hangi yöntemi kullanacağınızı, çalışma zamanında özelleştirmeyi kaldırmak isteyip istemediğinizi (yani, Word belgesi veya Excel çalışma kitabı açıkken özelleştirirken kod çalıştırarak) ya da özelleştirmeyi kapalı bir belgeden ya da istediğim bir belgeden kaldırmak istediğinize bağlıdır. Microsoft Office yüklü olmayan bir sunucuda s.

 ![video bağlantısı](../vsto/media/playvideo.gif "video bağlantısı") İlgili video gösterimi için bkz [. nasıl yapılır: Bir VSTO Derlemesini İliştirme veya bir Word belgesinden ayırma ](http://go.microsoft.com/fwlink/?LinkId=136782).

## <a name="to-remove-the-customization-assembly-at-run-time"></a>Çalışma zamanında özelleştirme derlemesini kaldırmak için

1. Özelleştirme kodunuzda <xref:Microsoft.Office.Tools.Word.Document.RemoveCustomization%2A> yöntemini (Word için) <xref:Microsoft.Office.Tools.Excel.Workbook.RemoveCustomization%2A> veya yöntemini (Excel için) çağırın. Bu yöntem yalnızca özelleştirmeye artık gerek duyulmadığında çağrılmalıdır.

     Kodunuzda bu yöntemi çağırdığınızda özelleştirmenin nasıl kullanıldığına bağlıdır. Örneğin, müşteriler, belgeyi yalnızca belgenin kendisi için ihtiyacı olan diğer istemcilere göndermeye hazırlanana kadar, özelleştirmenin özelliklerini kullanıyorsa, müşterinin tıkladığı zaman çağıran `RemoveCustomization` bazı Kullanıcı arabirimini sağlayabilirsiniz. Alternatif olarak, özelleştirmeniz ilk açıldığında belgeyi veriyle doldurursa, ancak özelleştirme doğrudan müşteriler tarafından erişilen başka herhangi bir özelliği sağlamıyorsa, özelleştirmenizin hemen ardından Removeccustomleştirme 'yı çağırabilirsiniz belgeyi başlatmayı sonlandırır.

## <a name="to-remove-the-customization-assembly-from-a-closed-document-or-a-document-on-a-server"></a>Bir sunucudaki kapalı bir belgeden veya bir belgeden özelleştirme derlemesini kaldırmak için

1. Konsol uygulaması veya Windows Forms projesi gibi Microsoft Office gerektirmeyen bir projede, *Microsoft. VisualStudio. Tools. Applications. ServerDocument. dll* derlemesine bir başvuru ekleyin.

2. Aşağıdaki **Içeri aktarmaları** veya **using** ifadesini, kod dosyanızın en üstüne ekleyin.

     [!code-csharp[Trin_VstcoreDeployment#1](../vsto/codesnippet/CSharp/Trin_VstcoreDeploymentCS/Program.cs#1)]
     [!code-vb[Trin_VstcoreDeployment#1](../vsto/codesnippet/VisualBasic/Trin_VstcoreDeploymentVB/Program.vb#1)]

3. <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> Sınıfının statik <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.RemoveCustomization%2A> yöntemini çağırın ve parametresi için çözüm belge yolunu belirtin.

     Aşağıdaki kod örneği, özelleştirmeyi masaüstündeki *WordDocument1. docx* adlı bir belgeden kaldırabildiğinizi varsayar.

     [!code-csharp[Trin_VstcoreDeployment#2](../vsto/codesnippet/CSharp/Trin_VstcoreDeploymentCS/Program.cs#2)]
     [!code-vb[Trin_VstcoreDeployment#2](../vsto/codesnippet/VisualBasic/Trin_VstcoreDeploymentVB/Program.vb#2)]

4. Projeyi derleyin ve özelleştirmeyi kaldırmak istediğiniz bilgisayarda uygulamayı çalıştırın. Bilgisayarda Office Runtime için Visual Studio 2010 Araçları yüklü olmalıdır.

## <a name="see-also"></a>Ayrıca bkz.
- [ServerDocument sınıfını kullanarak bir sunucudaki belgeleri yönetme](../vsto/managing-documents-on-a-server-by-using-the-serverdocument-class.md)
- [Nasıl yapılır: Belgelere yönetilen kod uzantıları iliştirme](../vsto/how-to-attach-managed-code-extensions-to-documents.md)
