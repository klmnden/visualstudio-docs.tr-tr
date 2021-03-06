---
title: Yayın Sayfası, Proje Tasarımcısı
ms.date: 11/04/2016
ms.technology: vs-ide-deployment
ms.topic: reference
f1_keywords:
- Microsoft.VisualStudio.Publish.ClickOnceProvider.Dialog.PropertyPage
helpviewer_keywords:
- Project Designer, Publish page
- Publish page in Project Designer
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6bbb43408dc12c55b72eb0ca0909d8b261198a5b
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926165"
---
# <a name="publish-page-project-designer"></a>Yayın Sayfası, Proje Tasarımcısı

**Proje Tasarımcısı** ' nın **Yayımla** sayfası ClickOnce dağıtımı için özellikleri yapılandırmak üzere kullanılır.

**Yayımla** sayfasına erişmek için **Çözüm Gezgini**' de bir proje düğümü seçin ve ardından **Proje** menüsünde **Özellikler**' e tıklayın. **Proje Tasarımcısı** göründüğünde, **Yayımla** sekmesine tıklayın.

> [!NOTE]
> Burada açıklanan bazı ClickOnce özellikleri, **derleme** menüsünde veya bu sayfadaki **publishwizard** düğmesine tıklanarak bulunan **publishwizard**'da da ayarlanabilir.

## <a name="uielement-list"></a>UIElement Listesi

 **Yayımlama klasörü konumu**

Uygulamanın yayımlandığı konumu belirtir. , Bir sürücü yolu (`C:\deploy\myapplication`), bir dosya paylaşma (`\\server\myapplication`) veya bir FTP sunucusu (`ftp://ftp.microsoft.com/myapplication`) olabilir. Göz at ( **...** ) düğmesinin çalışması Için **Yayımlama konumu** kutusunda metnin mevcut olması gerektiğini unutmayın.

 **Yükleme klasörü URL 'SI**

İsteğe bağlı. Kullanıcıların uygulamayı yüklemek için gideceği Web sitesini belirtir. Bu, yalnızca **yayımlama konumundan**farklı olduğunda (örneğin, uygulama bir hazırlama sunucusuna yayımlandığında) gereklidir.

 **Modu ve ayarları yükler**

Uygulamanın doğrudan **yayımlama konumundan** çalıştırılıp çalıştırılmadığını ( **uygulama yalnızca çevrimiçi kullanılabilir** olduğunda) veya yüklenip buradan **Başlat** menüsüne ve **Program Ekle/Kaldır** öğesine eklendiğini belirler. **Denetim Masası** ( **uygulama çevrimdışı kullanılabilir** olduğunda, ayrıca seçili olduğunda).

WPF Web tarayıcısı uygulamaları için **uygulama çevrimdışı olarak kullanılabilir** , çünkü bu uygulamalar yalnızca çevrimiçi kullanılabilir.

 **Uygulama dosyaları**

Her bir dosyanın nasıl ve nerede yükleneceğini belirlemek için kullanılan uygulama dosyaları iletişim kutusunu açar.

 **Önkoşullar**

Uygulamayla birlikte yüklenecek .NET Framework gibi Önkoşul bileşenlerini belirtmek için kullanılan Önkoşullar iletişim kutusunu açar.

 **Güncelleştirmeler**

Uygulamanın güncelleştirme davranışını belirtmek için kullanılan uygulama güncelleştirmeleri iletişim kutusunu açar. **Uygulama yalnızca çevrimiçi kullanılabilir** olduğunda kullanılamaz.

 **Seçenekler**

Diğer gelişmiş yayımlama seçeneklerini belirtmek için kullanılan Yayımla Seçenekleri iletişim kutusunu açar.

 **Yayımlama sürümü**

Uygulama için yayımlama sürüm numarasını ayarlar; sürüm numarası değiştirildiğinde, uygulama bir güncelleştirme olarak yayımlanır. Yayımla sürümünün (**ana**, **İkincil**, **derleme**, **Düzeltme**) her bölümü, izin verilen en yüksek 65355<xref:System.UInt16.MaxValue> <xref:System.Version>() değerine sahip olabilir.

ClickOnce kullanarak bir uygulamanın birden fazla sürüm yüklediğinizde, yükleme uygulamanın önceki sürümlerini belirttiğiniz yayımlama konum arşivinde adlı bir klasöre taşır. Yükleme dizini temizler önceki sürümünden önceki sürümleri bu şekilde korur arşivleme.

 **Her yayınla birlikte düzeltmeyi otomatik olarak artır**

İsteğe bağlı. Bu seçenek belirlendiğinde (varsayılan), yayımlama sürümü numarasının **Düzeltme** bölümü, uygulamanın her yayımlanışında bir artırılır. Bu, uygulamanın bir güncelleştirme olarak yayımlanmasına neden olur.

 **Yayımlama Sihirbazı**

Yayımla sihirbazını açar. Yayımla sihirbazının tamamlanması, **derleme** menüsündeki **Yayımla** komutunu çalıştırmasıyla aynı etkiye sahiptir.

 **Şimdi Yayımla**

Geçerli ayarları kullanarak uygulamayı yayımlar. **Publishwizard**'daki **son** düğmesine eşittir.

## <a name="see-also"></a>Ayrıca bkz.

- [ClickOnce Uygulamalarını Yayımlama](../../deployment/publishing-clickonce-applications.md)
- [Nasıl yapılır: Yayımlama Sihirbazını Kullanarak ClickOnce Uygulaması Yayımlama](../../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)
- [Nasıl yapılır: Visual Studio'nun Dosyaları Nereye Kopyalayacağını Belirtme](../../deployment/how-to-specify-where-visual-studio-copies-the-files.md)
- [Nasıl yapılır: Son Kullanıcıların Yükleme Yapacakları Konumu Belirtme](../../deployment/how-to-specify-the-location-where-end-users-will-install-from.md)
- [Nasıl yapılır: Teknik Destek için bir Bağlantı Belirtme](../../deployment/how-to-specify-a-link-for-technical-support.md)
- [Nasıl yapılır: ClickOnce Çevrimdışı veya Çevrimiçi Yükleme Modunu Belirtme](../../deployment/how-to-specify-the-clickonce-offline-or-online-install-mode.md)
- [Nasıl yapılır: CD Yüklemeleri için AutoStart'ı Etkinleştirme](../../deployment/how-to-enable-autostart-for-cd-installations.md)
- [Nasıl yapılır: ClickOnce Yayım Sürümünü Ayarlama](../../deployment/how-to-set-the-clickonce-publish-version.md)
- [Nasıl yapılır: ClickOnce Yayım Sürümünü Otomatik Olarak Artırma](../../deployment/how-to-automatically-increment-the-clickonce-publish-version.md)
- [Nasıl yapılır: ClickOnce Tarafından Hangi Dosyaların Yayımlandığını Belirtme](../../deployment/how-to-specify-which-files-are-published-by-clickonce.md)
- [Nasıl yapılır: ClickOnce Uygulamasıyla Önkoşulları Yükleme](../../deployment/how-to-install-prerequisites-with-a-clickonce-application.md)
- [Nasıl yapılır: ClickOnce Uygulaması için Güncelleştirmeleri Yönetme](../../deployment/how-to-manage-updates-for-a-clickonce-application.md)
- [Nasıl yapılır: ClickOnce Uygulaması için Yayımlama Dilini Değiştirme](../../deployment/how-to-change-the-publish-language-for-a-clickonce-application.md)
- [Nasıl yapılır: ClickOnce Uygulaması için Başlat Menüsü Adı Belirtme](../../deployment/how-to-specify-a-start-menu-name-for-a-clickonce-application.md)
- [Nasıl yapılır: ClickOnce Uygulaması için Bir Yayımlama Sayfası Belirtme](../../deployment/how-to-specify-a-publish-page-for-a-clickonce-application.md)
- [ClickOnce Güvenliği ve Dağıtımı](../../deployment/clickonce-security-and-deployment.md)
