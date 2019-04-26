---
title: Dotfuscator Özellikleri
ms.date: 03/28/2019
ms.devlang: dotnet
ms.topic: conceptual
keywords: Dotfuscator, Dotfuscator Community, Dotfuscator CE, PreEmptive, PreEmptive Solutions, PreEmptive koruma, koruma, community edition, gizleme, .NET, ücretsiz, Visual Studio 2017, Visual Studio 2019, Visual Studio
helpviewer_keywords:
- PreEmptive Protection Dotfuscator
- Dotfuscator Community Edition
- Dotfuscator Community
- Dotfuscator CE
- Dotfuscator
- obfuscation
- protection
description: Visual Studio'daki Dotfuscator Community ücretsiz bir kopyasını yeteneklerini öğrenin.
ms.assetid: 0ee89c58-c900-48fc-a6a2-65ace00e8bab
author: Joe-Sewell-PreEmptive
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 5bf42ec3c706282adf2752d21c0c121f89c2ed5f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62557261"
---
# <a name="capabilities-of-dotfuscator"></a>Dotfuscator Özellikleri

Bu sayfa, Dotfuscator Community yeteneklerini Gelişmiş seçenekleri aracılığıyla kullanılabilen bazı başvurular odaklanır [yükseltmeleri][upgrades].

Dotfuscator Community olduğu bir *derleme sonrası* sistem .NET uygulamaları için.
Bununla, Visual Studio kullanıcılarına bağlanabildiğinizden emin [derlemeleri karartmak] [ obfuscation] ve ekleme [active koruma önlemleri] [ checks] uygulamaya - tüm Dotfuscator özgün kaynak koduna erişim gerek.
Dotfuscator katmanlı koruma stratejisi oluşturma uygulamanızı birden çok yolla korur.

Dotfuscator Community gibi bir geniş .NET derlemesi ve uygulama türlerini destekler, [Evrensel Windows Platformu (UWP)] [ uwp] ve [Xamarin] [ xamarin].

## <a name="intellectual-property-protection"></a>Fikri mülkiyet koruması

Uygulama tasarımı, davranış ve uygulama fikri mülkiyet (IP) biçimler.
Ancak, .NET Framework için oluşturulan uygulamaların temelde books açın değildir; Ters mühendislik .NET derlemeleri için çok kolaydır [üst düzey meta veriler ve Ara kod içerdiğinden][assemblies].

Dotfuscator Community içeren temel [.NET karartma] [ obfuscation] biçiminde [yeniden adlandırma][renaming].
Bu adlandırma önemli bilgiler genel olarak Dotfuscator kodunuzla obfuscating tersine mühendislik, kaynak kodda için yetkisiz erişim riskini azaltır.
Gizleme çaba sarf, kod incelemesi - IP, ticari sır olarak yasal korunduğunu oluşturma önemli bir adım korumak için de gösterir.

Çoğu [uygulama bütünlüğünü koruma özellikleri](#application-integrity-protection) tersine mühendislik Dotfuscator Community daha fazla süreçlerden kaçınmıştır.
Örneğin, kötü bir aktör uygulamasının program mantığını anlamak için çalışan bir örneği için bir hata ayıklayıcının girişiminde bulunabilir.
Dotfuscator ekleme [koruma hata ayıklama davranışı][debug] uygulamanıza bu obstruct.

## <a name="application-integrity-protection"></a>Uygulama bütünlüğünü koruma

Kaynak kodunuzu korunmasına ek olarak, uygulamanızı tasarlandığı gibi kullanıldığından emin olmak önemli.
Saldırganlar, uygulamanızın lisanslama ilkeleri (yani, yazılım korsanlığı), çalabilir veya uygulama tarafından işlenen hassas verileri işlemek için ya da uygulamanın davranışını değiştirmek için aşmak için çalma girişiminde bulunabilir.

Dotfuscator Community ekleme [uygulama doğrulama kodu] [ checks] içine dahil olmak üzere derlemelerinizin [koruma kurcalamaya][tamper], [koruma hata ayıklama][debug], ve [hologram cihaza] [ root] ölçümleri.
Geçersiz uygulama durumu algılandığında bir doğrulama kodu için [çağrı durumunuza uygun bir şekilde ele almak için uygulama kodunun üzerine][check-app].
Veya kodu yazamazlar tercih ederseniz Geçersiz tanıtıcı kullanan uygulama, Dotfuscator de ekleme [yanıt][check-action] , kaynak kodunuzda değişiklik gerektirmeden davranışları.

Bu aynı yöntemlerin çoğu zorlamak için de kullanılabilir [yaşam son teslim tarihlerine][shelflife] yazılım değerlendirme veya deneme sürümü için.

## <a name="see-also"></a>Ayrıca Bkz.

[Bu konudaki tam Dotfuscator Community Kullanıcı Kılavuzu][full]

<!-- Copyright © 2019 PreEmptive Solutions, LLC -->

[assemblies]:  https://docs.microsoft.com/dotnet/standard/assembly-format
[uwp]:  https://www.preemptive.com/blog/article/856-uwp-applications-in-dotfuscator-ce/91-dotfuscator-ce
[xamarin]:  https://www.preemptive.com/obfuscating-xamarin-with-dotfuscator

[upgrades]:  upgrades.md

[obfuscation]:  https://www.preemptive.com/dotfuscator/ce/docs/help/obfuscation_overview.html
[renaming]:  https://www.preemptive.com/dotfuscator/ce/docs/help/obfuscation_renaming.html

[checks]:  https://www.preemptive.com/dotfuscator/ce/docs/help/checks_overview.html
[check-app]:  https://www.preemptive.com/dotfuscator/ce/docs/help/checks_overview.html#app-notification
[check-action]:  https://www.preemptive.com/dotfuscator/ce/docs/help/checks_overview.html#action

[tamper]:  https://www.preemptive.com/dotfuscator/ce/docs/help/checks_tamper.html
[debug]:  https://www.preemptive.com/dotfuscator/ce/docs/help/checks_debug.html
[root]: https://www.preemptive.com/dotfuscator/ce/docs/help/checks_root.html
[shelflife]:  https://www.preemptive.com/dotfuscator/ce/docs/help/checks_shelflife.html

[full]:  https://www.preemptive.com/dotfuscator/ce/docs/help/intro_capabilities.html
