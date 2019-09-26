---
title: ServerDocument sınıfını kullanarak bir sunucudaki belgeleri yönetme
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], managing on server
- Office documents [Office development in Visual Studio, managing on server
- ServerDocument class, managing documents on server
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 739946fc7fc6ea7014fb93010ca85094a7fc7056
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71251926"
---
# <a name="manage-documents-on-a-server-by-using-the-serverdocument-class"></a>ServerDocument sınıfını kullanarak bir sunucudaki belgeleri yönetme
  Microsoft Office Word ve Microsoft Office `ServerDocument` Excel yüklenmemiş olsa [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] bile belge düzeyi özelleştirmelerinin çeşitli yönlerini yönetmek için içindeki sınıfını kullanabilirsiniz. Aşağıdaki görevleri gerçekleştirebilirsiniz:

- Bir belge veya çalışma kitabının veri önbelleğindeki verilere erişin ve verileri değiştirin. Daha fazla bilgi için bkz. [belgedeki önbelleğe alınmış verilerle çalışma](#CachedData).

- Bir belgeyle ilişkili özelleştirme derlemesini yönetin. Daha fazla bilgi için bkz. [belge özelleştirmesini yönetme](#CustomizationInfo).

  [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

## <a name="understand-the-serverdocument-class"></a>ServerDocument sınıfını anlayın
 `ServerDocument` Sınıfı, Office yüklü olmayan bilgisayarlarda kullanılmak üzere tasarlanmıştır. Bu nedenle, genellikle bu sınıfı, Office projeleri yerine konsol projeleri veya Windows Forms projeleri gibi Office ile tümleştirilebilen uygulamalarda kullanırsınız. *Microsoft. VisualStudio. Tools. Applications. ServerDocument. dll* derlemesindeki sınıfınıkullanın.<xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument>

 `ServerDocument` Sınıfı kullanılarak[!INCLUDE[vs_dev12](../vsto/includes/vs-dev12-md.md)]oluşturulmuş belge düzeyi özelleştirmelerde işlem yapmak için kullanılabilir.

 Office çalışma zamanı için Visual Studio 2010 araçları ve .NET Framework için Office uzantıları hakkında daha fazla bilgi için, bkz. [Office çalışma zamanına genel bakış için Visual Studio Araçları](../vsto/visual-studio-tools-for-office-runtime-overview.md).

> [!NOTE]
> Sisteminde sınıfını kullanan eski bir uygulamanız varsa (sürüm `Visual Studio Tools for Office` 3,0 çalışma zamanı), uygulamayı çalıştıran bilgisayarlarda sistem (sürüm 3,0 çalışma zamanı) yüklü olmalıdır. `ServerDocument` `Visual Studio Tools for Office` `Visual Studio 2010 Tools for Office runtime` Bu uygulamalar çalıştırılamaz.

## <a name="CachedData"></a>Belgedeki önbelleğe alınmış verilerle çalışma
 `ServerDocument` Sınıfı, özelleştirilmiş belgelerde veri önbelleğiyle çalışmak için kullanabileceğiniz Üyeler sağlar. Önbelleğe alınan veriler hakkında daha fazla bilgi için bkz. sunucudaki belgelerdeki verileri [önbelleğe alma](../vsto/caching-data.md) ve [verilere erişme](../vsto/accessing-data-in-documents-on-the-server.md).

 Aşağıdaki tabloda, önbelleğe alınmış verilerle çalışmak için kullanabileceğiniz üyeler listelenmektedir.

|Görev|Kullanılacak üye|
|----------|-------------------|
|Bir belgenin veri önbelleğine sahip olup olmadığını belirleme.|<xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.IsCacheEnabled%2A> Yöntemi.|
|Bir belgedeki önbelleğe alınmış verilere erişmek için.<br /><br /> Daha fazla bilgi için bkz. [sunucudaki belgelerdeki verilere erişme](../vsto/accessing-data-in-documents-on-the-server.md).|<xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.CachedData%2A> Özelliği.|

## <a name="CustomizationInfo"></a>Belge özelleştirmesini yönetme
 Bir belgeyle ilişkili özelleştirme derlemesini yönetmek `ServerDocument` için sınıfının üyelerini kullanabilirsiniz. Örneğin, belgenin artık özelleştirmenin bir parçası olmaması için özelleştirmeyi bir belgeden program aracılığıyla kaldırabilirsiniz.

 Aşağıdaki tabloda, özelleştirme derlemesini yönetmek için kullanabileceğiniz üyeler listelenmektedir.

|Görev|Kullanılacak üye|
|----------|-------------------|
|Belge düzeyi özelleştirmenin bir parçası olup olmadığını belirleme.|<xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.GetCustomizationVersion%2A> Yöntemi.|
|Çalışma zamanında bir belgeye programlı bir şekilde özelleştirme eklemek için.<br /><br /> Daha fazla bilgi için [nasıl yapılır: Belgelere yönetilen kod uzantıları iliştirme](../vsto/how-to-attach-managed-code-extensions-to-documents.md)|<xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.AddCustomization%2A> Yöntemlerden biri.|
|Çalışma zamanında bir belgeden program aracılığıyla özelleştirmeyi kaldırma.<br /><br /> Daha fazla bilgi için [nasıl yapılır: Yönetilen kod uzantılarını belgelerden](../vsto/how-to-remove-managed-code-extensions-from-documents.md)kaldırın.|<xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.RemoveCustomization%2A> Yöntemi.|
|Belgeyle ilişkili dağıtım bildiriminin URL 'sini almak için.|<xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.DeploymentManifestUrl%2A> Özelliği.|

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Belgelere yönetilen kod uzantıları iliştirme](../vsto/how-to-attach-managed-code-extensions-to-documents.md)
- [Nasıl yapılır: Belgelerden yönetilen kod uzantılarını kaldırma](../vsto/how-to-remove-managed-code-extensions-from-documents.md)
- [Office çalışma zamanına genel bakış için Visual Studio Araçları](../vsto/visual-studio-tools-for-office-runtime-overview.md)
- [Önbellek verileri](../vsto/caching-data.md)
