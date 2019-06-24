---
title: Eski API'yi kullanarak metin arabelleğini erişme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - text buffers
ms.assetid: cd6cf4ae-fff5-4e23-b293-7cbafdb8aed2
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 661bf39e82fef5c040861bc9386dcb7f897d25cb
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66313624"
---
# <a name="access-the-text-buffer-by-using-the-legacy-api"></a>Erişim eski API'yi kullanarak metin arabelleği
Metin, metin akışları ve dosya kalıcılığına yönetmekten sorumludur. Arabellek okuma veya yazma diğer biçimlere rağmen arabellek ile tüm sıradan iletişim Unicode kullanılarak gerçekleştirilir. Eski API'leri, metin arabelleğini bir - veya iki boyutlu bir koordinat sistemini arabellekteki karakterin konumlarını belirlemek için kullanabilirsiniz.

## <a name="one--and-two-dimension-coordinate-systems"></a>Tek ve iki boyutu koordinat sistemleri
 Tek boyutlu bir koordinat konumu ilk karakter bir karakterin konumu arabellekteki 147 gibi temel alır. Kullandığınız <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextStream> tek boyutlu bir arabellek konuma erişmek için arabirim. İki boyutlu bir koordinat sistemini satır ve dizin çiftlerine dayanarak temel alır. Örneğin, bir karakter 43 arabellekte 5 satırında 43, o satırdaki ilk karakterin sağındaki beş karakter olabilir. Arabellek kullanarak iki boyutlu bir konuma erişim <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines> arabirimi. Hem <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines> ve <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextStream> arabirimleri metin arabelleği nesne tarafından uygulanan (<xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer>) ve birbirinden kullanarak erişilebilir `QueryInterface`. Aşağıdaki diyagramda bu ve diğer temel arabirimleri gösteren <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer>.

 ![Metin arabelleği nesnesi](../extensibility/media/vstextbuffer.gif "vsTextBuffer") metin arabelleği nesnesi

 Metin arabelleğinde ya da koordinat sistemini çalışır, ancak iki boyutlu koordinatlarını kullanmak için optimize edilmiştir. Tek boyutlu bir koordinat sistemi performans yükü oluşturabilirsiniz. Bu nedenle, mümkün olduğunda iki boyutlu koordinat sistemini kullanın.

 Arabellek ikinci sorumluluk dosya kalıcılığına metindir. Bunu yapmak için metin arabelleği nesnesi uygulayan <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData2> ve proje öğeleri için belge veri nesnesi bileşeni ve kalıcı ilgili diğer ortam bileşenleri olarak görev yapar. Daha fazla bilgi için [açma ve kaydetme proje öğeleri](../extensibility/internals/opening-and-saving-project-items.md).

## <a name="in-this-section"></a>Bu bölümde
- [Eski API'yi kullanarak görünüm ayarlarını değiştirme](../extensibility/changing-view-settings-by-using-the-legacy-api.md) eski API'yi kullanarak görünüm ayarlarını değiştirme açıklanmaktadır.

- [Genel ayarlar izlemek için metin Yöneticisi'ni kullanın](../extensibility/using-the-text-manager-to-monitor-global-settings.md) genel ayarları izlemek için metin Yöneticisi'ni kullanmayı açıklar.

## <a name="see-also"></a>Ayrıca bkz.
- [Çekirdek Düzenleyicisi içinde](../extensibility/inside-the-core-editor.md)