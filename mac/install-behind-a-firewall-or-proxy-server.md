---
title: Yükleme ve bir güvenlik duvarı veya proxy sunucusunun arkasına Mac için Visual Studio'yu kullanın
description: Bu belge, Visual Studio için kurumsal bir ortamda çalışmak Mac (ve kendi iş yükleri de dahil olmak üzere Xamarin) izin vermek için güvenlik duvarınızdan izin verilmelidir konaklar listesini sağlar.
ms.topic: troubleshooting
ms.assetid: 79C0F1A3-0C13-4E55-A820-1138A4082B77
author: asb3993
ms.author: amburns
ms.date: 10/23/2018
ms.openlocfilehash: 6f3afd51cf4109f07107e60d61565c9126fc5ee7
ms.sourcegitcommit: 91c7f1b525e0c22d938bc4080ba4ceac2483474f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67032790"
---
# <a name="install-and-use-visual-studio-for-mac-behind-a-firewall-or-proxy-server"></a>Yükleme ve bir güvenlik duvarı veya proxy sunucusunun arkasına Mac için Visual Studio'yu kullanın

Sizin veya kuruluşunuzun bir güvenlik duvarı veya Ara sunucu gibi güvenlik önlemleri kullanır, sonra vardır, bir "izin verilenler listesine" eklemek isteyebilirsiniz ve bağlantı noktaları ve protokoller, etki alanları Vis yüklediğinizde ve en iyi deneyimi sahip açmak isteyebilirsiniz ual Studio Mac ve Azure Hizmetleri için.


- [**Mac için Visual Studio yükleme**](#install-visual-studio-for-mac): Bu tabloları böylece tüm özellikleri ve Visual Studio'nun iş yükleri için Mac erişiminiz bağlanmaya izin vermelidir etki alanlarını dahil et

- [**Mac için Visual Studio'yu kullanın**](#use-visual-studio-for-mac): Bu tablolar bağlanmaya izin vermelidir ve böylece ilgili özelliklerine sahip etki alanları içerir.

## <a name="install-visual-studio-for-mac"></a>Mac için Visual Studio'yu yükleyin

Mac için Visual Studio çeşitli alanlarından indirdiği için ve sunucuları karşıdan yüklemek için etki alanları ve yapılandırmalarınızı içinde güvenilir olarak eklemek istediğiniz URL'leri aşağıda verilmiştir.

### <a name="microsoft-domains"></a>Microsoft etki alanları

| Etki Alanı| Amaç |
| ----------------------------------- |---------------------------|
| *.live.com| Kimlik bilgileri yönetimi |
| app.vssps.visualstudio.com| Yükleyici meta verileri|
| vortex.data.microsoft.com | Kilitlenme ve hata raporlama |
| az667904.vo.msecnd.net| Kilitlenme ve hata raporlama |
| xamarin.com | Yükleyici meta verileri|
| xampubdl.blob.core.windows.net| Yükleyici paketleri|
| download.VisualStudio.microsoft.com | Yükleyici paketleri|
| xamarin.azureedge.net | Yükleyici paketleri|
| developer.xamarin.com | Yükleyici paketleri|
| static.xamarin.com | Yükleyici paketleri|
| DL.xamarin.com | Yükleyici paketleri|
| dc.services.visualstudio.com| Kilitlenme raporlaması |

### <a name="third-party-domains"></a>Üçüncü taraf etki alanları

| Etki Alanı| Amaç |
| --------------------------|-------------------------|
| DL.Google.com | Android SDK |
| download.Oracle.com | Java SDK|
| api.apple-cloudkit.com| Apple güvenlik hizmetleri |

## <a name="use-visual-studio-for-mac"></a>Mac için Visual Studio'yu kullanın

Visual Studio'da Mac için bir proxy veya güvenlik duvarı ihtiyacınız olan her özelliğe sahip olduğunuzdan emin olmak için aşağıdaki etki alanlarını ve bağlantı noktalarını izin verilen erişim listesine eklemenizi öneririz.

### <a name="general"></a>Genel

| Etki Alanı | Bağlantı noktaları|Amaç|
| ----------------------|------------------|------------------|
| go.microsoft.com | 80/443|Microsoft URL çözümleme |
| vsstartpage.blob.core.windows.net| 80/443| Başlangıç sayfası|
| software.xamarin.com |  80/443|Updater hizmeti|
| addins.monodevelop.com | 80/443| Uzantısı Hizmetleri |
| visualstudio-devdiv-c2s.msedge.net | 80/443| Deneysel özellik ve bildirimleri |
| targetednotifications.azurewebsites.NET|  80/443| Bildirimleri yalnızca belirli türlerini makineleri/kullanım senaryoları için uygun bir liste için genel bir listesini filtrelemek için kullanılan|

### <a name="identity"></a>Kimlik

| Etki Alanı | Bağlantı noktaları|Amaç|
| ----------------------|------------------|------------------|
| login.microsoftonline.com | 80/443| Kimlik sağlayıcısı|
| secure.aadcdn.microsoftonline-p.com | 80/443|Kimlik sağlayıcısı|
| dc.services.visualstudio.com| 80/443|Kilitlenme raporlaması|
| Management.Azure.com|80/443| Azure Hizmetleri API'si |

### <a name="nuget"></a>NuGet

| Etki Alanı | Bağlantı noktaları|Amaç|
| ----------------------|------------------|------------------|
| api.nuget.org | 80/443|NuGet API'si|
| secure.aadcdn.microsoftonline-p.com |80/443| Kimlik sağlayıcısı|

### <a name="android-projects"></a>Android projeleri

| Etki Alanı| Amaç|
| ------------------------------------|------------------------------------|
| time.android.com| Android öykünücüsü saat sunucusu |
| connectivitycheck.gstatic.com | Android öykünücüsü için bağlantı|
| cloudconfig.googleapis.com| Android öykünücüsü API'leri|

## <a name="see-also"></a>Ayrıca bkz.

- [Yükleme ve bir güvenlik duvarı veya proxy sunucusunun arkasına Visual Studio ve Azure hizmetlerini kullanma](/visualstudio/install/install-and-use-visual-studio-behind-a-firewall-or-proxy-server)
- [Windows üzerinde benzer sorunlarını giderme](/visualstudio/install/troubleshooting-network-related-errors-in-visual-studio)
