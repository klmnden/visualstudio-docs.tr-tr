---
title: 'Nasıl yapılır: Belge verilerine görünüm ekleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], custom - attach views to document data
ms.assetid: f92c0838-45be-42b8-9c55-713e9bb8df07
caps.latest.revision: 23
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 671a243f65c68660c98c3730ca90568882a824d6
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54755611"
---
# <a name="how-to-attach-views-to-document-data"></a>Nasıl yapılır: Belge Verilerine Görünüm Ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yeni bir belge görünümü varsa, var olan bir belge veri nesnesine iliştirme mümkün olabilir.  
  
### <a name="to-determine-if-you-can-attach-a-view-to-an-existing-document-data-object"></a>Var olan bir belge veri nesnesine ekleyebilirsiniz görünüm belirlemek için  
  
1.  Uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A>.  
  
2.  Uygulamanızda `IVsEditorFactory::CreateEditorInstance`, çağrı `QueryInterface` IDE çağırdığında mevcut belge verileri nesne üzerinde `CreateEditorInstance` uygulaması.  
  
     Çağırma `QueryInterface` , belirtilen mevcut belge veri nesnesi incelemenize olanak sağlayan `punkDocDataExisting` parametresi.  
  
     Tam arabirimler sorgulaması gerekir ancak bağlıdır, belgeyi açmayı Düzenleyicisi üzerinde 4. adımında belirtilen şekilde.  
  
3.  Mevcut belge veri nesnesi üzerinde uygun arabirimleri bulamazsanız, düzenleyiciniz belge veri nesnesi düzenleyiciniz ile uyumsuz olduğunu belirten bir hata kodu dönün.  
  
     IDE'nin uygulamasında <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenStandardEditor%2A>, belge başka bir düzenleyicide açık durumda olan ve kapatmak isteyip istemediğinizi soran bir ileti kutusu size bildirir.  
  
4.  Bu belge kapatırsanız, Visual Studio Düzenleyicisi Fabrika için ikinci bir kez çağırır. Bu çağrıda `DocDataExisting` parametresi NULL değerine eşittir. Düzenleyici fabrikası uygulamanız sonra belge veri nesnesi kendi Düzenleyicisi'nde açın.  
  
    > [!NOTE]
    >  Var olan bir belge veri nesnesi çalışıp çalışmadığını belirlemek için de arabirim uygulamasına özel bilgi gerçek bir işaretçiye atayarak kullanabilirsiniz [!INCLUDE[vcprvc](../includes/vcprvc-md.md)] özel uygulamanızın sınıfı. Örneğin, tüm standart düzenleyicileri uygulamak `IVsPersistFileFormat`, işlevinden devralan <xref:Microsoft.VisualStudio.OLE.Interop.IPersist>. Bu nedenle, çağırabilirsiniz `QueryInterface` için <xref:Microsoft.VisualStudio.OLE.Interop.IPersist.GetClassID%2A>, sınıf kimliği ve mevcut belge veri nesnesi üzerinde sınıf kimliği uygulamanızın eşleşip eşleşmediğini ve belge veri nesnesi ile çalışabilirsiniz.  
  
## <a name="robust-programming"></a>Güçlü Programlama  
 Visual Studio, uygulamanıza çağırdığında <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> yöntemi arabimini geri bir işaretçi ise mevcut belge veri nesnesine `punkDocDataExisting` varsa parametresi. Döndürülen belge veri nesnesini inceler `punkDocDataExisting` belge veri nesnesi bu konudaki yordamının 4. adımda not açıklandığı gibi düzenleyiciniz için uygun olup olmadığını belirlemek için. Uygun sonra Düzenleyici fabrikası ikinci bir görünüm için veriler açıklandığı şekilde sağlamalıdır [birden çok belge görünümünü destekleme](../extensibility/supporting-multiple-document-views.md). Aksi durumda, ardından uygun bir hata iletisi görüntülenmelidir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Birden çok belge görünümünü destekleme](../extensibility/supporting-multiple-document-views.md)   
 [Özel Düzenleyicilerde Belge Verileri ve Belge Görünümü](../extensibility/document-data-and-document-view-in-custom-editors.md)
