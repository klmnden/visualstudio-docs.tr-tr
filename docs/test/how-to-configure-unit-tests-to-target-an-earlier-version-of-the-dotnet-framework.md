---
title: Birim testlerini .NET Framework'ün önceki sürümünü hedefleyecek
ms.date: 11/04/2016
ms.topic: conceptual
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
author: gewarren
ms.openlocfilehash: 0d77bd4fa5a1797b5e405c0b1af12cd1c24b18f7
ms.sourcegitcommit: 489aca71046fb6e4aafd0a4509cd7dc149d707b1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/25/2019
ms.locfileid: "58415947"
---
# <a name="how-to-configure-unit-tests-to-target-an-earlier-version-of-the-net-framework"></a>Nasıl yapılır: Birim testlerini .NET Framework'ün önceki sürümünü hedefleyecek şekilde yapılandırma

Microsoft Visual Studio ile bir test projesi oluşturduğunuzda, .NET Framework'ün en son sürümü ve hedef olarak varsayılan olarak ayarlanır. Test projeleri Visual Studio'nun önceki sürümlerinden yükseltiyorsanız, ayrıca, bunlar .NET Framework'ün en son sürümünü hedefleyecek şekilde yükseltilir. Proje özelliklerini düzenleyerek, açıkça projenin .NET Framework'ün önceki sürümleri için yeniden hedefleyebilirsiniz.

.NET Framework'ün belirli sürümlerini hedefleyen bir test projeleri birim oluşturabilirsiniz. Hedeflenen sürüm 3.5 veya sonraki sürümler olmalıdır ve bir istemci sürümü olamaz. Visual Studio, belirli sürümlerini hedefleyen birim testleri için aşağıdaki temel destek sağlar:

- Birim test projesi oluşturmak ve bunları belirli bir .NET Framework sürümünü hedef.

- Birim testleri belirli bir .NET Framework sürümünü hedefleyen yerel makinenizde Visual Studio'dan çalıştırabilirsiniz.

- Hedef .NET Framework'ün belirli bir sürümü kullanarak birim testlerini çalıştırabilirsiniz *MSTest.exe* komut isteminden.

- Birim Testleri yapının bir parçası olarak bir yapı aracısında çalıştırabilirsiniz.

**SharePoint uygulamalarını test etme**

Yukarıda listelenen özellikleri de birim testleri yazma ve Visual Studio kullanarak SharePoint uygulamaları için tümleştirme testleri sağlar. Visual Studio kullanarak SharePoint uygulamaları geliştirme hakkında daha fazla bilgi için bkz. [oluşturma SharePoint çözümleri](../sharepoint/create-sharepoint-solutions.md), [oluşturun ve SharePoint çözümlerinde hata ayıklama](../sharepoint/building-and-debugging-sharepoint-solutions.md) ve [doğrulayın ve hata ayıklama SharePoint kodunu](../sharepoint/verifying-and-debugging-sharepoint-code.md).

**Sınırlamalar**

.NET Framework'ün önceki sürümlerini kullanmak için test projelerinizi yeniden hedeflediğinizde aşağıdaki sınırlamalar geçerlidir:

- .NET Framework 3.5, çoklu sürüm desteği yalnızca birim testleri içeren test projeleri için desteklenir. .NET Framework 3.5, kodlanmış kullanıcı Arabirimi veya yük testi gibi diğer test türlerini desteklemez. Yeniden hedefleme, birim testleri dışında test türleri için engellenir.

- .NET Framework'ün önceki bir sürümde hedeflenen Test yürütme, yalnızca varsayılan ana bilgisayar bağdaştırıcısında desteklenir. ASP.NET ana bilgisayar bağdaştırıcısında desteklenmiyor. ASP.NET Geliştirme Sunucusu bağlamında çalışacak şekilde ASP.NET uygulamaları .NET Framework'ün geçerli sürümüyle uyumlu olması gerekir.

- .NET Framework 3.5 çoklu hedefleme desteği testleri çalıştırırken veri koleksiyonu desteği devre dışı bırakıldı. Visual Studio komut satırı araçlarını kullanarak kod kapsamı çalıştırabilirsiniz.

- Uzak makinede .NET Framework 3.5 kullanan birim testleri çalıştıramazsınız.

- Birim testleri için framework'ün önceki istemci sürümlerini hedefleyemez.

## <a name="retargeting-for-visual-basic-unit-test-projects"></a>Visual Basic birim testi projeleri için yeniden hedefleme

1. Yeni bir Visual Basic Oluştur **birim testi projesi** proje.

2. İçinde **Çözüm Gezgini**, seçin **özellikleri** sağ tıklama menüsünden Yeni bir Visual Basic test projesi.

     Visual Basic test projeniz için özellikleri görüntülenir.

3. Üzerinde **derleme** sekmesini, **Gelişmiş derleme seçenekleri** aşağıdaki çizimde gösterildiği gibi.

     ![Gelişmiş derleme seçenekleri](../test/media/howtoconfigureunittest35frameworka.png)

4. Kullanım **hedef Framework'ü (tüm yapılandırmaları)** için hedef Framework'ü değiştirmek için açılır listede **.NET Framework 3.5** veya sonraki bir sürümünü belirtme çizgisi B aşağıdaki resimde gösterildiği gibi. Bir istemci sürümü belirtilmemelidir.

     ![Hedef framework bırakma&#45;açılan listesinde](../test/media/howtoconfigureunitest35frameworkstepb.png)

## <a name="retargeting-for-c-unit-test-projects"></a>İçin yeniden hedefleme C# birim testi projeleri

1. Yeni bir C# **birim testi projesi** proje.

2. İçinde **Çözüm Gezgini**, seçin **özellikleri** yeni sağ tıklama menüsünden C# test projesi.

   Özellikleri, C# test projesi görüntülenir.

3. Üzerinde **uygulama** sekmesini, **hedef Framework'ü**. Aşağı açılan listeden seçin **.NET Framework 3.5** veya aşağıdaki çizimde gösterildiği gibi sonraki bir sürümü. Bir istemci sürümü belirtilmemelidir.

   ![Hedef framework bırakma&#45;açılan listesinde](../test/media/howtoconfigureunittest35frameworkcsharp.png)

## <a name="retargeting-for-ccli-unit-test-projects"></a>Yeniden hedefleme için C + +/ CLI birim testi projeleri

1. Yeni bir C++ oluşturma **birim testi projesi** proje.

   > [!WARNING]
   > İçin derleme C + +/ CLI birim testlerini .NET framework'ün önceki bir sürümü için Visual C++ için ilgili Visual Studio sürümünü kullanmanız gerekir.

2. İçinde **Çözüm Gezgini**, seçin **projeyi** yeni C++ test projenizden.

3. İçinde **Çözüm Gezgini**, kaldırılan C++ test projesi seçin ve ardından **Düzenle \<proje adı > .vcxproj**.

   *.Vcxproj* dosyası düzenleyicide açılır.

4. Ayarlama `TargetFrameworkVersion` sürüm 3.5 veya sonraki bir sürümde `PropertyGroup` etiketli `"Globals"`. Bir istemci sürümü belirtilmemelidir:

    ```xml
    <PropertyGroup Label="Globals">
        <TargetName>DefaultTest</TargetName>
        <ProjectTypes>{3AC096D0-A1C2-E12C-1390-A8335801FDAB};{8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942}</ProjectTypes>
        <ProjectGUID>{CE16D77A-E364-4ACD-948B-1EB6218B0EA3}</ProjectGUID>
        <TargetFrameworkVersion>3.5</TargetFrameworkVersion>
        <Keyword>ManagedCProj</Keyword>
        <RootNamespace>CPP_Test</RootNamespace>
      </PropertyGroup>
    ```

5. Kaydet ve Kapat *.vcxproj* dosya.

6. İçinde **Çözüm Gezgini**, Seç **projeyi** yeni C++ test projenizin sağ tıklatma menüsünden.

## <a name="see-also"></a>Ayrıca bkz.

- [SharePoint çözümleri oluşturma](../sharepoint/create-sharepoint-solutions.md)
- [Derleme ve SharePoint çözümlerinde hata ayıklama](../sharepoint/building-and-debugging-sharepoint-solutions.md)
- [Gelişmiş derleme Ayarları iletişim kutusu (Visual Basic)](../ide/reference/advanced-compiler-settings-dialog-box-visual-basic.md)
