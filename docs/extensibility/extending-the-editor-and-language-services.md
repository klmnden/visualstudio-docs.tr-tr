---
title: Düzenleyici ve dil hizmetlerini genişletme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], new -
ms.assetid: 8d04f8db-eda7-4b3e-b6eb-c06df104502a
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ec9009f3c331da608c22d38f35a08e157e878771
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66312974"
---
# <a name="extend-the-editor-and-language-services"></a>Düzenleyici ve dil hizmetlerini genişletme
Kendi düzenleyicinizi için dil hizmeti özellikleri (örneğin, IntelliSense) ekleyin ve özelliklerin çoğunu Visual Studio Kod Düzenleyicisi'ni genişletin.  Genişletebilirsiniz tam listesi için bkz. [dil hizmeti ve düzenleyici uzantı noktaları](../extensibility/language-service-and-editor-extension-points.md).

 Çoğu Düzenleyici özellikleri, Yönetilen Genişletilebilirlik Çerçevesi (MEF) kullanarak genişletin. Örneğin, söz dizimi renklendirme, genişletmek istediğiniz Düzenleyici özelliği ise, bir MEF yazabilirsiniz *bileşen parçası* istediğiniz farklı renklendirme ve bunları ele istediğiniz nasıl sınıflandırmalarını tanımlar. Düzenleyici, aynı özellik birden fazla uzantı da destekler.

 Düzenleyici sunu katmanını temel Windows Presentation Framework (WPF). WPF Grafik kitaplığı için esnek metin biçimlendirme sağlar ve ayrıca grafik ve animasyon gibi görsel öğeler sağlar.

 Visual Studio SDK'sı olarak da bilinen bağdaştırıcıları sağlar *dolgular* önceki sürümleri için yazılmış VSPackages desteklemek için. Bununla birlikte, mevcut bir VSPackage varsa, daha iyi performans ve güvenilirlik elde etmek için yeni teknoloji güncelleştirme öneririz.

## <a name="related-topics"></a>İlgili Konular

|Başlık|Açıklama|
|-----------|-----------------|
|[Dil hizmeti ve düzenleyici uzantılarıyla çalışmaya başlama](../extensibility/getting-started-with-language-service-and-editor-extensions.md)|Düzenleyici uzantısı oluşturma açıklanır.|
|[Düzenleyicinin içinde](../extensibility/inside-the-editor.md)|Düzenleyici genel yapısını açıklar ve bazı özellikleri listeler.|
|[Genişletilebilirlik Çerçevesi Düzenleyicisi'nde yönetilen](../extensibility/managed-extensibility-framework-in-the-editor.md)|Yönetilen Genişletilebilirlik Çerçevesi (MEF) düzenleyiciyle kullanmayı açıklar.|
|[Dil hizmeti ve düzenleyici uzantı noktaları](../extensibility/language-service-and-editor-extension-points.md)|Düzenleyici uzantı noktaları listeler. Uzantı noktaları Genişletilebilir Düzenleyici özelliklerini temsil eder.|
|[İzlenecek yol: Görünüm kenarlığı, komutlar ve ayarlar (sütun kılavuzları) oluşturma](../extensibility/walkthrough-creating-a-view-adornment-commands-and-settings-column-guides.md)|Size yol gösterir ve belirli bir ekran genişliği kod sağlamanıza yardımcı olmak için sütun kılavuz çizgileri çizen bir görünüm kenarlığı oluşturma açıklanmaktadır.  Ayrıca, okuma ve yazma ayarları yanı sıra bildirme ve komut penceresinden çağırabilirsiniz komutlar uygulama gösterir.|
|[Düzenleyici içeri aktarımları](../extensibility/editor-imports.md)|Bir uzantı aktarabilirsiniz hizmetler listelenir.|
|[Eski kod düzenleyicisine uyum](../extensibility/adapting-legacy-code-to-the-editor.md)|Eski kod (önceden Visual Studio Düzenleyicisi'ni genişletmek için 2010) uyarlamak için farklı yollar açıklanmaktadır.|
|[Eski dil hizmetini geçirme](../extensibility/internals/migrating-a-legacy-language-service.md)|VSPackage'ı temel dil hizmetini geçirme açıklanmaktadır.|
|[İzlenecek yol: Bağlantı bir dosya adı uzantısı için bir içerik türü](../extensibility/walkthrough-linking-a-content-type-to-a-file-name-extension.md)|Bir içerik türü için bir dosya adı uzantısına bağlama işlemi gösterilmektedir.|
|[İzlenecek yol: Dış boşluk karakteri oluşturma](../extensibility/walkthrough-creating-a-margin-glyph.md)|Simge kenar boşluğuna ekleme işlemi gösterilmektedir.|
|[İzlenecek yol: Metni vurgulama](../extensibility/walkthrough-highlighting-text.md)|Nasıl kullanılacağını gösterir *etiketleri* metni vurgulayın.|
|[İzlenecek yol: Anahat oluşturma Ekle](../extensibility/walkthrough-outlining.md)|Küme ayraçları belirli bir tür için anahat oluşturma ekleme işlemi gösterilmektedir.|
|[İzlenecek yol: Eşleşen küme ayraçlarını görüntüleme](../extensibility/walkthrough-displaying-matching-braces.md)|Eşleşen küme ayraçlarını vurgulamak gösterilmektedir.|
|[İzlenecek yol: Hızlıbilgi araç ipuçlarını görüntüleme](../extensibility/walkthrough-displaying-quickinfo-tooltips.md)|Özellikler, yöntemler ve olaylar gibi kod öğeleri açıklayan Hızlıbilgi açılan pencereler görüntüleme işlemini göstermektedir.|
|[İzlenecek yol: İmza Yardımı görüntüleme](../extensibility/walkthrough-displaying-signature-help.md)|Bir imzada sayısı ve parametre türleri hakkında bilgiler vermemiz açılan pencereler görüntüleme işlemini göstermektedir.|
|[İzlenecek yol: Deyim tamamlama görüntüleme](../extensibility/walkthrough-displaying-statement-completion.md)|Deyim tamamlama uygulanması gösterilmektedir.|
|[İzlenecek yol: Kod parçacıkları uygulama](../extensibility/walkthrough-implementing-code-snippets.md)|Kod parçacığı genişletme uygulanması gösterilmektedir.|
|[İzlenecek yol: Ampul önerilerini görüntüleme](../extensibility/walkthrough-displaying-light-bulb-suggestions.md)|Ampuller kod öneriler için görüntüleme işlemini göstermektedir.|
|[İzlenecek yol: Düzenleyici uzantısı ile Kabuk komutu kullanma](../extensibility/walkthrough-using-a-shell-command-with-an-editor-extension.md)|Bir menü komutu vspackage'ta bir MEF Bileşeni ile ilişkilendirilecek gösterilmektedir.|
|[İzlenecek yol: Düzenleyici uzantısı ile kısayol tuşu kullanma](../extensibility/walkthrough-using-a-shortcut-key-with-an-editor-extension.md)|Bir MEF Bileşeni ile menü kısayolu vspackage'ta ilişkilendirilecek gösterilmektedir.|
|[Managed Extensibility Framework (MEF)](/dotnet/framework/mef/index)|Bilgi hakkında Yönetilen Genişletilebilirlik Çerçevesi (MEF) sağlar.|
|[Windows Presentation Foundation](/dotnet/framework/wpf/index)|Windows Presentation Foundation (WPF) hakkında bilgi sağlar.|

## <a name="reference"></a>Başvuru
 Visual Studio düzenleyicisinde, aşağıdaki ad alanlarını içerir.

 <xref:Microsoft.VisualStudio.Language.Intellisense>

 <xref:Microsoft.VisualStudio.Language.StandardClassification>

 <xref:Microsoft.VisualStudio.Editor>

 <xref:Microsoft.VisualStudio.Text>

 <xref:Microsoft.VisualStudio.Text.Adornments>

 <xref:Microsoft.VisualStudio.Text.Classification>

 <xref:Microsoft.VisualStudio.Text.Differencing>

 <xref:Microsoft.VisualStudio.Text.Document>

 <xref:Microsoft.VisualStudio.Text.Editor>

 <xref:Microsoft.VisualStudio.Text.Editor.OptionsExtensionMethods>

 <xref:Microsoft.VisualStudio.Text.Formatting>

 <xref:Microsoft.VisualStudio.Text.IncrementalSearch>

 <xref:Microsoft.VisualStudio.Text.Operations>

 <xref:Microsoft.VisualStudio.Text.Outlining>

 <xref:Microsoft.VisualStudio.Text.Projection>

 <xref:Microsoft.VisualStudio.Text.Tagging>

 <xref:Microsoft.VisualStudio.Utilities>