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
author: ghogen
ms.author: ghogen
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: faef9f55a88385953a121574f761193cc8c11ea9
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416829"
---
# <a name="how-to-configure-projects-to-target-platforms"></a>Nasıl yapılır: Projeleri hedef platformlar için yapılandırma

Visual Studio uygulamalarınızı 64 bit platformlar da dahil olmak üzere, farklı platformları hedeflemek için ayarlamanıza olanak tanır. Visual Studio 64-bit platform desteği hakkında daha fazla bilgi için bkz. [64-bit uygulamalar](/dotnet/framework/64-bit-apps).

## <a name="target-platforms-with-the-configuration-manager"></a>Configuration Manager ile hedef platformları

**Configuration Manager** , projenizde hedeflemek üzere yeni bir platform eklemek için bir yol sağlar. Visual Studio 'ya dahil olan platformlardan birini seçerseniz, projenizin özellikleri seçili platform için projenizi oluşturmak üzere değiştirilir.

### <a name="to-configure-a-project-to-target-a-64-bit-platform"></a>Bir projeyi 64 bitlik bir platformu hedefleyecek şekilde yapılandırmak için

1. Menü çubuğunda**Configuration Manager** **Oluştur** > ' u seçin.

2. **Etkin çözüm platformu** listesinde, çözümün hedeflenecek 64 bitlik bir platform seçin ve sonra **Kapat** düğmesini seçin.

    1. İstediğiniz Platform **etkin çözüm platformu** listesinde görünmüyorsa, **Yeni**' yi seçin.

         **Yeni çözüm platformu** iletişim kutusu görüntülenir.

    2. **Yazın veya yeni platform listesini seçin** , **x64**öğesini seçin.

        > [!NOTE]
        > Yapılandırmanıza yeni bir ad verirseniz, **Proje tasarımcısında** ayarları doğru platformu hedefleyecek şekilde değiştirmeniz gerekebilir.

    3. Ayarları geçerli platform yapılandırmasından kopyalamak istiyorsanız, seçin ve sonra **Tamam** düğmesini seçin.

64 bitlik platformu hedefleyen tüm projeler için özellikler güncellenir ve projenin sonraki derlemesi 64 bit platformlar için iyileştirilir.

## <a name="target-platforms-in-the-project-designer"></a>Proje tasarımcısında hedef platformlar

**Proje Tasarımcısı** Ayrıca, projenizle farklı platformları hedeflemek için bir yol sağlar. **Yeni çözüm platformu** iletişim kutusundaki listede yer alan platformlardan birini seçmek çözümünüz için çalışmazsa, özel bir yapılandırma adı oluşturabilir ve **Proje tasarımcısında** ayarları değiştirerek doğru platformu hedefleyebilirsiniz .

Bu görevin gerçekleştirilmesi, kullanmakta olduğunuz programlama diline göre farklılık gösterir. Daha fazla bilgi için aşağıdaki bağlantılara bakın:

- Projeler [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] için bkz. [/Platform (Visual Basic)](/dotnet/visual-basic/reference/command-line-compiler/platform).

- Projeler [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] için bkz. [derleme sayfası, proje Tasarımcısı (C#)](../ide/reference/build-page-project-designer-csharp.md).

- Projeler [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)] için bkz. [/clr (ortak dil çalışma zamanı derlemesi)](/cpp/build/reference/clr-common-language-runtime-compilation).

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme platformlarını anlama](../ide/understanding-build-platforms.md)
- [/Platform (C# derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/platform-compiler-option)
- [64 bitlik uygulamalar](/dotnet/framework/64-bit-apps)
- [Visual Studio IDE 64 bit desteği](../ide/visual-studio-ide-64-bit-support.md)
