---
title: Bir projedeki başvuruları yönetme
ms.date: 04/11/2018
ms.topic: conceptual
f1_keywords:
- vs.ProjectPropertiesReferencePaths
- cs.ProjectPropertiesReferencePaths
helpviewer_keywords:
- C# projects, references
- referencing objects, project references
- external component references
- referencing namespaces
- Visual Basic projects, references
- referencing components, external components
- Web references, types of project references
- namespaces [Visual Studio], referencing
- COM components, referencing
- objects [Visual Studio], referencing
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d04e5703c96b710208cc1ecc79a169a458463497
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62535581"
---
# <a name="manage-references-in-a-project"></a>Bir projedeki başvuruları yönetme

Bir dış bileşene karşı kodu yazın veya bağlı hizmet önce projeniz ilk buna bir başvuru içermelidir. Visual Studio bileşen veya hizmet bulmak gereken bilgileri içeren bir proje dosyası girdisinde aslında bir başvurudur.

Bir başvuru eklemek için sağ tıklayın **başvuruları** veya **bağımlılıkları** düğümünde **Çözüm Gezgini** ve **Başvuru Ekle**. Ayrıca proje düğümüne sağ tıklayın ve seçin **Ekle** > **başvuru**. Daha fazla bilgi için [nasıl yapılır: Başvuruları Ekle Kaldır](../ide/how-to-add-or-remove-references-by-using-the-reference-manager.md).

![Visual C dilinde bir başvuru ekleyin&#43;&#43;](../ide/media/vs2015_cpp_add_reference.png)

Bileşen ve hizmetlere aşağıdaki türde bir başvuru ekleyebilirsiniz:

- .NET framework sınıf kitaplıkları veya derlemeleri

- UWP uygulamaları

- COM bileşenleri

- Diğer derlemeleri veya aynı çözüm içindeki projelerin sınıf kitaplıkları

- XML Web hizmetleri

## <a name="uwp-app-references"></a>UWP uygulama başvuruları

### <a name="project-references"></a>Proje başvuruları

Koşuluyla bu projeleri, Windows 10'da kullanımdan kaldırılan API'leri kullanmıyorsa, Evrensel Windows Platformu (UWP) projeleri çözümdeki diğer UWP projeleri veya Windows 8.1 projeleri veya ikilileri, başvuruları oluşturabilirsiniz. Daha fazla bilgi için [UWP için Windows çalışma zamanı 8'den taşıma](/windows/uwp/porting/w8x-to-uwp-root).

Windows 10 için Windows 8.1 projeleri yeniden hedeflemek tercih ederseniz bkz [bağlantı noktası, geçirme ve yükseltme Visual Studio projeleri](../porting/port-migrate-and-upgrade-visual-studio-projects.md).

### <a name="extension-sdk-references"></a>Uzantı SDK başvuruları

Visual Basic C#, uzantı Sdk'leri, Windows 10'da kullanımdan kaldırılan API'leri kullanmıyorsa sürece, C++ ve JavaScript Evrensel Windows Platformu (UWP) uygulamaları, Windows 8.1, hedef uzantı Sdk'lerine başvurabilir. Olup, UWP uygulamaları tarafından başvurulabilir bulmak için uzantı SDK satıcısı sitesini gözden geçirin.

Belirlerseniz, uygulamanız tarafından başvurulan uzantı SDK'SİNİN desteklenmediğini ve ardından aşağıdaki adımları gerçekleştirmeniz gerekir:

1. Hataya neden olan projenin adını arayın. Projenizin hedeflediği platform, proje adı yanında, parantez içinde belirtilir. Örneğin, **MyProjectName (Windows 8.1)** projenizi anlamına **MyProjectName** platform sürümü Windows 8.1 desteği.

1. Desteklenmeyen uzantı SDK'sine sahip satıcının sitesine gidin ve projenizin hedeflediği platformun sürümü ile uyumlu olan bağımlılıkları içeren uzantı SDK'SİNİN sürümünü yükleyin.

    > [!NOTE]
    > Bir uzantı SDK bağımlılıklar başka uzantı SDK'lar üzerinde olup bulmanın bir yolu olan bakarak **başvuru Yöneticisi**. Visual Studio'yu yeniden başlatın, yeni bir C# UWP uygulaması projesini, sonra projeye sağ tıklayın ve ardından **Başvuru Ekle**. Git **Windows** sekmesini, sonra **uzantıları** alt sekme ve uzantı SDK'yı seçin. Sağ bölmede bakın **başvuru Yöneticisi**. Bağımlılıkları varsa, burada listelenir.

    > [!IMPORTANT]
    > Windows 10 projenizin hedeflediği ve önceki adımda yüklenen uzantı SDK'de Microsoft Visual C++ çalışma zamanı paketinde bağımlılık vardır, Microsoft Visual C++ çalışma zamanı sürümü Windows 10 ile uyumlu olan v14.0 olduğu ve yüklü Visual Studio ile.

1. Önceki adımda yüklenen uzantı SDK'de başka uzantı SDK'lar üzerinde bağımlılıkları varsa, bağımlılıklar ve projeniz platformun sürümü ile uyumlu olan bu bağımlılıkların sürümlerini yükleyin satıcıları sitelerini gidin hedefleme.

1. Visual Studio'yu yeniden başlatın ve uygulamanızı açın.

1. Sağ **başvuruları** veya **bağımlılıkları** hataya ve proje düğümünde **Başvuru Ekle**.

1. Tıklayın **Windows** sekmesini ve ardından **uzantıları** alt sekmesinde, eski uzantı Sdk'lerinin onay kutularının işaretini kaldırın ve yeni uzantı Sdk'lerinin onay kutularını işaretleyin. **Tamam**'ı tıklatın.

## <a name="add-a-reference-at-design-time"></a>Tasarım zamanında başvuru ekleme

Projenizde bir derlemeye bir başvuru yaptığınızda, Visual Studio derleme aşağıdaki konumlarda arar:

- Geçerli proje dizini. (Kullanarak bu derlemeleri bulabilirsiniz **Gözat** sekmesini.)

- Aynı çözüm içindeki diğer proje dizinleri. (Bu derlemeleri bulabilirsiniz **projeleri** sekmesini.)

> [!NOTE]
> - Tüm projeleri dolaylı bir başvuru içeren **mscorlib**.
> - Tüm projeleri dolaylı bir başvuru içeren `System.Core`bile `System.Core` başvurular listesinden kaldırılır.
> - Visual Basic projeleri dolaylı bir başvuru içeren <xref:Microsoft.VisualBasic>.

## <a name="references-to-shared-components-at-run-time"></a>Çalışma zamanında paylaşılan bileşenlere başvurular

Çalışma zamanında bileşenler projenin çıkış yolunda veya genel derleme önbelleği (GAC) içinde olmalıdır. Bu konumlardan birinde olmayan bir nesneye başvuru içeriyorsa, projeyi oluşturduğunuzda projenin çıktı yoluna başvuruyu kopyalamanız gerekir. <xref:Microsoft.VisualStudio.VCProjectEngine.VCProjectReference.CopyLocal%2A> Özelliği, bu kopyanın çıkarılmak zorunda olup olmadığını gösterir. Değer ise **True**, projeyi oluşturduğunuzda proje dizinine başvuru kopyalanır. Değer ise **False**, ise başvuru kopyalanmaz.

GAC'ye kayıtlı bir özel bileşene başvuru içeren bir uygulamayı dağıtırsanız, bileşen uygulama ile birlikte açmamasından dağıtılmaz <xref:Microsoft.VisualStudio.VCProjectEngine.VCProjectReference.CopyLocal%2A> ayarı. Visual Studio'nun önceki sürümlerinde, ayarlayabilirsiniz <xref:Microsoft.VisualStudio.VCProjectEngine.VCProjectReference.CopyLocal%2A> derlemenin dağıtıldığı emin olmak için bir başvuru özelliği. Şimdi, derlemeyi \Bin klasörüne el ile eklemelisiniz. Bu, özel kod ile size tanıdık olmayan yayımlama riskini azaltarak, scrutiny altında tüm özel kodları yerleştirir.

Varsayılan olarak, <xref:Microsoft.VisualStudio.VCProjectEngine.VCProjectReference.CopyLocal%2A> özelliği **False** derleme veya bileşen, genel derleme önbelleğindeyse veya bir çerçeve bileşeniyse. Aksi takdirde, değeri şuna ayarlı **True**. Projeden projeye başvurular her zaman ayarlanmış **True**.

## <a name="reference-a-project-or-assembly-that-targets-a-different-version-of-the-net-framework"></a>Bir proje ya da farklı bir .NET Framework sürümünü hedefleyen derlemeye başvuru

Projelere veya farklı bir .NET Framework sürümünü hedef derlemelere başvuran uygulamalar oluşturabilirsiniz. Örneğin, .NET Framework 4.5 hedefleyen bir derlemeye başvuran hedefleyen .NET Framework 4. 6'da, bir uygulama oluşturabilirsiniz. .NET Framework'ün önceki bir sürümünü hedefleyen bir proje oluşturursanız, bu projedeki bir proje ya da daha yeni bir sürümünü hedefleyen derlemeye başvuru ayarlanamaz.

Daha fazla bilgi için [Multi-targeting'e genel bakış](../ide/visual-studio-multi-targeting-overview.md).

## <a name="project-to-project-references"></a>Proje için proje başvuruları

Projeden projeye başvurular, derlemeler içeren projelere başvurulardır; bunları kullanarak oluşturduğunuz **proje** sekmesi. Visual Studio, projeye bir yolu verildiğinde bir derleme bulabilirsiniz.

Bir derleme üreten bir proje varsa, proje başvurusu ve bir dosya başvurusu (aşağıya bakın) kullanmamanız gerekir. Bir proje-proje başvurusunun avantajı yapı sistemindeki projeler arasında bağımlılık oluşturmasıdır. Bağımlı proje başvuran proje oluşturulan son daraltılmasından değişmiş ise oluşturulacaktır. Bu nedenle bağımlı proje oluşturmadan başvuran projeyi oluşturmak olasıdır ve başvuru geçersiz hale gelebilir bir dosya başvurusu bir yapı bağımlılığı oluşturmaz. (Diğer bir deyişle, proje proje daha önce oluşturulmuş bir sürümüne başvuruda bulunabilir.) Bu, gerekli tek bir DLL'nin çeşitli sürümlerini sonuçlanabilir *bin* dizinini mümkün değildir. Bu çakışma oluştuğunda, bir ileti gibi görürsünüz "Uyarı: Bu 'dosya' başvurusunun üzerine yazacağından 'proje' projesindeki ' dosya' bağımlılığı çalıştırma dizinine kopyalanamıyor". Daha fazla bilgi için [başvuruları bozuk sorun giderme](../ide/troubleshooting-broken-references.md) ve [nasıl yapılır: Oluşturma ve proje bağımlılıkları kaldırma](../ide/how-to-create-and-remove-project-dependencies.md).

> [!NOTE]
> Bir projenin .NET Framework hedef sürümü, sürüm 4.5 ise ve diğer projenin hedef sürümü sürüm 2, 3, 3.5 veya 4.0 ise bir proje proje başvurusu yerine dosya başvurusu oluşturulur.

## <a name="file-references"></a>Dosya başvuruları

Dosya başvurularını doğrudan Visual Studio projenin bağlamı dışında derlemelerine başvurular var. Bunları kullanarak oluşturduğunuz **Gözat** sekmesinde **başvuru Yöneticisi**. Bir dosya başvurusu bir derleme veya bileşen ve çıktı olarak oluşturan Proje değil yalnızca sahip olduğunuzda kullanın.

## <a name="see-also"></a>Ayrıca bkz.

- [Bozuk başvurularda sorun giderme](../ide/troubleshooting-broken-references.md)
- [Nasıl yapılır: Başvuruları Ekle Kaldır](../ide/how-to-add-or-remove-references-by-using-the-reference-manager.md)
