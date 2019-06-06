---
title: Güvenlik
ms.date: 06/01/2018
ms.topic: conceptual
helpviewer_keywords:
- security [Visual Studio], applications
- application design, securability
ms.assetid: 7d32c4cf-8bec-4307-a2a8-42f0ceddf3eb
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2c5b0f4c748cd923ca02cb16ba374747c20d12d7
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66747663"
---
# <a name="secure-applications"></a>Uygulamaları güvenli hale getirme

Uygulama geliştirme sürecinizde, tasarımdan geliştirmeye kadar her yönüyle güvenliği göz önünde bulundurmalısınız. Visual Studio mümkün olduğunca güvenli bir şekilde çalıştırarak başlayın. Bkz: [kullanıcı izinleri](../ide/user-permissions-and-visual-studio.md).

Etkin bir şekilde güvenli uygulamalar geliştirmenize yardımcı olması için, geliştirmekte olduğunuz platformların güvenlik kavramları ve güvenlik özellikleri hakkında temel bilgiye sahip olmanız gerekir. Güvenli kodlama tekniklerini de anlamanız gerekir.

## <a name="code-for-security"></a>Güvenlik kodu

Bu güvenlik açıklarına neden olan çoğu kodlama hatası, geliştiricilerin kullanıcı girdisiyle çalışırken yanlış varsayımlarda bulunmaları olun veya bulunmadığından, kendisi için geliştirmekte olduğunuz platform tam olarak anlamadığınız oluşur.

- [Güvenli kodlama yönergeleri](/dotnet/standard/security/secure-coding-guidelines) .NET kodu güvenlik sistemi ile çalışacak şekilde tasarlanmıştır farklı yollarını açıklar.
- [C++ için en iyi güvenlik uygulamaları](/cpp/top/security-best-practices-for-cpp) C++ geliştiricilerine yönelik güvenlik araçları ve uygulamaları hakkında bilgi içerir.

## <a name="build-for-security"></a>Derleme için güvenlik

Güvenliği, ayrıca yapı işleminde önemli bir husus vardır. Bazı ek adımlar, dağıtılmış bir uygulamayı güvenliğini artırmak ve yetkisiz tersine mühendislik, yanıltma veya diğer saldırıları önlemeye yardımcı olmak:

- [Dotfuscator](dotfuscator/index.md) ücretsizdir ve .NET derlemelerini yetkisiz hata ayıklama gibi ters mühendislik ve yetkisiz kullanıma karşı korunmasına yardımcı olur.
- [Tanımlayıcı ad imzalama](managing-assembly-and-manifest-signing.md) benzersiz ad sahtekarlığını önlemeye ve yazılım bileşenlerini tanımlamak için kullanılabilir.

## <a name="see-also"></a>Ayrıca bkz.

- [.NET içinde güvenlik](/dotnet/standard/security/index)
- [Azure güvenlik](/azure/security/)
- [Windows 10 Mobile Güvenlik Kılavuzu](/windows/security/threat-protection/windows-10-mobile-security-guide)
- [Apache Cordova platform güvenlik özellikleri](/visualstudio/cross-platform/tools-for-cordova/security/best-practices?view=toolsforcordova-2017)
- [ASP.NET Core güvenlik](/aspnet/core/security/?view=aspnetcore-2.1)
- [Windows Forms güvenliği](/dotnet/framework/winforms/windows-forms-security)