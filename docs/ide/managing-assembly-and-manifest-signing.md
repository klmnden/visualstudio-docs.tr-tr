---
title: Derleme ve bildirim imzalamayı yönetme
ms.date: 02/17/2017
ms.topic: conceptual
helpviewer_keywords:
- manifests [Visual Studio]
- signing manifests [Visual Studio]
- application manifests [Visual Studio]
- assemblies [Visual Studio], signing
ms.assetid: 6c1ef36b-25f7-4ad0-b29a-51801b7a5420
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 17cda43c2fab2944e5027f5292b405f8a9e2e084
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62538247"
---
# <a name="manage-assembly-and-manifest-signing"></a>Derleme ve bildirim imzalamayı yönetme

Tanımlayıcı ad imzalama bir yazılım bileşeni genel olarak benzersiz bir kimlik sağlar. Güçlü adlar derleme başkası tarafından görünerek edilemez olduğunu garanti ve bileşen bağımlılıklar ve yapılandırma deyimleri bileşen sürümü ve doğru bileşeni eşleme emin olmak için kullanılır.

Güçlü bir ad derlemenin kimliğinden (basit metin adından, sürüm numarası ve kültür bilgilerini) bir ortak anahtar belirteci ve dijital imza oluşur.

Visual Basic ve C# projelerinde imzalama derlemeler hakkında daha fazla bilgi için bkz: [tanımlayıcı adlı derlemeler oluşturma ve kullanma](/dotnet/framework/app-domains/create-and-use-strong-named-assemblies).

Görselde derlemeleri imzalama hakkında bilgi için C++ projeleri için bkz: [tanımlayıcı adlandırılmış derlemeler (C++/CLI)](/cpp/dotnet/strong-name-assemblies-assembly-signing-cpp-cli).

> [!NOTE]
> Ters mühendislik karşı derlemenin tanımlayıcı ad imzalama korumaz. Ters mühendislik karşı korumak için bkz: [Dotfuscator Community](dotfuscator/index.md).

## <a name="asset-types-and-signing"></a>Varlık türleri ve imzalama

.NET derlemelerini ve uygulama bildirimleri imzalayabilirsiniz:

- Yürütülebilir dosyalar (*.exe*)

- Uygulama bildirimleri (*. exe.manifest*)

- Dağıtım bildirimleri (*.application*)

- Paylaşılan bileşen derlemeler (*.dll*)

Aşağıdaki varlık türleri imzalayın:

1. Derlemeleri, Genel Derleme Önbelleği (GAC) bunları dağıtmak istiyorsanız.

2. ClickOnce Uygulama ve dağıtım bildirimleri. Visual Studio, bu uygulamalar için varsayılan olarak imzalama sağlar.

3. COM birlikte çalışabilirlik için kullanılan birincil birlikte çalışma derlemelerini. Birincil birlikte çalışma derlemesi bir COM tür kitaplığından oluştururken, TLBIMP yardımcı programı güçlü adlandırma zorlar.

Genel olarak, yürütülebilir dosyalar kaydolma. Kesin adlandırılmış bir bileşeni uygulama ile dağıtılan kesin adlandırılmış bir bileşen başvuramaz. Visual Studio uygulama yürütülebilir dosyaları oturum açmasını sağlamayan ancak bunun yerine zayıf adlı yürütülebilir öğeye işaret uygulama bildirimini imzalar. İmzalama, bağımlılıkları yönetmek daha zor zorlaştırabilir çünkü uygulamanıza özel bileşenler imzalama kaçının.

## <a name="how-to-sign-an-assembly-in-visual-studio"></a>Bir derlemeyi Visual Studio'da oturum açma

Bir uygulama veya bileşenin kullanarak oturum **imzalama** Proje Özellikleri penceresi için sekmesinde ('nde proje düğümüne sağ tıklayın **Çözüm Gezgini** seçip **özellikleri**). Seçin **imzalama** sekmesine ve ardından seçin **derlemeyi imzalamayı** onay kutusu.

Bir anahtar dosyası belirtin. Yeni bir anahtar dosyası oluşturmayı seçerseniz, yeni anahtar dosyaları her zaman oluşturulan *.pfx* biçimi. Yeni dosya için bir ad ve parola gerekir.

> [!WARNING]
> Anahtar dosyanızı başkası kullanmasını önlemek için bir parola ile her zaman korur. Sağlayıcıları veya sertifika depolarını kullanarak, anahtarlarınızın güvenliğini sağlayabilirsiniz.

Ayrıca, önceden oluşturduğunuz bir anahtara işaret edebilir. Anahtarları oluşturma hakkında daha fazla bilgi için bkz. [ortak-özel anahtar çifti oluşturma](/dotnet/framework/app-domains/how-to-create-a-public-private-key-pair).

Yalnızca ortak anahtar erişimi varsa, anahtar atama erteleneceği Gecikmeli imzalama'ı kullanabilirsiniz. Seçerek imzalamayı geciktirme etkinleştirme **gecikme yalnızca oturum** onay kutusu. Gecikmeli imzalanmış bir proje çalıştırmaz ve hata ayıklaması yapılamıyor. Ancak, geliştirme sırasında doğrulama kullanarak atlayabilir [Sn.exe tanımlayıcı ad aracı](/dotnet/framework/tools/sn-exe-strong-name-tool) ile `-Vr` seçeneği.

Bildirimleri imzalama hakkında daha fazla bilgi için bkz: [nasıl yapılır: Uygulama ve dağıtım bildirimlerini imzalama](../ide/how-to-sign-application-and-deployment-manifests.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Tanımlayıcı adlı derlemeler](/dotnet/framework/app-domains/strong-named-assemblies)
- [Tanımlayıcı adlandırılmış derlemeler (C++/CLI)](/cpp/dotnet/strong-name-assemblies-assembly-signing-cpp-cli)
