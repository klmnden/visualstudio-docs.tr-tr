---
title: Bir .NET sürümünü hedefleme
ms.date: 03/21/2019
ms.topic: conceptual
helpviewer_keywords:
- targeting .NET [Visual Studio]
- .NET version [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 2c316610fc007e3e8642567c01a5172feb461bda
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66747129"
---
# <a name="how-to-target-a-version-of-net"></a>Nasıl yapılır: .NET sürümü hedefleme

Bu makalede, bir .NET Framework projesi oluşturduğunuzda, belirli bir .NET Framework sürümünü hedefleyecek şekilde açıklar. Ayrıca varolan bir Visual Basic içinde hedeflenen sürümün nasıl değiştirileceğini açıklar C#, veya F# proje.

> [!IMPORTANT]
> C++ projeleri için hedef sürümü değiştirme hakkında daha fazla bilgi için bkz: [nasıl yapılır: Hedef framework ve platform araç takımını değiştirmek](/cpp/build/how-to-modify-the-target-framework-and-platform-toolset).

## <a name="target-a-version-when-you-create-a-project"></a>Bir proje oluşturduğunuzda bir sürümünü hedefleme

Bir .NET Framework projesi oluşturduğunuzda, kullanılabilir .NET Framework sürümlerinin hangi sürümlerinin yüklü olduğunu ve seçilen proje şablonuna bağlıdır.

1. Menü çubuğunda, **dosya** > **yeni** > **proje**.

1. Oluşturmak istediğiniz proje türü için bir .NET Framework şablonu seçin.

1. Gelen **Framework** açılır listede iletişim kutusunun alt kısmında, projenizin hedeflemesini istediğiniz .NET Framework sürümünü seçin.

   Çerçeve listesi yalnızca seçtiğiniz şablon için geçerli olan sürümler gösterilmektedir.

   > [!NOTE]
   > .NET Core gibi bazı proje türleri görüntüleme **Framework** aşağı açılan listesi.

   ::: moniker range="vs-2017"

   ![Framework açılan yeni proje iletişim kutusunda Visual Studio 2017](media/vside-newproject-framework.png)

   ::: moniker-end

   ::: moniker range=">=vs-2019"

   ![VS 2019 Framework seçicide](media/vs-2019/configure-new-project-framework.png)

   ::: moniker-end

1. Devam [proje oluşturma](create-new-project.md).

## <a name="change-the-targeted-version"></a>Hedeflenen sürümü değiştirmek

Visual Basic'te .NET hedeflenen sürümünü değiştirebilirsiniz C#, veya F# bu yordamı izleyerek proje.

1. İçinde **Çözüm Gezgini**, değiştirin ve ardından istediğiniz projenin kısayol menüsünü **özellikleri**.

    ![Visual Studio Çözüm Gezgini özellikleri](../ide/media/vs_slnexplorer_properties.png)

1. Sol sütununda **özellikleri** penceresinde seçin **uygulama** sekmesi.

    ![Visual Studio uygulama özellikleri uygulama sekmesi](../ide/media/vs_slnexplorer_properties_applicationtab.png)

    > [!NOTE]
    > Bir UWP uygulaması oluşturduktan sonra Windows veya .NET hedeflenen sürümünü değiştiremezsiniz.

1. İçinde **hedef Framework'ü** listesinde, istediğiniz sürümü seçin.

1. Görüntülenen doğrulama iletişim kutusunda seçin **Evet** düğmesi.

    Projenin yüklemesi kaldırılır. Yeniden yüklediğinde, yalnızca seçtiğiniz .NET sürümünü hedefler.

    > [!NOTE]
    > Kodunuzu .NET, hedeflenen olandan farklı bir sürümüne başvurular içeriyorsa, derleme veya kod çalıştırdığınızda hata iletileri görülebilir. Bu hataları gidermek için başvuruları değiştirmeniz gerekir. Bkz: [hedefleme hatalarının .NET sorun giderme](../msbuild/troubleshooting-dotnet-framework-targeting-errors.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Framework hedefleme genel bakış](../ide/visual-studio-multi-targeting-overview.md)
- [.NET Framework hedefleme hatalarının sorunlarını giderme](../msbuild/troubleshooting-dotnet-framework-targeting-errors.md)
- [Uygulama sayfası, Proje Tasarımcısı (C#)](../ide/reference/application-page-project-designer-csharp.md)
- [Uygulama sayfası, Proje Tasarımcısı (Visual Basic)](../ide/reference/application-page-project-designer-visual-basic.md)
- [Nasıl yapılır: Hedef framework ve platform araç takımını (C++) değiştirme](/cpp/build/how-to-modify-the-target-framework-and-platform-toolset)