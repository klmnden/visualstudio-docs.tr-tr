---
title: UWP uygulamaları için uygulama özellik sayfası
ms.date: 01/23/2018
ms.topic: reference
f1_keywords:
- AppPackage.Properties.Application
helpviewer_keywords:
- Application page [UWP project]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- uwp
ms.openlocfilehash: 416661a39f54429f24cca66a0ec1be7b6c87629d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62791058"
---
# <a name="application-property-page-uwp-projects"></a>Uygulama özellik sayfası (UWP projeleri)

Kullanım **uygulama** Evrensel Windows Platformu (UWP) projenin derleme ve paket bilgilerini ve hedef Windows 10 sürümü belirtmek için özellik sayfası.

![Uygulama özellik sayfası](media/application-page-uwp.png)

Erişim için **uygulama** sayfasında, proje düğümünde **Çözüm Gezgini**. Ardından **proje** > **özellikleri** menü çubuğundaki. Özellik sayfaları açmak **uygulama** sekmesi.

## <a name="general-section"></a>Genel bölümünde

**Derleme adı**&mdash;derleme bildirimi tutacak çıkış dosyasının adını belirtir.

Bu özelliğe program aracılığıyla erişmek için bkz: <xref:VSLangProj.ProjectProperties.AssemblyName%2A>.

**Varsayılan ad alanı**&mdash;projeye eklenen dosyaları için temel ad alanını belirtir. Ad alanları hakkında daha fazla bilgi için bkz. [ad alanları (C# programlama Kılavuzu)](/dotnet/csharp/programming-guide/namespaces/), [ad alanları (Visual Basic)](/dotnet/visual-basic/programming-guide/program-structure/namespaces), veya [ad alanları (C++)](/cpp/cpp/namespaces-cpp).

Bu özelliğe program aracılığıyla erişmek için bkz: <xref:VSLangProj.ProjectProperties.RootNamespace%2A>.

**Derleme bilgileri**&mdash;görüntüler bu düğmeyi seçerek [derleme bilgileri iletişim kutusu](../../ide/reference/assembly-information-dialog-box.md).

**Paket bildirimi**&mdash;bu düğmeyi seçerek, bildirim Tasarımcısı açılır. Bildirim Tasarımcısı'nı seçerek de erişilebilir _Package.appxmanifest_ dosyası **Çözüm Gezgini**. Daha fazla bilgi için [bir paket bildirim Tasarımcısı ile yapılandırma](/windows/uwp/packaging/packaging-uwp-apps#configure-an-app-package).

## <a name="targeting-section"></a>Bölüm hedefleme

Bu bölümde açılan listeleri kullanarak, uygulamanız için en düşük sürümü Windows 10 ve hedef sürümü ayarlayabilirsiniz. Windows 10 en son sürümünü hedefleyen tavsiye edilir ve çok daha eski bir minimum sürümünü destekleyen bir kurumsal uygulama geliştiriyorsanız. Seçmek için hangi Windows 10 sürümü hakkında daha fazla bilgi için bkz. [UWP sürümünü seçin](/windows/uwp/updates-and-versions/choose-a-uwp-version).

Visual Studio'da hedef platform hakkında bilgi için bkz [Platform hedefleme](/visualstudio/productinfo/vs2017-compatibility-vs#platform-targeting).

## <a name="see-also"></a>Ayrıca bkz.

- [İlk UWP uygulamanızı oluşturma](/windows/uwp/get-started/your-first-app)
- [Bir UWP sürümünü seçin](/windows/uwp/updates-and-versions/choose-a-uwp-version)