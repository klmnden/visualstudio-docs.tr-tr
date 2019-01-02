---
title: Yayın Sayfası, Proje Tasarımcısı
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- Microsoft.VisualStudio.Publish.ClickOnceProvider.Dialog.PropertyPage
helpviewer_keywords:
- Project Designer, Publish page
- Publish page in Project Designer
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9d8ff0600efbb591e8646c5369aa255e7ce153b3
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53911422"
---
# <a name="publish-page-project-designer"></a>Yayın Sayfası, Proje Tasarımcısı
**Yayımla** sayfasının **Proje Tasarımcısı** ClickOnce dağıtım özelliklerini yapılandırmak için kullanılır.

 Erişim için **Yayımla** sayfasında, içinde bir proje düğümü seçin **Çözüm Gezgini**ve ardından **proje** menüsünde tıklayın **özellikleri**. Zaman **Proje Tasarımcısı** görünen tıklayın **Yayımla** sekmesi.

> [!NOTE]
> Burada açıklanan ClickOnce özelliklerden bazıları da ayarlanabilir **PublishWizard**erişilebilir **derleme** menüsü veya tıklayarak **PublishWizard** bu düğmesi Sayfa.


## <a name="uielement-list"></a>UIElement Listesi
 **Yayımlama klasörü konumu**

 Burada uygulama yayınlandıktan konumu belirtir. Bir sürücü yolu (`C:\deploy\myapplication`), bir dosya paylaşımı (`\\server\myapplication`), veya bir FTP sunucusuna (`ftp://ftp.microsoft.com/myapplication`). Metin mevcut olması gerektiğini unutmayın **yayımlama konumu** Gözat sırayla kutusuna (**...** ) çalışmaya düğmesi.

 **Yükleme klasörü URL'si**

 İsteğe bağlı. Kullanıcıların uygulamayı yüklemek için Git bir Web sitesi belirtir. Bu yalnızca, bu farklıdır gereklidir **yayımlama konumu**, örneğin, ne zaman uygulama yayımlandığında bir hazırlık sunucusu için.

 **Yükleme modu ve ayarları**

 Uygulamayı doğrudan çalıştırılıp çalıştırılmadığını belirleyen **yayımlama konumu** (zaman **uygulama yalnızca çevrimiçi kullanılabilir** seçilir) veya yüklü ve eklenen **Başlat**  menü ve **Program Ekle veya Kaldır** öğesi **Denetim Masası** (zaman **uygulamayı çevrimdışı olarak da kullanılabilir** seçili).

 WPF web tarayıcı uygulamaları, **uygulamayı çevrimdışı olarak da kullanılabilir** seçeneği devre dışıdır, çünkü bu tür uygulamalar yalnızca çevrimiçi kullanılabilir.

 **Uygulama dosyaları**

 Tek tek dosyaların nasıl ve nerede yüklü belirtmek için kullanılan uygulama dosyalarını iletişim kutusu açılır.

 **Önkoşullar**

 Uygulama ile birlikte yüklenmesi için .NET Framework gibi önkoşul bileşenleri belirtmek için kullanılan Önkoşullar iletişim kutusu açılır.

 **Güncelleştirmeler**

 Uygulama için güncelleştirme davranışını belirtmek için kullanılan uygulama güncelleştirmeleri iletişim kutusu açılır. Kullanılabilir olduğunda **uygulama yalnızca çevrimiçi kullanılabilir** seçilir.

 **Seçenekler**

 Ek Gelişmiş yayımlama seçeneklerini belirtmek için kullanılan Yayımlama Seçenekleri iletişim kutusu açılır.

 **Yayım sürümü**

 Uygulama için yayımlama sürüm numarasını ayarlar; sürüm numarası değiştirildiğinde, uygulama bir güncelleştirme olarak yayımlanır. Yayınlama sürümünü her parçası (**ana**, **küçük**, **derleme**, **düzeltme**) 65355 maksimum değeri olabilir (<xref:System.UInt16.MaxValue>), tarafından izin verilen maksimum <xref:System.Version>.

 ClickOnce kullanarak bir uygulamanın birden fazla sürüm yüklediğinizde, yükleme uygulamanın önceki sürümlerini belirttiğiniz yayımlama konum arşivinde adlı bir klasöre taşır. Yükleme dizini temizler önceki sürümünden önceki sürümleri bu şekilde korur arşivleme.

 **Her yayımlamada otomatik artış**

 İsteğe bağlı. Bu seçenek seçildiğinde (varsayılan), **düzeltme** Yayımla sürüm numarasının bölümü bir artırılır uygulamayı yayınladınız her zaman. Bu, bir güncelleştirme olarak yayımlanacak uygulama neden olur.

 **Yayımlama Sihirbazı**

 Açılır Yayımlama Sihirbazı. Yayımlama Sihirbazı Tamamlanıyor çalışan aynı etkiye sahip **Yayımla** komutunu **derleme** menüsü.

 **Şimdi Yayımla**

 Geçerli ayarları kullanarak uygulamanın yayınlar. Eşdeğer **son** düğmesine **PublishWizard**.

## <a name="see-also"></a>Ayrıca Bkz.

- [ClickOnce Uygulamalarını Yayımlama](../../deployment/publishing-clickonce-applications.md)
- [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)
- [Nasıl yapılır: Visual Studio'nun dosyaları nereye kopyalayacağını belirtme](../../deployment/how-to-specify-where-visual-studio-copies-the-files.md)
- [Nasıl yapılır: Burada son kullanıcıların yükleme yapacakları konumu belirtme](../../deployment/how-to-specify-the-location-where-end-users-will-install-from.md)
- [Nasıl yapılır: Teknik destek için bir bağlantı belirtme](../../deployment/how-to-specify-a-link-for-technical-support.md)
- [Nasıl yapılır: ClickOnce çevrimdışı belirtin veya çevrimiçi yükleme modunu](../../deployment/how-to-specify-the-clickonce-offline-or-online-install-mode.md)
- [Nasıl yapılır: CD yüklemeleri için AutoStart'ı etkinleştir](../../deployment/how-to-enable-autostart-for-cd-installations.md)
- [Nasıl yapılır: Kümesi ClickOnce yayım sürümü](../../deployment/how-to-set-the-clickonce-publish-version.md)
- [Nasıl yapılır: Otomatik olarak artırma ClickOnce yayım sürümü](../../deployment/how-to-automatically-increment-the-clickonce-publish-version.md)
- [Nasıl yapılır: ClickOnce tarafından hangi dosyaların yayımlandığını belirtme](../../deployment/how-to-specify-which-files-are-published-by-clickonce.md)
- [Nasıl yapılır: ClickOnce uygulamasıyla Önkoşulları Yükleme](../../deployment/how-to-install-prerequisites-with-a-clickonce-application.md)
- [Nasıl yapılır: ClickOnce uygulaması için güncelleştirmeleri yönetme](../../deployment/how-to-manage-updates-for-a-clickonce-application.md)
- [Nasıl yapılır: Değişiklik ClickOnce uygulaması için yayımlama dilini](../../deployment/how-to-change-the-publish-language-for-a-clickonce-application.md)
- [Nasıl yapılır: ClickOnce uygulaması için Başlat menüsü adı belirtme](../../deployment/how-to-specify-a-start-menu-name-for-a-clickonce-application.md)
- [Nasıl yapılır: ClickOnce uygulaması için bir yayımlama sayfası belirtme](../../deployment/how-to-specify-a-publish-page-for-a-clickonce-application.md)
- [ClickOnce Güvenliği ve Dağıtımı](../../deployment/clickonce-security-and-deployment.md)
