---
title: .NET Framework hedefleme hatalarının sorunlarını giderme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.FrameworkTargetingErrors
- MSBuild.ResolveAssemblyReference.FailedToResolveReferenceBecausePrimaryAssemblyInExclusionList
helpviewer_keywords:
- targeting .NET Framework version [Visual Studio]
- versions [Visual Studio], .NET Framework Client Profile
- multi-targeting
- multitargeting
- .NET Framework Client Profile
ms.assetid: 830e3e45-9a93-4279-a249-75b84599aefb
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 465952fa41eab7d112ca839be2940cded3d69b33
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66744621"
---
# <a name="troubleshoot-net-framework-targeting-errors"></a>.NET Framework hedefleme hatalarının sorunlarını giderme
Bu konuda başvurusu nedeniyle oluşabilecek MSBuild hataları açıklanır sorunlar ve bu hataların nasıl çözebilirsiniz.

## <a name="you-have-referenced-a-project-or-assembly-that-targets-a-different-version-of-the-net-framework"></a>Bir proje ya da farklı bir .NET Framework sürümünü hedefleyen derlemeye başvuru
 Projelere veya .NET Framework'ün farklı sürümlerini hedefleyen derlemelere başvuran uygulamalar oluşturabilirsiniz. Örneğin, .NET Framework 2. 0'ı hedefleyen bir derlemeye başvuruyor ancak için .NET Framework 4 istemci Profili'ni hedefleyen bir uygulama oluşturabilirsiniz. .NET Framework'ün önceki bir sürümünü hedefleyen bir proje oluşturursanız, projeye bir proje ya da .NET Framework 4 veya .NET Framework 4 kendisi için istemci Profili'ni hedefleyen derlemeye başvuru ayarlanamaz. Hatayı gidermek için uygulamanızın bir profil veya projelere veya derlemelere göre uygulamanızı başvuran hedeflenen profiliyle uyumlu olan profilleri hedefler emin olun.

## <a name="you-have-re-targeted-a-project-to-a-different-version-of-the-net-framework"></a>Bir proje .NET Framework'ün farklı bir sürüme yeniden hedeflenen
 Uygulamanız için .NET Framework hedef sürümü değiştirme, Visual Studio bazı başvuruları değiştirir, ancak bazı başvuruları el ile güncelleştirmeniz gerekebilir. Hedef uygulama değiştirirseniz, örneğin, bir durum önceden bahsedilmiş hatalarla oluşabilir [!INCLUDE[net_v35SP1_long](../msbuild/includes/net_v35sp1_long_md.md)] ve uygulama veya kaynaklar için .NET Framework 4 istemci profili üzerinde kullanan ayarları vardır.

 Uygulama ayarlarını geçici olarak çözmek için açık **Çözüm Gezgini**, seçin **tüm dosyaları göster**ve ardından düzenleme *app.config* dosyasını Visual Studio XML düzenleyicisinde. Sürümü .NET Framework'ün uygun sürümünü eşleştirmek için ayarları değiştirin. Örneğin, 4.0.0.0 2.0.0.0 için sürüm ayarını değiştirebilirsiniz. Benzer şekilde, uygulamanın her zaman kaynakları eklemiştir açın **Çözüm Gezgini**, seçin **tüm dosyaları göster** sırasıyla, düğme **Projem** (Visual Basic) veya **Özellikleri** (C#) ve ardından düzenleme *Resources.resx* dosyasını Visual Studio XML düzenleyicisinde. Sürüm ayarı 4.0.0.0 2.0.0.0 için değiştirin.

 Uygulamanızın simgeleri veya bit eşlemleri gibi kaynaklara veya veri bağlantı dizeleri gibi ayarları varsa, ayrıca hata üzerinde tüm öğeleri kaldırarak çözebilirsiniz **ayarları** sayfasının **Proje Tasarımcısı**ve ardından gereken ayarları yeniden ekleme.

## <a name="you-have-re-targeted-a-project-to-a-different-version-of-the-net-framework-and-references-do-not-resolve"></a>Bir proje .NET Framework'ün farklı bir sürüme yeniden hedeflenmiş ve başvuruları çözümlenmiyor
 Bir proje farklı bir .NET Framework sürümü için hedefi yeniden belirlerseniz, başvurularınızı düzgün bazı durumlarda çözülemiyor olabilir. Açık tam derlemelere başvuruları genellikle bu soruna neden ancak çözümlenmiyor başvurularının kaldırılması ve sonra bunları projeye geri ekleyerek çözebilirsiniz. Alternatif olarak, başvuruları değiştirmek için proje dosyasını düzenleyebilirsiniz. İlk olarak, aşağıdaki biçimde başvuruları kaldırın:

```xml
<Reference Include="System.ServiceModel, Version=3.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089, processorArchitecture=MSIL" />
```

 Ardından, bunları basit form ile değiştirin:

```xml
<Reference Include="System.ServiceModel" />
```

> [!NOTE]
> Projenizi kapatıp sonra ayrıca tüm başvuruları doğru çözümleyemiyorsa emin olmak için yeniden oluşturmalısınız.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: .NET Framework sürümü hedefleme](../ide/how-to-target-a-version-of-the-dotnet-framework.md)
- [.NET framework istemci profili](/dotnet/framework/deployment/client-profile)
- [Framework hedefleme genel bakış](../ide/visual-studio-multi-targeting-overview.md)
- [Çoklu Sürüm Desteği](../msbuild/msbuild-multitargeting-overview.md)