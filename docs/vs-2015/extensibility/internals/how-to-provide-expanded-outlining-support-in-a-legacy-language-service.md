---
title: 'Nasıl yapılır: Eski dil hizmetinde genişletilmiş ana hat oluşturma desteği sağlayın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], outlining support
- language services, supporting outlining
- outlining, supporting
ms.assetid: df759e89-8193-418c-8038-6626304d387b
caps.latest.revision: 17
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: b1b2fd8f3d7e4f3637957ef11c4acb20ba51261d
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63442670"
---
# <a name="how-to-provide-expanded-outlining-support-in-a-legacy-language-service"></a>Nasıl yapılır: Eski Dil Hizmetinde Genişletilmiş Ana Hat Oluşturma Desteği Sağlama
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Ana hat oluşturma desteği destekleyen ötesinde dil genişletmek için iki seçenek **tanımlara Daralt** komutu. Düzenleyici tarafından denetlenen anahat bölge ekleme ve istemci tarafından denetlenen anahat bölge ekleme.  
  
## <a name="adding-editor-controlled-outline-regions"></a>Düzenleyici tarafından denetlenen anahat bölge ekleme  
 Daraltılmış, bir anahat bölgesi oluşturmak ve ardından bölge genişletilmiş olmadığını işlemek için Düzenleyici'izin vermek için bu yaklaşımı kullanın ve VS. Ana hat oluşturma desteği sağlamak için bu iki seçenekten birini bu az güçlü seçenektir. İçin bu seçeneği kullanarak metni belirtilen aralığı yeni bir ana hat bölge oluşturma <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningSession.AddOutlineRegions%2A>. Bu bölge oluşturulduktan sonra davranışını düzenleyici tarafından denetlenir. Düzenleyici tarafından denetlenen anahat bölgeleri uygulamak için aşağıdaki yordamı kullanın.  
  
#### <a name="to-implement-an-editor-controlled-outline-region"></a>Bir düzenleyici tarafından denetlenen anahat bölgesi uygulamak için  
  
1. Çağrı `QueryService` için <xref:Microsoft.VisualStudio.TextManager.Interop.SVsTextManager>  
  
     Bu bir işaretçi döndürür <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager>.  
  
2. Çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.GetHiddenTextSession%2A>, verilen metin arabelleği için bir işaretçi olarak geçen. Bu bir işaretçi döndürür <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession> arabellek için nesne.  
  
3. Çağrı <xref:System.Runtime.InteropServices.Marshal.QueryInterface%2A> üzerinde <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession> işaretçisi için <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningSession>.  
  
4. Çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningSession.AddOutlineRegions%2A> ekleyin ya da daha yeni bir kerede bölgeleri genel çizgileriyle belirtin.  
  
     Bu yöntem anahat, mevcut anahat bölgeleri olup kaldırıldı veya korunur ve olup anahat bölge genişletilmiş veya varsayılan olarak daraltılmış metin aralığı belirtmenize olanak tanır.  
  
## <a name="adding-client-controlled-outline-regions"></a>İstemci tarafından denetlenen anahat bölge ekleme  
 Kullandığı gibi istemci tarafından denetlenen (veya akıllı) uygulama anahat oluşturma için bu yaklaşımı kullanın [!INCLUDE[csprcs](../../includes/csprcs-md.md)] ve [!INCLUDE[vbprvb](../../includes/vbprvb-md.md)] dil Hizmetleri. Kendi ana hattı yöneten bir dil hizmeti, bunlar geçersiz olduğunda eski anahat bölgeleri yok etmek için ve gerektiğinde yeni anahat bölgesi oluşturmak için metin arabelleği içeriği izler.  
  
#### <a name="to-implement-a-client-controlled-outline-region"></a>Bir istemci tarafından denetlenen anahat bölgeye uygulamak için  
  
1. Çağrı `QueryService` için <xref:Microsoft.VisualStudio.TextManager.Interop.SVsTextManager>. Bu bir işaretçi döndürür <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager>.  
  
2. Çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.GetHiddenTextSession%2A>, verilen metin arabelleği için bir işaretçi olarak geçen. Bu, gizli metin oturumu zaten için arabellek var olup olmadığını belirler.  
  
3. Metin oturum zaten var ve ardından, biri ve var olan bir işaretçi oluşturmak ihtiyacınız yoktur, <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession> nesne döndürülür. Bu işaretçinin, listeleme ve ana hat bölgeler oluşturmak için kullanın. Aksi takdirde, çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.CreateHiddenTextSession%2A> arabellek için gizli metin oturum oluşturmak için. Bir işaretçi <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession> nesne döndürülür.  
  
    > [!NOTE]
    > Çağırdığınızda <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.CreateHiddenTextSession%2A>, gizli metin istemci belirtebilirsiniz (diğer bir deyişle, bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextClient> nesne). Bu istemci gizli metin olduğunda sizi bilgilendirir veya ana bölge genişletilmiş veya daraltılmış kullanıcı tarafından.  
  
4. Çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession.AddHiddenRegions%2A> yapısı) parametre: Bir değer belirleyebilirsiniz <xref:Microsoft.VisualStudio.TextManager.Interop.HIDDEN_REGION_TYPE> içinde `iType` üyesi <xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion> yapısı gizli bölge yerine bir anahat bölgesi oluşturmakta olduğunuz belirtmek için. Bölge istemci tarafından denetlenen veya Düzenleyicisi tarafından denetlenen içinde olup olmadığını belirtin `dwBehavior` üyesi <xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion> yapısı. Akıllı ana hat oluşturma uygulamanız anahat bölgeleri Düzenleyicisi ve istemci denetlenen bir karışımını içerebilir. Anahat bölgeniz, "... gibi", buna daraltıldığında görüntülenen başlık metnini belirtin `pszBanner` üyesi <xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion> yapısı. Editör'ün varsayılan başlık metni gizli bölge için "...".
