---
title: Eski API'sini kullanarak kod Windows özelleştirme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - code windows
ms.assetid: 5328ab2f-55cb-4680-9744-ec79f55acd1b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c0ea617a252d60d8e8d5810c42f7331508c28165
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56708985"
---
# <a name="customize-code-windows-by-using-the-legacy-api"></a>Eski API'sini kullanarak kod windows özelleştirme
Bir kod penceresinde bir veya daha fazla metin görünümlerini destekleyen bir belge penceresi nesnesidir. Tam bir kod penceresi özelliklerini ilişkili dil hizmetine bağlıdır. Çok Belgeli Arabirim (MDI) modunda kod penceresinde MDI alt çerçeve ' dir.

 Kodu windows dil Hizmetleri tarafından denetlenir ve her dil hizmeti, kendi kod penceresinde yöneticisini sağlayabilir. Bu, kod penceresi dalgalı çizgiler, renklendirme ve daha fazlası gibi kendi kenarlıklar eklemek dil hizmeti sağlar. Core pencereyi oluşturma hakkında daha fazla bilgi için bkz. [eski API'yi kullanarak çekirdek Düzenleyici örneği](../extensibility/instantiating-the-core-editor-by-using-the-legacy-api.md).

 Bir kod penceresi bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame> metni görünümü ve nesne tarihli herhangi Kenarlıklar nesnesi. Düzenleyici, çekirdek Örnekleme sırasında kod penceresinde oluşturduğunuzda, dil hizmetinizi ekleyebilirsiniz bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindowManager> kod penceresine olarak aşağıdaki çizimde gösterilmiştir.

 ![CodeWindow grafiği](../extensibility/media/vscodewindow.gif "vscodewindow") kod penceresi

 Dil hizmeti, kod penceresi Yöneticisi uygular ve açılan çubuğu gibi Kenarlıklar yönetmekten sorumludur. Kod penceresi çağrıları <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindowManager.AddAdornments%2A> kod penceresinde başlatma sırasında yöntemi. Bu çağrı yapıldığında, dil hizmeti açılan çubuğu veya düğme çubuğu ekleyebilirsiniz (<xref:Microsoft.VisualStudio.TextManager.Interop.IVsButtonBarClient>) için kod penceresi.

## <a name="in-this-section"></a>Bu bölümde
 `Customizing Code Windows by Using the Legacy API` Kodu windows eski API'yi kullanarak özelleştirmek nasıl açıklar.

- [Nasıl yapılır: Başka bir düzenleyicide bir düzenleyicide konak](../extensibility/how-to-host-an-editor-in-another-editor.md) bir düzenleyici penceresi içine ikinci bir düzenleyici barındırmak nasıl açıklar.

- [Nasıl yapılır: Düzenleyici odağı kaybettiğinde olayları yangın](../extensibility/how-to-fire-events-when-the-editor-loses-focus.md) belge veri nesnesine bir belge görünümü ekleme açıklanmaktadır.

## <a name="see-also"></a>Ayrıca bkz.
- <xref:Microsoft.VisualStudio.TextManager.Interop.VsCodeWindow>
- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView>
- <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer>
- <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView>
- [Eski API'yi kullanarak çekirdek Düzenleyici örneği](../extensibility/instantiating-the-core-editor-by-using-the-legacy-api.md)
- [Eski API'yi kullanarak erişim erişimcisinde görünümü](../extensibility/accessing-thetext-view-by-using-the-legacy-api.md)