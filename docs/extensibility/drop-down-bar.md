---
title: Aşağı açılan çubuğu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - drop-down bar
ms.assetid: 4bb621bd-72f5-43d5-916f-9f66617da049
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bb1501159ad0feb9facce8e2b3969f8fabfe684a
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66324294"
---
# <a name="drop-down-bar"></a>Aşağı açılan çubuğu
Aşağı açılan çubuğu kod penceresinin en üstünde sağlanır ve iki açılan listeleri içerir.

## <a name="drop-down-bar-interfaces"></a>Aşağı açılan çubuğu arabirimleri
 İçinde [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)], örneğin, aşağı açılan çubuğu listelerini içerir [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)] öğeleri ve [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)] öğeleri üye işlevleri aşağıdaki resimde gösterildiği gibi.

 ![DROP&#45;aşağı çubukları](../extensibility/media/vsdropdown_bar.gif "vsDropdown_bar") çubuğu açılır

 Bir açılan çubuğu uygularken birincil önem dört arabirimi vardır:

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsDropdownBarClient>

     Aşağı açılan çubuğunun içeriğini eklemek için bu arabirimi uygulayın. Her bir açılan birleşimini düz metin veya başvurmaktan metin içerebilir (kalın, italik veya alt çizgi), pencere metin yazı tipi renkleri veya çıkış gri yazı tipi renklendirme sahip olabilir ve isteğe bağlı olarak açılan öğesinin yanındaki küçük bir bit eşlem sağlayabilir. Benzer şekilde <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCompletionSet> arabirimi, bit eşlem resimleri görüntü listeleri sağlanır. Farklı bir görüntü listesini her bir açılan bileşimi olabilir; Ancak, her bir görüntü listesi görüntüler aynı yükseklikte içermelidir. Ayrıca, kullanarak <xref:Microsoft.VisualStudio.TextManager.Interop.IVsDropdownBarClient.GetComboTipText%2A> yöntemi, her bir birleşimi için bir araç ipucu sağlayabilir.

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsDropdownBarManager>

     Bu arabirim oluşturmak veya bir kod penceresinde açılan çubuğunu yok etmek için çağırın. Bu arabirim, aşağı açılan çubuğu zaten bir kod penceresine çağırarak ekli olup olmadığını belirlemek için de kullanılabilir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsDropdownBarManager.GetDropdownBar%2A> yöntemi. Çağrı <xref:System.Runtime.InteropServices.Marshal.QueryInterface%2A> için <xref:Microsoft.VisualStudio.TextManager.Interop.IVsDropdownBarManager> gelen <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow>.

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsDropdownBar>

     Doğrudan aşağı açılan çubuğu ile iletişim kurmak için bu arabirimi çağırın. Bu arabirim, açılan listeyi yenilemeye zorlamak için kullanabileceğiniz içeriği çubuk veya Seçimi liste kutuları biriyle değiştirin.

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextManagerEvents>

     Kayıtlı `ShowDropdownBarOption` dil hizmeti kayıt defteri anahtarında, kod penceresi yöneticinize açılan çubuğu görüntülenip görüntülenmeyeceğini ilgili kullanıcı tercihlerini ile eşitlemek için bu olay izlemelidir. Bu seçenek Dil hizmeti anahtarınızı kaydetmeyin sonra açılan çubuğunu gösterme veya gizleme seçeneğini devre dışı **seçenekleri** menüsü.

## <a name="attach-a-drop-down-bar-to-a-code-window"></a>Bir kod penceresine bir açılan çubuğu ekleme
 Oluşturulduğunda bir açılan çubuğu koda eklemek için bir dil hizmeti için açılan iliştirin ne zaman çubuk <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindowManager.AddAdornments%2A> yöntemi çağrılır. Bir çağrı, <xref:Microsoft.VisualStudio.TextManager.Interop.IVsDropdownBarManager.GetDropdownBar%2A> yöntemi gösteren bir açılan çubuğu zaten mevcut çağırma ve emin <xref:Microsoft.VisualStudio.TextManager.Interop.IVsDropdownBarManager.AddDropdownBar%2A>. Erişim için <xref:Microsoft.VisualStudio.TextManager.Interop.IVsDropdownBarManager> arabirim, çağrı <xref:System.Runtime.InteropServices.Marshal.QueryInterface%2A> gelen <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow> işaretçi döndürdü, ne zaman, <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindowManager> uygulama bağlı.

## <a name="see-also"></a>Ayrıca bkz.
- [Eski API'sini kullanarak kod windows özelleştirme](../extensibility/customizing-code-windows-by-using-the-legacy-api.md)
- [Eski dil hizmetinde gezinti çubuğu desteği](../extensibility/internals/support-for-the-navigation-bar-in-a-legacy-language-service.md)