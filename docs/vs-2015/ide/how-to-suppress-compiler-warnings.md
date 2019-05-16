---
title: 'Nasıl yapılır: Derleyici uyarılarını gizleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: 31827b17-f933-413d-b28a-b19f903b64ca
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 994b29fb4592d55a04389896ee9db8848dceda67
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65695391"
---
# <a name="how-to-suppress-compiler-warnings"></a>Nasıl yapılır: Derleyici Uyarılarını Engelleme

[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Derleyici uyarılarını içerecek şekilde istemediğiniz bir veya daha fazla tür belirterek bir yapı günlüğüne declutter. Örneğin, bazı gözden geçirmek için bu teknik, ancak Normal, ayrıntılı ya da tanılama günlük derleme ayrıntı ayarladığınızda, otomatik olarak oluşturulan bilgilerin tümünü kullanabilirsiniz. Ayrıntı düzeyi hakkında daha fazla bilgi için bkz. [nasıl yapılır: Görüntüleme, kaydetme ve yapılandırma derleme günlüğü dosyalarını](../ide/how-to-view-save-and-configure-build-log-files.md).

### <a name="to-suppress-specific-warnings-for-visual-c-or-f"></a>Görsel için belirli uyarıları bastırmak için C# veya F\#

1. İçinde **Çözüm Gezgini**, uyarıları bastırmak istediğiniz projeyi seçin.

2. Menü çubuğunda, **görünümü**, **özellik sayfaları**.

3. Seçin **derleme** sayfası.

4. İçinde **uyarıları bastırma** kutusunda gizlemek istediğiniz uyarıların hata kodlarını noktalı virgülle ayırarak belirtin ve ardından çözümü yeniden oluşturun.

### <a name="to-suppress-specific-warnings-for-visual-c"></a>Visual C++ için belirli uyarıları bastırmak için

1. İçinde **Çözüm Gezgini**, projeyi seçin veya uyarıları bastırmak istediğiniz dosya kaynağı.

2. Menü çubuğunda, **görünümü**, **özellik sayfaları**.

3. Seçin **yapılandırma özellikleri** kategorisi seçin **C/C++** kategori seçip **Gelişmiş** sayfası.

4. Aşağıdaki adımlardan birini uygulayın:

    - İçinde **belirli uyarıları devre dışı** kutusunda, gizlemek istediğiniz uyarıları hata kodlarının noktalı virgülle ayrılmış belirtin.

    - İçinde **belirli uyarıları devre dışı** kutusunda **Düzenle** daha fazla seçenek görüntülenecek.

5. Seçin **Tamam** düğmesini ve ardından çözümü yeniden oluşturun.

## <a name="suppressing-warnings-for-visual-basic"></a>Visual Basic için uyarıları gizleme

Belirli bir derleyici uyarılarını Visual Basic projesi için .vbproj dosyasını düzenleyerek gizleyebilirsiniz. Ayrıca [derleme sayfası, Proje Tasarımcısı](../ide/reference/compile-page-project-designer-visual-basic.md) kategoriye göre uyarıları bastırmak için. Daha fazla bilgi için [Visual Basic'teki uyarıları yapılandırma](../ide/configuring-warnings-in-visual-basic.md).

#### <a name="to-suppress-specific-warnings-for-visual-basic"></a>Visual Basic için belirli uyarıları bastırmak için

1. İçinde **Çözüm Gezgini**, uyarıları bastırmak istediğiniz projeyi seçin.

2. Menü çubuğunda, **proje**, **projeyi**.

3. İçinde **Çözüm Gezgini**, proje için kısayol menüsünü açın ve ardından **Düzenle**_ProjectName_**.vbproj**.

    Proje dosyası Kod Düzenleyicisi'nde açılır.

4. Bulun `<NoWarn></NoWarn>` ile oluşturmakta olduğunuza yapı yapılandırma öğesi.

    Aşağıdaki örnekte gösterildiği `<NoWarn></NoWarn>` kalın metin için hata ayıklama derleme yapılandırmasını x x86 öğesinde platformu:

   ```xml
   <PropertyGroup Condition=" '$(Configuration)|$(Platform)' == 'Debug|x86' ">
       <PlatformTarget>x86</PlatformTarget>
       <DebugSymbols>true</DebugSymbols>
       <DebugType>full</DebugType>
       <Optimize>false</Optimize>
       <OutputPath>bin\Debug\</OutputPath>
       <DefineDebug>true</DefineDebug>
       <DefineTrace>true</DefineTrace>
       <ErrorReport>prompt</ErrorReport>
       <NoWarn></NoWarn>
       <WarningLevel>1</WarningLevel>
     </PropertyGroup>
   ```

5. Bir veya daha fazla uyarı numaralarını değeri olarak Ekle `<NoWarn>` öğesi. Birden çok uyarı numaralarını belirtirseniz, aşağıdaki örnekte gösterildiği gibi bir virgül ile ayırın.

   ```xml
   <PropertyGroup Condition=" '$(Configuration)|$(Platform)' == 'Debug|x86' ">
       <PlatformTarget>x86</PlatformTarget>
       <DebugSymbols>true</DebugSymbols>
       <DebugType>full</DebugType>
       <Optimize>false</Optimize>
       <OutputPath>bin\Debug\</OutputPath>
       <DefineDebug>true</DefineDebug>
       <DefineTrace>true</DefineTrace>
       <ErrorReport>prompt</ErrorReport>
       <NoWarn>40059,42024</NoWarn>
       <WarningLevel>1</WarningLevel>
     </PropertyGroup>
   ```

6. .vbproj dosyasındaki değişiklikleri kaydedin.

7. Menü çubuğunda, **proje**, **projeyi**.

8. Menü çubuğunda, **derleme**, **çözümü yeniden derle**.

    **Çıkış** penceresi artık belirtilen uyarıları gösterir.

   Daha fazla bilgi için [/nowarn](https://msdn.microsoft.com/library/7ebf2106-0652-4fdc-bf60-70fc86465d83).

## <a name="see-also"></a>Ayrıca Bkz.

- [İzlenecek yol: Uygulama Oluşturma](../ide/walkthrough-building-an-application.md)
- [Nasıl yapılır: Derleme Günlüğü Dosyalarını Görüntüleme, Kaydetme ve Yapılandırma](../ide/how-to-view-save-and-configure-build-log-files.md)
- [Derleme ve Oluşturma](../ide/compiling-and-building-in-visual-studio.md)
