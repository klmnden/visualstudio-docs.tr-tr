---
title: Hedeflenen .NET Framework
ms.date: 02/06/2018
ms.topic: conceptual
helpviewer_keywords:
- targeting .NET Framework [Visual Studio]
- framework targeting [Visual Studio]
- .NET framework targeting [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: cb7af190ac7fc5d4d5ce547029689f6c902a6e4f
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66747638"
---
# <a name="framework-targeting-overview"></a>Framework hedefleme genel bakış

Visual Studio'da, projenizin hedeflemesini istediğiniz .NET sürümünü belirtebilirsiniz. Uygulamanın hedef bilgisayarda yüklü framework sürümü ile uyumlu olmalıdır Framework'ten başka bir bilgisayarda çalıştırmak .NET Framework uygulamaları için.

Hedef Çerçeve hakkında daha fazla bilgi için bkz: [hedef çerçeveyi](/dotnet/standard/frameworks).

Ayrıca, farklı sürümlerini hedefleyen .NET, projeleri içeren bir çözüm oluşturabilirsiniz. Çerçeve hedefleme, uygulamanın yalnızca belirtilen çerçeve sürümünde kullanılabilir olan işlevleri kullanmasının garantilenmesine yardımcı olur.

> [!TIP]
> Ayrıca, farklı platformlar için uygulamaları hedefleyebilirsiniz. Daha fazla bilgi için [çoklu hedefleme](../msbuild/msbuild-multitargeting-overview.md).

## <a name="framework-targeting-features"></a>Çerçeve hedefleme özellikleri

Çerçeve hedefleme şu özellikleri içerir:

- Önceki bir framework sürümünü hedefleyen bir proje açtığınızda Visual Studio otomatik olarak projeyi yükseltebilir veya hedefi olarak bırakın-olduğu.

- Bir .NET Framework projesi oluşturduğunuzda, hedeflemek istediğiniz .NET Framework sürümünü belirtebilirsiniz.

- Yapabilecekleriniz [birden çok çerçeveyi hedefleyen](/dotnet/standard/frameworks#how-to-specify-target-frameworks) tek bir projede.

- Aynı çözümdeki çeşitli projelerin her birinde, farklı bir .NET sürümünü hedefleyebilirsiniz.

- Varolan bir projenin .NET sürümünü değiştirebilirsiniz hedefler.

   Visual Studio bir projenin hedeflediği gerekli kılar .NET sürümünü değiştirdiğinizde, başvurular ve yapılandırma dosyalarını değiştirir.

Dinamik olarak Visual Studio'nun bir önceki framework sürümünü hedefleyen bir proje üzerinde çalışırken, geliştirme ortamını aşağıdaki gibi değişir:

- Öğelere **Yeni Öğe Ekle** iletişim kutusu, **Yeni Başvuru Ekle** iletişim kutusu ve **hizmet Başvurusu Ekle** kullanılabilir olmayan seçenekleri atlamak için iletişim kutusu hedeflenen sürümü.

- Özel denetimlerinde filtreler **araç kutusu** hedeflenen sürümde olmayanları kaldırın ve yalnızca göstermek için birden çok denetim uygun olduğunda en güncel kontrol eder.

- Bu filtreler **IntelliSense** hedeflenen sürümde kullanılamayan dil özelliklerini atlamak için.

- Özelliklere **özellikleri** hedeflenen sürümde bulunmayan o atlamak için penceresi.

- Bu, hedeflenen sürümde kullanılamayan seçenekleri atlamak için menü seçeneklerine filtre uygular.

- Derlemeler için derleyici ve derleyici seçenekleri hedeflenen sürüm için uygun sürümünü kullanır.

> [!NOTE]
> - Çerçeve hedefleme, uygulamanızın doğru şekilde çalışacağını garanti etmez. Hedeflenen sürümde çalışacağından çalıştığından emin olmak için uygulamanızı test etmeniz gerekir.
> - .NET Framework 2.0 altında framework sürümlerini hedefleyemezsiniz.

## <a name="select-a-target-framework-version"></a>Hedef framework sürümü seçin

Bir .NET Framework projesi oluşturduğunuzda, proje şablonunu seçtikten sonra hedef .NET Framework sürümünü seçebilirsiniz. Seçili şablon türü için geçerli olan yüklü framework sürümleri kullanılabilir çerçeveleri listesini içerir. .NET Framework proje şablonları, örneğin .NET Core şablonları için **Framework** açılır listede görünmez.

::: moniker range="vs-2017"

![Framework açılan VS 2017'de](media/vside-newproject-framework.png)

::: moniker-end

::: moniker range=">=vs-2019"

![VS 2019 Framework açılan listesi](media/vs-2019/configure-new-project-framework.png)

::: moniker-end

Varolan bir projede, hedef .NET sürümünü Proje Özellikleri iletişim kutusunda değiştirebilirsiniz. Daha fazla bilgi için [nasıl yapılır: .NET sürümü hedefleme](../ide/how-to-target-a-version-of-the-dotnet-framework.md).

## <a name="resolve-system-and-user-assembly-references"></a>Sistem ve kullanıcı derleme başvurularını çözümleme

Bir .NET sürümünü hedeflemek için önce uygun derleme başvurularını yüklemeniz gerekir. Farklı sürümleri .NET Geliştirici paketleri indirebileceğiniz [.NET indirir](https://www.microsoft.com/net/download/windows) sayfası.

.NET Framework projeleri için **Başvuru Ekle** iletişim kutusunda, hedef .NET Framework sürümüne ait değil ve böylece bunlar yanlışlıkla bir projeye eklenemez sistem derlemelerini devre dışı bırakır. (Sistem derlemeleri, *.dll* bir .NET Framework sürümünü dahil edilen dosyaların.) Hedeflenen sürümden daha yüksek bir framework sürümüne ait başvuruları çözmeyecek ve böyle bir başvuruya dayanan denetimler eklenemez. Böyle bir başvuruyu etkinleştirmek istiyorsanız, başvuru içeren bir projenin .NET Framework hedef sıfırlayın. Daha fazla bilgi için [nasıl yapılır: Hedef framework sürümü](../ide/how-to-target-a-version-of-the-dotnet-framework.md).

Derleme başvuruları hakkında daha fazla bilgi için bkz: [tasarım zamanında derlemeleri çözme](../msbuild/resolving-assemblies-at-design-time.md).

## <a name="enable-linq"></a>LINQ'i etkinleştirmek

.NET Framework 3.5 veya sonraki sürümler, bir başvuru hedeflediğinizde **System.Core** ve bir proje seviyesinde içeri alma için <xref:System.Linq> (yalnızca Visual Basic'te) otomatik olarak eklenir. LINQ özelliklerini kullanmak istiyorsanız, ayrıca etkinleştirmelisiniz `Option Infer` üzerinde (yalnızca Visual Basic'te). Hedefi önceki bir .NET Framework sürümü ile değiştirirseniz başvuru ve içe aktarma otomatik olarak kaldırılır. Daha fazla bilgi için [LINQ ile çalışma](/dotnet/csharp/tutorials/working-with-linq).

## <a name="see-also"></a>Ayrıca bkz.

- [Hedef çerçeveler](/dotnet/standard/frameworks)
- [Çoklu sürüm desteği (MSBuild)](../msbuild/msbuild-multitargeting-overview.md)
- [Nasıl yapılır: Hedef framework ve platform araç takımını (C++) değiştirme](/cpp/build/how-to-modify-the-target-framework-and-platform-toolset)