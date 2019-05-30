---
title: Eski API'yi kullanarak çekirdek Düzenleyici örnekleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - instantiating editor
ms.assetid: dda23b18-96ef-43c6-b0dc-06d15cbe5cbb
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 06aabce486d128682ee249163db0c2339a7207f5
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66309139"
---
# <a name="instantiate-the-core-editor-by-using-the-legacy-api"></a>Eski API'yi kullanarak çekirdek Düzenleyici örneği

Düzenleyici metin düzenleme ekleme, silme, kopyalama ve yapıştırma gibi işlevleri sorumludur. Bu, bu işlevler, metin renklendirme, girinti ve IntelliSense deyim tamamlama gibi dil Hizmetleri tarafından sağlanan işlevleri ile birleştirir.

Üç yoldan biriyle çekirdek Düzenleyici örneği örneği oluşturabilir:

- Açıkça çekirdek örneği bir pencerede Düzenleyicisi oluşturun.

- Çekirdek Düzenleyici örneği döndüren bir düzenleyici fabrikası sağlayın

- Proje hiyerarşisindeki dosyasını açın.

Aşağıdaki bölümlerde, eski API'SİNİN Düzenleyici örneği oluşturmak için nasıl kullanılacağı açıklanmaktadır.

## <a name="explicitly-open-a-core-editor-instance"></a>Açıkça bir çekirdek Düzenleyici örneği açın.

Çekirdek Düzenleyici örneği açıkça alınırken:

- Elde bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer> düzenlenmekte olan belge veri nesnesini tutacak.

- Bir satır yönelimli gösterimini belge veri nesnesi oluşturma bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines> alanından arabirim <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer> arabirimi.

- Ayarlama <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines> varsayılan uygulaması örneği için belge veri nesnesi olarak <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow> arabirimi kullanılarak <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow.SetBuffer%2A> yöntemi.

   Konak <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow> örneğini bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame> kullanarak arabirimi <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.CreateToolWindow%2A> yöntemi.

Bu noktada, görüntüleme <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame> arabirimi çekirdek Düzenleyici örneği içeren bir pencere sağlar.

Olmamasından kısayol tuşları olması veya gelişmiş özelliklere erişim ancak, bu çok yararlı bir örneği değil. Kısayol tuşları ve gelişmiş özelliklere erişim elde etmek için:

- Kullanım <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer.SetLanguageServiceID%2A> dil hizmeti ve düzenleyici kullanan belge veri nesnesi ilişkilendirmek için yöntemi.

- Kendi kısayol tuşları oluşturabilir veya ayarlayarak Sistem varsayılanı kullanın <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame> nesnelerin özelliklerini görüntüleme. Bunu yapmak için <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.SetGuidProperty%2A> yöntemiyle [__VSFPROPID. VSFPROPID_InheritKeyBindings](<xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID.VSFPROPID_InheritKeyBindings>) özelliği.

   Edinmek ve standart kısayol tuşlarını kullanmak için onları oluşturmak kullanarak *.vsct* dosya. Daha fazla bilgi için [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md).

## <a name="how-to-use-an-editor-factory-to-obtain-the-core-editor"></a>Çekirdek Düzenleyici almak için bir düzenleyici fabrikası kullanma

Bir düzenleyici fabrikası kullanarak bir çekirdek Düzenleyici uygularken <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> yöntemi açıkça barındırmak için önceki bölümde açıklanan tüm adımları izleyin. bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow> kullanarak bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer> belge veri nesnesi bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame> nesne.

Metni görüntülemek için elde bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView> alanından arabirim <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow> nesne ve çağrı <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> yöntemi.

Düzenleyici için dil hizmeti sağlamak için çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer.SetLanguageServiceID%2A> yöntemi içinde <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> yöntemi.

Varsayılan kısayol tuşları, önceki bölümde aksine elde etmek için tarafından döndürülen komut içeriğini kullanın. <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> çekirdek Düzenleyicisi'nden alınırken yöntemi <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> yöntemi.

Varsa <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> yöntemi, metin düzenleyici olarak aynı komutu GUID döndürür, çekirdek Düzenleyici örneği, otomatik olarak varsayılan kısayol tuşlarını alır.

Genel bilgi için bkz. [izlenecek yol: Çekirdek düzenleyici oluşturma ve bir düzenleyici dosya türü kaydetme](../extensibility/walkthrough-creating-a-core-editor-and-registering-an-editor-file-type.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Çekirdek Düzenleyicisi içinde](../extensibility/inside-the-core-editor.md)
- [Açın ve proje öğeleri Kaydet](../extensibility/internals/opening-and-saving-project-items.md)
- [İzlenecek yol: Bir çekirdek Düzenleyicisi ve bir düzenleyici dosya türü kayıt oluşturma](../extensibility/walkthrough-creating-a-core-editor-and-registering-an-editor-file-type.md)