---
title: 'Nasıl yapılır: Projeye özgü düzenleyicileri açma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- project types, opening a project-specific editor
- editors [Visual Studio SDK], opening project-specific editors
- projects [Visual Studio SDK], opening folders
ms.assetid: 83e56d39-c97b-4c6b-86d6-3ffbec97e8d1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4d90a748627b3a2345e40eac7c1894e87673d1ca
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56693262"
---
# <a name="how-to-open-project-specific-editors"></a>Nasıl yapılır: Projeye özgü düzenleyicileri açma
Bir proje tarafından açılmış bir öğe dosyası doğası gereği bu proje için belirli düzenleyiciye bağlıysa, proje dosyası bir projeye özgü Düzenleyicisi'ni kullanarak açmanız gerekir. Dosya bir düzenleyicide seçme IDE'nin mekanizması aşağı temsilci olarak seçilemez. Örneğin, standart bir bit eşlem Düzenleyicisi kullanmak yerine, projeniz için benzersiz olan bilgileri tanıdığı bir belirli bir bit eşlem Düzenleyicisi belirtmek için bu projeye özgü Düzenleyicisi seçeneği kullanabilirsiniz.

 IDE çağrıları <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3.OpenItem%2A> yöntemi belirli bir proje tarafından bir dosyanın açılması gerektiğini belirler. Daha fazla bilgi için [Aç komutunu kullanarak dosyaları görüntüleme](../extensibility/internals/displaying-files-by-using-the-open-file-command.md). Uygulamak için aşağıdaki kılavuzları kullanın `OpenItem` projenizin bir projeye özgü Düzenleyicisi'ni kullanarak bir dosyayı açmak için yöntemi.

## <a name="to-implement-the-openitem-method-with-a-project-specific-editor"></a>Bir projeye özgü düzenleyicisiyle OpenItem yöntemi uygulamak için

1.  Çağrı <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable.FindAndLockDocument%2A> yöntemi (`RDT_EditLock`) (belge veri nesnesi) dosya zaten açık olup olmadığını belirlemek için.

    > [!NOTE]
    >  Belge verileri ve belge görünümü nesneleri hakkında daha fazla bilgi için bkz. [belge verileri ve belge görünümü özel düzenleyicilerde](../extensibility/document-data-and-document-view-in-custom-editors.md).

2.  Dosya zaten açık değilse, dosya çağırarak resurface <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.IsDocumentOpen%2A> yöntemi ve IDO_ActivateIfOpen için bir değer belirterek `grfIDO` parametresi.

     Dosya açıksa ve arama projenin dışında bir proje belge sahibi, başka bir projeden açılmasını Düzenleyicisi kullanıcı için bir uyarı görüntülenir. Dosya penceresini kullanıma sunulur.

3.  Metin arabelleği (belge veri nesnesi) zaten açık olan ve başka bir görünüme eklemek istiyorsanız, bu görünüm takma için sorumludur. Projeden bir görünüm (belge görünümü nesnesi) örnekleme için önerilen yaklaşım şu şekildedir:

    1.  Çağrı `QueryService` üzerinde <xref:Microsoft.VisualStudio.Shell.Interop.SLocalRegistry> işaretçisi almak için hizmeti <xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2> arabirimi.

    2.  Çağrı <xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2.CreateInstance%2A> belge görünümü sınıfının bir örneğini oluşturmak için yöntemi.

4.  Çağrı <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.CreateDocumentWindow%2A> yöntemi, belge görünüm nesnesi belirtme.

     Bu yöntem, bir belge penceresi içinde belge view nesnesinin siteler.

5.  Ya da uygun çağrıları gerçekleştirmek <xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat.InitNew%2A> veya <xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat.Load%2A> yöntemleri.

     Bu noktada, görünüm, tam olarak başlatılmış ve açılması hazır olması gerekir.

6.  Çağrı <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.Show%2A> Göster ve görünümü açmak için yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [Açın ve proje öğeleri Kaydet](../extensibility/internals/opening-and-saving-project-items.md)
- [Nasıl yapılır: Açık standart düzenleyicileri](../extensibility/how-to-open-standard-editors.md)
- [Nasıl yapılır: Açık belgeler için düzenleyicileri açma](../extensibility/how-to-open-editors-for-open-documents.md)