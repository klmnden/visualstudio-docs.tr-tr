---
title: Yazma ve sık erişimli yeniden XAML kullanarak XAML hatalarını ayıklama
description: XAML sık erişimli yeniden yükleyin veya XAML Düzenle ve devam et, uygulama çalıştırılırken XAML kodunuzu değişiklik yapmanızı sağlar
ms.custom: ''
ms.date: 02/28/2019
ms.topic: conceptual
helpviewer_keywords:
- xaml edit and continue
- xaml hot reload
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a002c3876eecf0f31a8d104fa235b1208af90699
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62929141"
---
# <a name="write-and-debug-running-xaml-code-with-xaml-hot-reload-in-visual-studio"></a>Yazma ve Visual Studio'da XAML sık erişimli yeniden yükle ile çalışan XAML kodu hatalarını ayıklama

Etkin Visual Studio XAML yeniden uygulamanız çalışırken XAML kodu değişiklik yapmanıza izin vererek, WPF veya UWP uygulaması UI oluşturmanıza yardımcı olur. Bu özellik, artımlı olarak derleyip test etmeye çalışan uygulamanın veri bağlamı, kimlik doğrulama durumu ve tasarım zamanı sırasında simülasyonunu yapmak zordur diğer gerçek karmaşıklığı avantajı ile XAML kodu sağlar.

XAML sık erişimli yeniden bu senaryolarda özellikle yararlıdır:

* Hata ayıklama modunda uygulama başlatıldıktan sonra XAML kodunuzu bulunan kullanıcı Arabirimi sorunlarını giderme.

* Bir uygulama için yeni bir kullanıcı Arabirimi bileşeninin oluşturma yararlanırken, uygulamanızın çalışma zamanı bağlam geliştirme altındadır.

|Desteklenen uygulama türleri|İşletim sistemi ve araçları|
|-|-|-|
|Windows Presentation Foundation (WPF) |.NET framework 4.6 +</br>Windows 7 ve üzeri |
|Evrensel Windows uygulamaları (UWP)|Windows 10 ve üzeri ile [Windows 10 SDK'sı](https://developer.microsoft.com/windows/downloads/windows-10-sdk) 14393 + |

> [!NOTE]
> Visual Studio XAML sık erişimli yeniden yükleme şu anda yalnızca uygulamanızı Visual Studio'da hata ayıklayıcısı ekli çalıştırırken desteklenir (**F5** veya **hata ayıklamayı Başlat**). Bu deneyim kullanarak etkinleştirilemiyor *iliştirme*.

## <a name="known-limitations"></a>Bilinen sınırlamalar

Aşağıdaki XAML sınırlamaları yeniden hot bilinmektedir. Yaşadığınız herhangi bir sınırlama geçici olarak çözmek için yalnızca hata ayıklayıcıyı durdurun ve ardından işlemi tamamlamak.

|Sınırlama|WPF|UWP|Notlar|
|-|-|-|-|
|Uygulama çalışırken olayları denetimlere bağlama|Desteklenmez|Desteklenmez|Hata bakın: *Olay sağlamak başarısız oldu*|
|Bu, uygulamanızın sayfa/penceresinde gibi bir kaynak sözlüğünde kaynağı nesneleri oluşturma veya *App.xaml*|Desteklenmez|Desteklenir|Örnek: ekleme bir ```SolidColorBrush``` olarak kullanmak için bir kaynak sözlüğüne bir ```StaticResource```.</br>Not: Statik kaynaklar, stil dönüştürücüleri ve diğer öğeleri bir kaynak sözlüğüne yazılan XAML sık erişimli yeniden kullanırken uygulanan ve kullanılan olabilir. Yalnızca kaynak oluşturulması desteklenmiyor.</br> Kaynak sözlüğünü değiştirme ```Source``` özelliği.| 
|Uygulama çalışırken, yeni denetimler, sınıflar, windows veya diğer dosyaları projenize ekleme|Desteklenmez|Desteklenmez|Yok.|
|NuGet paketleri (ekleme/kaldırma/güncelleştirme paketleri) yönetme|Desteklenmez|Desteklenmez|Yok.|
|Veri bağlama değiştirme kullanan {x: Bind} işaretleme uzantısı|Yok|Visual Studio 2019 ve sonraki sürümlerinde desteklenir.|Visual Studio 2018 veya önceki sürümlerde desteklenmiyor|

## <a name="error-messages"></a>Hata iletileri

XAML sık erişimli yeniden kullanırken aşağıdaki hatalar arasında gelebilir.

|Hata iletisi|Açıklama|
|-|-|-|
|Olay sağlamak başarısız oldu|Hata, bir olay, uygulama çalışırken, desteklenmiyor, denetimleri birine wire çalıştığınız gösterir.|
|XAML Düzenle ve devam et, güncelleştirilecek öğe bulamadı.|Düzenleme yaparken sık yeniden XAML uygulamanızda güncelleştirilemiyor. hata oluşur.</br> Bu hata, bazen çalışan uygulamanızı görünümüne gitmek için XAML kullanıldığı kullanarak çözülebilir.</br> Bazı durumlarda, bu hata, hata ayıklama oturumunu yeniden başlatana kadar değişikliğinizi uygulanamaz anlamına gelir. |
|Bu değişiklik, hata ayıklama oturumu sırasında desteklenmiyor.|Hata olduğunu gösterir çalıştığınız değişiklik XAML sık erişimli yeniden yükleme tarafından desteklenmiyor. Hata ayıklama oturumunu durdurmak, değişikliği yapın ve ardından hata ayıklama oturumunu yeniden başlatın.|