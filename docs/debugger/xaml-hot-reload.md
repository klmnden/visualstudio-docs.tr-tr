---
title: XAML 'yi dinamik yeniden yükleme kullanarak yazma ve hata ayıklama
description: XAML çalışırken yeniden yükleme veya XAML düzenleme ve devam etme, uygulamaları çalıştırırken XAML kodunuzda değişiklik yapmanıza olanak sağlar
ms.date: 08/05/2019
ms.topic: conceptual
helpviewer_keywords:
- xaml edit and continue
- xaml hot reload
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0acacac883153990861385c96eeb3379c464f97f
ms.sourcegitcommit: 2da366ba9ad124366f6502927ecc720985fc2f9e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68870997"
---
# <a name="write-and-debug-running-xaml-code-with-xaml-hot-reload-in-visual-studio"></a>Visual Studio 'da XAML etkin yeniden yüklemesine sahip XAML kodunu yazma ve hata ayıklama

XAML çalışırken yeniden yükleme, uygulamanızın çalışırken XAML kodunda değişiklik yapmanıza izin vererek WPF veya UWP uygulama kullanıcı arabirimi (UI) oluşturmanıza yardımcı olur. Dinamik yeniden yükleme, hem Visual Studio hem de Visual Studio için Blend kullanılabilir. Bu özellik, çalışan uygulamanın veri bağlamının, kimlik doğrulama durumunun ve tasarım zamanı sırasında benzetim yapmak zor olan diğer gerçek hayklığın avantajıyla XAML kodunu artımlı olarak derleyip test etmenizi sağlar.

XAML dinamik yeniden yükleme, özellikle bu senaryolarda yararlı olur:

* Uygulama hata ayıklama modunda başlatıldıktan sonra XAML kodunuzda bulunan Kullanıcı arabirimi sorunlarını düzeltme.

* Uygulamanın çalışma zamanı bağlamından yararlanarak geliştirme aşamasındaki bir uygulama için yeni bir kullanıcı arabirimi bileşeni oluşturma.

|Desteklenen uygulama türleri|İşletim sistemi ve araçlar|
|-|-|-|
|Windows Presentation Foundation (WPF) |.NET Framework 4.6 +</br>Windows 7 ve üzeri |
|Evrensel Windows uygulamaları (UWP)|Windows 10 ve üzeri, [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk) 14393 + |

> [!NOTE]
> Visual Studio XAML etkin yeniden yüklemesi şu anda yalnızca Visual Studio 'da uygulamanızı çalıştırırken veya hata ayıklayıcı ekli olarak Visual Studio için Blend desteklenir (**F5** veya **hata ayıklamayı Başlat**). Bu deneyimi, [Işleme İliştir](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md)' i kullanarak etkinleştiremezsiniz.

## <a name="known-limitations"></a>Bilinen sınırlamalar

XAML sık yeniden yükleme 'nin bilinen kısıtlamaları aşağıda verilmiştir. ' De çalıştırdığınız herhangi bir sınırlamaya geçici bir çözüm bulmak için, hata ayıklayıcıyı durdurmanız ve sonra işlemi doldurmanız yeterlidir.

|Sınırlama|WPF|UWP|Notlar|
|-|-|-|-|
|Uygulama çalışırken denetimlere yönelik bağlantı olayları|Desteklenmez|Desteklenmez|Bkz: hata: *Olayın başarısız olduğundan emin olun*|
|Uygulamanızın sayfa/pencere veya *app. xaml* gibi bir kaynak sözlüğünde kaynak nesneleri oluşturma|Desteklenmez|Desteklenir|Örnek: `SolidColorBrush` `StaticResource`olarak kullanmak için bir kaynak sözlüğüne ekleme.</br>Not: Statik kaynaklar, stil dönüştürücüler ve bir kaynak sözlüğüne yazılan diğer öğeler, XAML etkin yeniden yükleme kullanılırken uygulanabilir/kullanılabilir. Yalnızca kaynağın oluşturulması desteklenmez.</br> Kaynak sözlüğü `Source` Özelliği değiştiriliyor.|
|Uygulama çalışırken projenize yeni denetimler, sınıflar, pencereler veya diğer dosyalar ekleme|Desteklenmez|Desteklenmez|Yok.|
|NuGet paketlerini yönetme (paket ekleme/kaldırma/güncelleştirme)|Desteklenmez|Desteklenmez|Yok.|
|{X:Bind} biçimlendirme uzantısını kullanan veri bağlamasını değiştirme|Yok|Visual Studio 2019 ve sonraki sürümlerde desteklenir|Visual Studio 2017 veya önceki sürümlerde desteklenmez|

## <a name="error-messages"></a>Hata iletileri

XAML sık yükleme 'yi kullanırken aşağıdaki hatalarda gelebiliriz.

|Hata iletisi|Açıklama|
|-|-|
|Olayın başarısız olduğundan emin olun|Hata, sizin uygulamanız çalışırken desteklenmeyen denetimlerinizin birine bir olay gönderilmeye çalıştığınız anlamına gelir.|
|XAML Düzenle ve devam et güncelleştirilecek herhangi bir öğe bulamadı.|Etkin yeniden yükleme işleminin uygulamanızda güncelleştiremediğinde XAML 'yi düzenlediğinizde hata oluşur.</br> Bu hata, bazen XAML 'nin kullanıldığı bir görünüme gitmek için çalışan uygulamanız kullanılarak düzeltilebilir.</br> Bazen bu hata, hata ayıklama oturumunu yeniden başlatana kadar belirli bir değişikliğin uygulanmadığı anlamına gelir. |
|Bu değişiklik, hata ayıklama oturumu sırasında desteklenmez.|Hata, denediğiniz değişikliğin XAML etkin yeniden yükleme tarafından desteklenmediğini gösterir. Hata ayıklama oturumunu durdurun, değişikliği yapın ve hata ayıklama oturumunu yeniden başlatın.|
