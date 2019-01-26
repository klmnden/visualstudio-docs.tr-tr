---
title: Güvenlik ve Yerleştirilmiş Yardımcı Derlemeler
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- key pairs for strong-named assemblies
- strong-named assemblies, security considerations
- satellite assemblies, localized
- code signing, assemblies
- security [Visual Studio], assemblies
- strong-named assemblies, localized
- assemblies [Visual Studio], security
- localization, satellite assemblies
ms.assetid: 6d953840-b301-47d5-8d34-30c1b29b5071
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9938398f0a4f9c81e26b3ddb3c0754e56a31a286
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55040275"
---
# <a name="security-and-localized-satellite-assemblies"></a>Güvenlik ve Yerleştirilmiş Yardımcı Derlemeler

Ana derlemenizin güçlü adlandırma kullanıyorsa, uydu derlemeleri ana derleme olarak aynı özel anahtarla oturum açmanız gerekir. Ortak/özel anahtar çifti eşleşmiyor ana ve yardımcı derlemeler, kaynaklarınız arasında yüklü değil ise. Derlemeleri imzalama hakkında daha fazla bilgi için bkz. [nasıl yapılır: Bir derlemeyi katı bir adla imzalamak](/dotnet/framework/app-domains/how-to-sign-an-assembly-with-a-strong-name).

 Genel olarak, kuruluşunuzun imzalama grubu veya özel anahtarla oturum dış imzalama kuruluş olması gerekebilir. Özel anahtarı hassas niteliği nedeniyle budur: erişimi kısıtlıdır genellikle birkaç kişi için. Geliştirme sırasında Gecikmeli imzalama kullanabilirsiniz. Daha fazla bilgi için [derlemeyi imzalamayı geciktirme](/dotnet/framework/app-domains/delay-sign-assembly).

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme güvenliği konuları](/dotnet/framework/app-domains/assembly-security-considerations)  - [anahtar güvenlik kavramları](/dotnet/standard/security/key-security-concepts)
- [.NET Framework Tabanlı Uluslararası Uygulamalara Giriş](../ide/introduction-to-international-applications-based-on-the-dotnet-framework.md)
- [Uygulamaları Yerelleştirme](../ide/localizing-applications.md)
- [Uygulamaları Genelleştirme ve Yerelleştirme](../ide/globalizing-and-localizing-applications.md)