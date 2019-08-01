---
title: Özel proje ve öğe şablonları oluşturma | Microsoft Docs
ms.date: 3/16/2019
ms.topic: conceptual
ms.assetid: 586da5dc-f678-402b-afd0-0332959fd7a6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: dff4d3566dcfb4b40f1008eed09371e42459c3a5
ms.sourcegitcommit: 9fc8b144d4ed1c46aba87c0b7e1d24454e0eea9d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/25/2019
ms.locfileid: "68493117"
---
# <a name="create-custom-project-and-item-templates"></a>Özel proje ve öğe şablonları oluşturma

Visual Studio SDK, özel bir proje şablonu ve özel bir öğe şablonu oluşturan proje şablonları içerir. Bu şablonlar, bazı ortak parametresi değişimleri dahil ve zip dosyaları olarak oluşturun. Değil bunlar otomatik olarak dağıtılır ve deneysel örneğinde kullanılabilir değildir. Oluşturulan ZIP dosyasını Kullanıcı şablonu dizinine kopyalamanız gerekir.

Şablon oluşturma şablonları, daha büyük uzantılarında şablonları dahil sağlar. Bu, kaynak dosyalarda sürüm denetimi uygulamanıza ve bir grup şablon projesini tek bir VSıX paketinde oluşturmanıza olanak sağlar.

Ayrıca, NuGet paketlerini yüklemek için bir şablon yapılandırabilirsiniz. Daha fazla bilgi için bkz. [Visual Studio şablonlarındaki NuGet paketleri](/nuget/visual-studio-extensibility/visual-studio-templates).

Temel şablon oluşturma senaryoları için kullanmanız gereken **şablonu dışarı aktar** Sihirbazı'nı, ama için sıkıştırılmış bir dosya çıkarır. Temel şablon oluşturma hakkında daha fazla bilgi için bkz. [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md).

> [!NOTE]
> Visual Studio 2017'den itibaren özel Proje ve öğe şablonları için tarama artık gerçekleştirilir. Bunun yerine, uzantı yükleme konumu olarak bu şablonları tanımlamak, şablon bildirim dosyalarını sağlamanız gerekir. VSIX uzantılarınızı güncelleştirmek için Visual Studio 2017'yi kullanabilirsiniz. Uzantınızı bir MSI kullanarak dağıtırsanız, şablon bildirim dosyalarını el ile oluşturmanız gerekir. Daha fazla bilgi için bkz. [Visual Studio 2017 için özel proje ve öğe şablonlarını yükseltme](../extensibility/upgrading-custom-project-and-item-templates-for-visual-studio-2017.md). Şablon bildirim şeması, [Visual Studio şablon bildirimi şema başvurusunda](../extensibility/visual-studio-template-manifest-schema-reference.md)belgelenmiştir.

## <a name="create-a-project-template"></a>Proje şablonu oluşturma

1. Bir proje şablonu projesi oluşturun. Proje şablonunu **Yeni proje** iletişim kutusunda "proje şablonu" arayarak ve C# ya da Visual Basic sürümünü seçerek bulabilirsiniz.

     Şablon bir sınıf dosyası, bir simge, *. vstemplate* dosyası, *ProjectTemplate. vbproj* veya *ProjectTemplate. csproj*adlı düzenlenebilir bir proje dosyası ve genellikle diğer proje türleri tarafından oluşturulan bazı dosyalar (örneğin *,) oluşturur. Resources. resx* dosyası, bir *AssemblyInfo* dosyası ve bir *. Settings* dosyası. Her kod dosyası, uygun yerlerde genel parametresi değişimleri içerir.

![Proje Şablonu proje seçimi](media/project-template-selection.png)

2. Ekleme ve projeniz için gereken proje öğeleri kaldırın. Düzenlenebilir proje dosyasını, *AssemblyInfo* dosyasını veya *. vstemplate* dosyasını kaldırmayın.

3. *. Vstemplate* dosyasını, eklemeleri ve silmeleri yansıtacak şekilde güncelleştirin. [Proje](../extensibility/project-element-visual-studio-templates.md) öğesi içermelidir bir [ProjectItem](../extensibility/projectitem-element-visual-studio-item-templates.md) şablona dahil edilecek her bir dosya için öğesi.

4. Kod dosyalarınızı ve diğer kullanıcıya yönelik içeriği değiştirme ve uygun parametresi değişimleri ekleyin.

5. Oluşturulan içerik gerektiği gibi değiştirin.

6. Projeyi oluşturun.

     Visual Studio, şablonunuzu içeren bir *. zip* dosyası oluşturur. Değil dağıtılan ve deneysel örneğinde kullanılabilir değil.

## <a name="create-an-item-template"></a>Öğe şablonu oluşturma

1. Bir öğe şablonu projesi oluşturun.

     Şablon bir sınıf dosyası, bir simge, bir *. vstemplate* dosyası ve bir *AssemblyInfo* dosyası oluşturur. Bazı ortak parametresi değişimleri sınıf dosyası içerir.

2. Ekleme ve projeniz için gereken proje öğeleri kaldırın.

3. *. Vstemplate* dosyasını, eklemeleri ve silmeleri yansıtacak şekilde güncelleştirin. [Proje](../extensibility/project-element-visual-studio-templates.md) öğesi içermelidir bir [ProjectItem](../extensibility/projectitem-element-visual-studio-item-templates.md) şablona dahil edilecek her bir dosya için öğesi.

4. Kod dosyalarınızı ve diğer kullanıcıya yönelik içeriği değiştirme ve uygun parametresi değişimleri ekleyin.

5. Oluşturulan içerik gerektiği gibi değiştirin.

6. Projeyi oluşturun.

     Visual Studio, şablonunuzu içeren sıkıştırılmış bir dosya oluşturur. Değil dağıtılan ve deneysel örneğinde kullanılabilir değil.

## <a name="deployment"></a>Dağıtım

### <a name="to-deploy-the-project-or-item-template"></a>Projeyi veya öğe şablonunu dağıtmak için

1. Bir VSIX projesi oluşturun. Daha fazla bilgi için bkz. [VSIX proje şablonu](../extensibility/vsix-project-template.md).

2. VSIX projesini başlangıç projesi olarak ayarlayın. İçinde **Çözüm Gezgini**, VSIX proje düğümünü sağ tıklatın ve seçin seçin **başlangıç projesi olarak ayarla**.

3. Proje şablonu projesi VSIX projesinin bir varlık ayarlayın. *. Valtmanifest* dosyasını açın. Git **varlıklar** sekmesine **yeni**.

    1. Ayarlama **türü** alanı **Microsoft.VisualStudio.ProjectTemplate** veya **Microsoft.VisualStudio.ItemTemplate**.

    2. Kaynağı için **mevcut çözümde bir proje** seçeneğini ve ardından şablonunuzu içeren projeyi seçin.

4. Çözümü oluşturun ve **F5**tuşuna basın. Deneysel örneği açılır.

5. Proje şablonu projesi için, proje şablonunuzu, **Yeni proje** iletişim kutusunda (**Dosya** > **Yeni** > **Proje**), görsel C# veya Visual Basic düğümünde görmeniz gerekir. Bir öğe şablonu projesi için, öğe şablonunuzun **Yeni öğe Ekle** iletişim kutusunda listelendiğini görmeniz gerekir. **Yeni öğe Ekle** iletişim kutusunu görüntülemek için, **Çözüm Gezgini**, proje düğümünü seçin ve**Yeni öğe** **Ekle** > ' ye tıklayın.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio şablon başvurusu](../ide/creating-project-and-item-templates.md)
- [Visual Studio şablonları NuGet paketleri](/nuget/visual-studio-extensibility/visual-studio-templates)
