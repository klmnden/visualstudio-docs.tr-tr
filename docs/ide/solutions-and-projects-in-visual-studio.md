---
title: Çözümler ve projeler
ms.date: 10/05/2017
ms.topic: conceptual
f1_keywords:
- vs.addnewitem
- vs.addnewsolutionitem
- vs.openproject
- vs.addexistingitem
- vs.addexistingsolutionitem
- vs.environment.projects
- vs.environment.solutions
- VS.SolutionExplorer
- VS.SolutionExplorer.Solutions
helpviewer_keywords:
- solutions [Visual Studio]
- projects [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 42a8dbc2fd9a6fc89b0be62271b048f8275a82b2
ms.sourcegitcommit: ba5e072c9fedeff625a1332f22dcf3644d019f51
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/31/2019
ms.locfileid: "66432203"
---
# <a name="solutions-and-projects-in-visual-studio"></a>Visual Studio'da projeler ve çözümler

Bu makalede bu kavramı bir *proje* ve *çözüm* Visual Studio'da. Yeni bir proje oluşturmak nasıl de kısaca ele alınmaktadır ve **Çözüm Gezgini** araç penceresi.

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [projeler ve çözümler Mac için Visual Studio'da](/visualstudio/mac/projects-and-solutions).

## <a name="projects"></a>Projeler

Web sitesi, eklenti, vb. bir uygulama oluşturduğunuzda, Visual Studio'da ile başlatma bir *proje*. Mantıksal bir anlamda, bir projenin tüm kaynak kodu dosyaları, simgeler, resimler, veri dosyalarını, bir yürütülebilir dosya, kitaplık veya Web sitenize derlenmiş vb. içerir. Bir proje, derleyici ayarları ve çeşitli hizmetler veya programınızın iletişim kuran bileşenler tarafından gerekebilecek diğer yapılandırma dosyalarını da içerir.

> [!NOTE]
> Çözümlerin veya projelerin düzenlemek, yapı ve kod hatalarını ayıklamak için Visual Studio'da kullanmak zorunda değilsiniz. Yalnızca Visual Studio kaynak dosyalarını içeren klasörü açın ve düzenlemeye başlayın. Daha fazla bilgi için [kod Visual Studio'da projeler veya çözümler olmadan geliştirme](../ide/develop-code-in-visual-studio-without-projects-or-solutions.md).

Bir proje uzantılı bir XML dosyasında aşağıdaki gibi tanımlanır *.vbproj*, *.csproj*, veya *.vcxproj*. Bu dosya, projedeki tüm öğeleri yolları ve sanal klasör hiyerarşisi içerir. Ayrıca, yapılandırma ayarlarını içerir.

> [!TIP]
> Visual Studio'da bir proje dosyasının içeriğini bakmak için ilk proje adlarında'i seçerek projeyi **Çözüm Gezgini** seçip **kaldırma proje** bağlamı veya sağ tıklama menüsünde. Daha sonra yeniden bağlam menüsünü açın ve seçin **Düzenle \<projectname\>** .

Visual Studio'da proje dosyası tarafından kullanılan **Çözüm Gezgini** proje içeriğini ve ayarlarını görüntülemek için. Projenizi derlerken, MSBuild altyapısına yürütülebilir dosyayı oluşturmak için proje dosyasını kullanır. Çıkış diğer türleri üretmek için projeleri de özelleştirebilirsiniz.

## <a name="solutions"></a>Çözümler

Bir proje içinde yer alan bir *çözüm*. Adını rağmen bir çözüm "yanıt" değildir. Bu yalnızca bir veya daha fazla ilgili projelerini, yapı bilgilerini, Visual Studio penceresi ayarlarını ve belirli bir proje ile ilişkili olmayan diğer tüm dosyalar yanı sıra bir kapsayıcıdır. Bir metin dosyası tarafından açıklanan bir çözüm (uzantı *.sln*) kendi benzersiz biçimde; bunu el ile düzenlenmesi amaçlanmaz.

Visual Studio kullanan iki dosya türleri ( *.sln* ve *.suo*) çözümleri için ayarları saklamak için:

|Dahili numara|Ad|Açıklama|
|---------------|----------|-----------------|
|.sln|Visual Studio çözümü|Projeler, proje öğeleri ve çözümde çözüm öğeleri düzenler.|
|.suo|Çözüm kullanıcı seçenekleri|Kullanıcı düzeyi ayarları ve kesme noktaları gibi özelleştirmelerini depolar.|

## <a name="create-new-projects"></a>Yeni projeler oluştur

Belirli bir tür uygulama veya Web sitesi için bir proje şablondan yeni bir proje oluşturmak için en kolay yolu başlatmaktır. Bir proje şablonu, önceden oluşturulan kod dosyaları, yapılandırma dosyaları, varlıkları ve ayarları temel bir kümesinden oluşur. Oluşturduğunuz yeni proje iletişim kutusunda bu şablonları mevcuttur (**dosya** > **yeni** > **proje**). Daha fazla bilgi için [Visual Studio'da yeni proje oluşturma](create-new-project.md) ve [çözümler ve projeler oluşturma](../ide/creating-solutions-and-projects.md).

Genellikle belirli bir şekilde projelerinizi özelleştirirseniz, ardından yeni projeleri oluşturmak için kullanabileceğiniz özel Proje şablonu oluşturabilirsiniz. Daha fazla bilgi için [proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md).

Yeni bir proje oluşturduğunuzda, varsayılan olarak kaydedilmeden *%USERPROFILE%\source\repos*. Bu konumda değiştirebilirsiniz **proje konumu** bölümündeki **Araçları** > **seçenekleri** > **projeler ve Çözümleri** > **konumları**. Daha fazla bilgi için [sayfa projeler ve çözümler, Seçenekler iletişim kutusu](../ide/reference/projects-and-solutions-options-dialog-box.md).

## <a name="solution-explorer"></a>Çözüm Gezgini

Yeni bir proje oluşturduğunuzda, kullanabileceğiniz **Çözüm Gezgini** proje ve çözüm ve onların ilişkilendirilmiş öğelerini görüntülemek ve yönetmek için. Aşağıdaki çizimde gösterildiği **Çözüm Gezgini** ile bir C# iki proje içeren bir çözümü:

![Çözüm Gezgini](../ide/media/vs2015_solution_explorer.png)

Çoğu menü komutları, çeşitli öğelere sağ tıklama menüsünden kullanılabilir **Çözüm Gezgini**. Yalnızca birkaçıdır çalışan testleri ve bir dosyayı yeniden adlandırma, bir başvuru eklemeyi, NuGet paketlerini yönetme, bir proje oluşturma şu komutları içerir. Araç çubuğunun üstündeki **Çözüm Gezgini** bir klasör görünümüne bir çözüm görünümünde, gizli dosyaları göster ve tüm düğümleri Daralt düğmesi vardır.

ASP.NET Core projeleri için nasıl dosyaları iç içe geçmiş özelleştirebilirsiniz **Çözüm Gezgini**. Daha fazla bilgi için [Çözüm Gezgini'nde dosya iç içe yerleştime özelleştirme](file-nesting-solution-explorer.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio IDE](../get-started/visual-studio-ide.md)
- [Projeler ve çözümler (Mac için Visual Studio)](/visualstudio/mac/projects-and-solutions)
- [Ekleme ve kaldırma proje öğeleri (Mac için Visual Studio)](/visualstudio/mac/add-and-remove-project-items)
