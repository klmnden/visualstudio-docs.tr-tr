---
title: 'Nasıl yapılır: Projeleri hedef platformlar için yapılandırma'
ms.date: 11/04/2016
ms.technology: vs-ide-compile
ms.topic: conceptual
helpviewer_keywords:
- project settings [Visual Studio], targeting platforms
- platforms, targeting specific CPUs
- project properties [Visual Studio], targeting platforms
- projects [Visual Studio], targeting platforms
- 64-bit [Visual Studio]
- 64-bit programming [Visual Studio]
- CPUs, targeting specific
- 64-bit applications [Visual Studio]
ms.assetid: 845302fc-273d-4f81-820a-7296ce91bd76
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e9f605e761380b3dc856926dff5bd1712753a8ba
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60045687"
---
# <a name="how-to-configure-projects-to-target-platforms"></a>Nasıl yapılır: Projeleri hedef platformlar için yapılandırma

Visual Studio uygulamalarınızı 64 bit platformlar da dahil olmak üzere, farklı platformları hedeflemek için ayarlamanıza olanak tanır. Visual Studio 64-bit platform desteği hakkında daha fazla bilgi için bkz. [64-bit uygulamalar](/dotnet/framework/64-bit-apps).

## <a name="target-platforms-with-the-configuration-manager"></a>Configuration Manager ile hedef platformlar

**Configuration Manager** projenizle hedef hızla yeni bir platform eklemek bir yol sağlar. Visual Studio'ya dahil edildi platformlardan birini seçerseniz, seçilen platform için projenizi yaratmanız için projeniz için özellikleri değiştirilmiştir.

### <a name="to-configure-a-project-to-target-a-64-bit-platform"></a>Bir 64 bit platformları hedefleyen bir proje yapılandırma

1. Menü çubuğunda, **derleme** > **Configuration Manager**.

2. İçinde **etkin çözüm platformu** listesinde, hedef çözümü için 64 bit platform seçin ve ardından **Kapat** düğmesi.

    1. İstediğiniz platform görünmüyorsa **etkin çözüm platformu** listesinde **yeni**.

         **Yeni çözüm platformu** iletişim kutusu görüntülenir.

    2. İçinde **yazın veya seçin yeni platformu** listesinde **x64**.

        > [!NOTE]
        >  Yapılandırmanızı yeni bir ad verin, ayarlarını değiştirmeniz gerekebilir **Proje Tasarımcısı** doğru platformunu hedeflemek için.

    3. Geçerli bir platform yapılandırmasını ayarlar kopyalamak istiyorsanız, bunu seçin ve ardından **Tamam** düğmesi.

64-bit platformu hedefleyen tüm projeler için özellikler güncelleştirilir ve projenin sonraki derleme için 64-bit platformlarda iyileştirilir.

## <a name="target-platforms-in-the-project-designer"></a>Proje Tasarımcısı'nda Hedef platformlar

**Proje Tasarımcısı** ayrıca projenizle farklı platformları hedeflemek için bir yol sağlar. Listede bulunan platformlardan birini seçilirken **yeni çözüm platformu** iletişim kutusunda, çözümünüz için çalışmıyor, özel yapılandırma adı oluşturmak ve ayarlarını değiştirmeyi **Proje Tasarımcısı**  doğru platformunu hedeflemek için.

Bu görevi gerçekleştirmek, kullandığınız programlama diline göre değişir. Daha fazla bilgi için aşağıdaki bağlantılara bakın:

- İçin [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] projeleri için bkz: [/Platform (Visual Basic)](/dotnet/visual-basic/reference/command-line-compiler/platform).

- İçin [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] projeleri için bkz: [derleme sayfası, Proje Tasarımcısı (C#)](../ide/reference/build-page-project-designer-csharp.md).

- İçin [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)] projeleri için bkz: [/CLR (ortak dil çalışma zamanı derlemesi)](/cpp/build/reference/clr-common-language-runtime-compilation).

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme platformlarını anlama](../ide/understanding-build-platforms.md)
- [/ Platform (C# Derleyici Seçenekleri)](/dotnet/csharp/language-reference/compiler-options/platform-compiler-option)
- [64-bit uygulamalar](/dotnet/framework/64-bit-apps)
- [Visual Studio IDE 64 Bit desteği](../ide/visual-studio-ide-64-bit-support.md)
