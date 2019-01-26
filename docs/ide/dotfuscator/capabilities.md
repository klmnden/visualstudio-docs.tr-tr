---
title: Dotfuscator Özellikleri
ms.date: 10/10/2017
ms.devlang: dotnet
ms.prod: visual-studio-dev15
ms.topic: conceptual
keywords: Dotfuscator, Dotfuscator CE, PreEmptive, PreEmptive Solutions, PreEmptive koruma, koruma, community edition, gizleme, .NET, ücretsiz, Visual Studio 2017
helpviewer_keywords:
- PreEmptive Protection Dotfuscator
- Dotfuscator Community Edition
- Dotfuscator CE
- Dotfuscator
- obfuscation
- protection
description: Visual Studio 2017'de dahil edilen ücretsiz Dotfuscator Community Edition özelliklerini öğrenin.
ms.assetid: 0ee89c58-c900-48fc-a6a2-65ace00e8bab
author: Joe-Sewell-PreEmptive
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: b532bed6a20bd0fe79d4cdb820e9bcd5f15d1d8f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54935637"
---
# <a name="capabilities-of-dotfuscator"></a>Dotfuscator Özellikleri

Bu sayfa, Gelişmiş seçenekleri aracılığıyla kullanılabilen bazı başvurular Dotfuscator Community Edition (Dotfuscator CE) özelliklerine odaklanmıştır [yükseltmeleri][upgrades].

Dotfuscator olduğu bir *derleme sonrası* sistem .NET uygulamaları için.
Visual Studio kullanıcılarına Dotfuscator CE ile bağlanabildiğinizden emin [derlemeleri karartmak] [ obfuscation] ve ekleme [active koruma önlemleri] [ checks] içine Uygulama - tüm Dotfuscator özgün kaynak koduna erişim gerek olmadan.
Dotfuscator katmanlı koruma stratejisi oluşturma uygulamanızı birden çok yolla korur.

Dotfuscator CE gibi bir geniş .NET derlemesi ve uygulama türlerini destekler, [Evrensel Windows Platformu (UWP)] [ uwp] ve [Xamarin] [ xamarin].

## <a name="intellectual-property-protection"></a>Fikri mülkiyet koruması

Uygulama tasarımı, davranış ve uygulama fikri mülkiyet (IP) biçimler.
Ancak, .NET Framework için oluşturulan uygulamaların temelde books açın değildir; Ters mühendislik .NET derlemeleri için çok kolaydır [üst düzey meta veriler ve Ara kod içerdiğinden][assemblies].

Dotfuscator CE içeren temel [.NET karartma] [ obfuscation] biçiminde [yeniden adlandırma][renaming].
Bu adlandırma önemli bilgiler genel olarak Dotfuscator kodunuzla obfuscating tersine mühendislik, kaynak kodda için yetkisiz erişim riskini azaltır.
Gizleme çaba sarf, kod incelemesi - IP, ticari sır olarak yasal korunduğunu oluşturma önemli bir adım korumak için de gösterir.

Çoğu [uygulama bütünlüğünü koruma özellikleri](#application-integrity-protection) tersine mühendislik Dotfuscator CE daha fazla süreçlerden kaçınmıştır.
Örneğin, kötü bir aktör uygulamasının program mantığını anlamak için çalışan bir örneği için bir hata ayıklayıcının girişiminde bulunabilir.
Dotfuscator ekleme [koruma hata ayıklama davranışı] [ debug] uygulamanıza bu obstruct.

## <a name="application-integrity-protection"></a>Uygulama bütünlüğünü koruma

Kaynak kodunuzu korunmasına ek olarak, uygulamanızı tasarlandığı gibi kullanıldığından emin olmak önemli.
Saldırganlar, uygulamanızın lisanslama ilkeleri (yani, yazılım korsanlığı), çalabilir veya uygulama tarafından işlenen hassas verileri işlemek için ya da uygulamanın davranışını değiştirmek için aşmak için çalma girişiminde bulunabilir.

Dotfuscator CE ekleme [uygulama doğrulama kodu] [ checks] içine dahil olmak üzere derlemelerinizin [koruma kurcalamaya][tamper], [ Anti-hata ayıklama][debug], ve [hologram cihaza] [ root] ölçümleri.
Geçersiz uygulama durumu algılandığında bir doğrulama kodu için [uygun bir şekilde çağırmak durum adresine uygulama koduna bağlı][check-app].
Veya kodu yazamazlar tercih ederseniz Geçersiz tanıtıcı kullanan uygulama, Dotfuscator de ekleme [yanıt] [ check-action] , kaynak kodunuzda değişiklik gerektirmeden davranışları.

Bu aynı yöntemlerin çoğu zorlamak için de kullanılabilir [yaşam son teslim tarihlerine] [ shelflife] yazılım değerlendirme veya deneme sürümü için.

## <a name="see-also"></a>Ayrıca Bkz.

[Bu konudaki tam Dotfuscator CE Kullanıcı Kılavuzu][full]

<!-- Copyright © 2017 PreEmptive Solutions, LLC -->

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
