---
title: 'Nasıl yapılır: Eski dil hizmetinde ana hat oluşturma desteği | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], collapse to definitions command
- language services, supporting Collapse to Definitions command
- hidden text, Collapse to Definitions command
ms.assetid: bb6e74c3-93e4-4ef7-afc7-1c9b342f083b
caps.latest.revision: 18
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d92baa824dbb70dd591cadef99775f943c651aef
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63436151"
---
# <a name="how-to-support-outlining-in-a-legacy-language-service"></a>Nasıl yapılır: Eski Dil Hizmetinde Ana Hat Oluşturmayı Destekleme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Anahat oluşturma, genişletme veya daraltma farklı bölgelerdeki metin için kullanılır. Anahat oluşturma şekilde kullanılan tarafından farklı dillerde farklı şekilde tanımlanabilir. Daha fazla bilgi için [anahat](../../ide/outlining.md).  
  
 Eski dil Hizmetleri bir VSPackage'ı bir parçası olarak uygulanır, ancak dil hizmeti özellikleri uygulamak için daha yeni MEF uzantıları kullanmaktır. Anahat oluşturma uygulamak için en yeni yolu hakkında daha fazla bilgi için bkz: [izlenecek yol: Anahat oluşturma](../../extensibility/walkthrough-outlining.md).  
  
> [!NOTE]
> Yeni bir düzenleyici API hemen kullanmaya başlamak öneririz. Bu dil hizmetinizin performansını ve yeni düzenleyici özellikleri yararlanmanıza olanak tanır.  
  
 Bu komut, language service Pro desteklemek nasıl gösterir.  
  
### <a name="to-support-outlining"></a>Ana hat oluşturmayı desteklemek için  
  
1. Uygulama <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningCapableLanguage> dil hizmeti nesneniz üzerinde.  
  
2. Çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningSession.AddOutlineRegions%2A> yeni anahat bölge ekleme için anahat oluşturma geçerli oturum nesnesi üzerinde.  
  
## <a name="robust-programming"></a>Güçlü Programlama  
 Bir kullanıcı seçtiğinde **Daralt tanımları** üzerinde **anahat** menüsü, IDE çağrıları <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningCapableLanguage.CollapseToDefinitions%2A> dil hizmetinizde.  
  
 Bu yöntem çağrıldığında, IDE içinde geçen bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines> işaretçi (işaretçiye bir metin arabelleği için) ve bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningSession> (geçerli anahat oluşturma oturumu için bir işaretçi).  
  
 Çağırabilirsiniz <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningSession.AddOutlineRegions%2A> yöntemi bu bölgelerde belirterek, birden çok ana hat bölgeler için `rgOutlnReg` parametresi. `rgOutlnReg` Parametresi bir <xref:Microsoft.VisualStudio.TextManager.Interop.NewOutlineRegion> yapısı. Bu işlem, belirli bir bölge genişletilmiş veya daraltılmış gibi gizli bölge farklı özelliklerini belirtmenize olanak sağlar.  
  
> [!NOTE]
> Yeni satır karakterleri gizleme hakkında dikkatli olun. Gizli metin ilk satırını başından son karakter bir bölümdeki son satırın son yeni satır karakteri görünür bırakmak genişletmelidir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Eski dil hizmetinde gizli metin desteği](../../extensibility/internals/how-to-provide-hidden-text-support-in-a-legacy-language-service.md)   
 [Nasıl yapılır: Eski Dil Hizmetinde Genişletilmiş Ana Hat Oluşturma Desteği Sağlama](../../extensibility/internals/how-to-provide-expanded-outlining-support-in-a-legacy-language-service.md)
