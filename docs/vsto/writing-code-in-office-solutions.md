---
title: Office çözümlerinde kod yazma
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VST.Project.RefactoringCancelled
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- solutions [Office development in Visual Studio], writing code
- managed code [Office development in Visual Studio]
- Office development in Visual Studio, programming languages supported
- Office applications [Office development in Visual Studio], automating
- Office applications [Office development in Visual Studio], writing code
- writing code for Office solutions
- programming [Office development in Visual Studio], model
- Automation [Office development in Visual Studio], managed code
- application development [Office development in Visual Studio], programming model
- Office solutions [Office development in Visual Studio], writing code
- automating Office applications
- application development [Office development in Visual Studio], writing code
- application development [Office development in Visual Studio], automating
- Office projects [Office development in Visual Studio], changing namespaces
- solutions [Office development in Visual Studio], programming model
- programming [Office development in Visual Studio]
- namespaces [Office developmentin Visual Studio], changing in Office solutions
- projects [Office development in Visual Studio], writing code
- Office applications [Office development in Visual Studio], programming model
- managed code extensions [Office development in Visual Studio], writing code
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: cead0569ae067fcc503f7f2074807c609e6eed75
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255037"
---
# <a name="write-code-in-office-solutions"></a>Office çözümlerinde kod yazma
  Office projelerinde, Visual Studio 'daki diğer proje türlerinden farklı kod yazmanın bazı yönleri vardır. Bu farklılıkların birçoğu, Office nesne modellerinin yönetilen koda sunulma yöntemiyle ilgilidir. Diğer farklar Office projelerinin tasarımı ile ilgilidir.

 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]

## <a name="managed-code-and-office-programming"></a>Yönetilen kod ve Office programlama
 Tümleşik bir Microsoft Office çözümü oluşturmayı mümkün kılan temel teknoloji, bileşen nesne modeli (COM) teknolojisinin bir parçası olan otomatikleştirilmiştir. Otomasyon, uygun programlama arabirimlerini destekleyen herhangi bir uygulama, DLL veya ActiveX denetimi tarafından kullanıma sunulan yazılım nesnelerini oluşturmak ve denetlemek için kod kullanmanıza olanak sağlar.

### <a name="understand-primary-interop-assemblies"></a>Birincil birlikte çalışma derlemelerini anlama
 Microsoft Office uygulamalar, işlevlerinin çoğunu Otomasyon olarak sunar. Ancak, Office uygulamalarını otomatik hale getirmek için yönetilen kodu (Visual Basic C#veya gibi) kullanamazsınız. Yönetilen kod kullanarak Office uygulamalarını otomatikleştirmek için Office birincil birlikte çalışma derlemelerini (PIA 'lar) kullanmanız gerekir. Birincil birlikte çalışma derlemeleri, yönetilen kodun Office uygulamalarının COM tabanlı nesne modeliyle etkileşime geçmesini sağlar.

 Her Microsoft Office uygulamasının bir PIA 'i vardır. Visual Studio 'da bir Office projesi oluşturduğunuzda, projeye uygun PIA başvurusu otomatik olarak eklenir. Projedeki diğer Office uygulamalarının özelliklerini otomatikleştirmek için, uygun PIA 'ye el ile bir başvuru eklemeniz gerekir. Daha fazla bilgi için [nasıl yapılır: Birincil birlikte çalışma derlemeleri](../vsto/how-to-target-office-applications-through-primary-interop-assemblies.md)aracılığıyla Office uygulamalarını hedefleyin.

### <a name="use-primary-interop-assemblies-at-design-time-and-runtime"></a>Tasarım zamanında ve çalışma zamanında birincil birlikte çalışma derlemelerini kullanın
 Geliştirme görevlerinin çoğunu gerçekleştirmek için Office PIA 'Ları geliştirme bilgisayarınızda genel derleme önbelleğinde yüklü ve kayıtlı olmalıdır. Daha fazla bilgi için bkz. [Office çözümleri geliştirmek için bir bilgisayarı yapılandırma](../vsto/configuring-a-computer-to-develop-office-solutions.md).

 Office PIA 'ları, [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] son kullanıcı bilgisayarlarında veya daha sonra hedeflenen Office çözümlerini çalıştırmak için gerekli değildir. Daha fazla bilgi için bkz. [Office çözümleri tasarlama ve oluşturma](../vsto/designing-and-creating-office-solutions.md).

### <a name="use-types-in-primary-interop-assemblies"></a>Birincil birlikte çalışma derlemelerindeki türleri kullan
 Office PIA 'Ları, Office uygulamalarının nesne modelini ve doğrudan kodunuzda kullanılması amaçlanan ek altyapı türlerini sunan türlerin bir birleşimini içerir. Office PIA 'leri türlerine genel bakış için bkz. [Office birincil birlikte çalışma derlemelerindeki sınıflara ve arabirimlere genel bakış](/previous-versions/office/office-12/ms247299\(v\=office.12\)).

 Office PIA ' deki türler COM tabanlı nesne modellerinde türlere karşılık geldiğinden, bu türleri kullanma yönteminiz genellikle diğer yönetilen türlerden farklıdır. Örneğin, bir Office birincil birlikte çalışma derlemesinde isteğe bağlı parametrelere sahip yöntemleri çağırma yöntemi, projenizde kullanmakta olduğunuz programlama diline bağlıdır. Daha fazla bilgi için aşağıdaki konulara bakın:

- [Office çözümlerinde Isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md).

- [Office çözümlerinde geç bağlama](../vsto/late-binding-in-office-solutions.md).

## <a name="program-model-of-office-projects"></a>Office projelerinin program modeli
 Tüm Office projeleri, kodunuz için giriş noktası sağlayan bir veya daha fazla oluşturulmuş sınıf içerir. Bu sınıflar Ayrıca, ana bilgisayar uygulamasının nesne modeline ve Eylemler bölmeleri ve özel görev bölmeleri gibi özelliklere erişim sağlar.

### <a name="understand-the-generated-classes"></a>Oluşturulan sınıfları anlayın
 Excel ve Word için belge düzeyi projelerinde oluşturulan sınıf, uygulamanın nesne modelindeki en üst düzey bir nesneye benzer. Örneğin, bir Word belgesi `ThisDocument` projesindeki oluşturulan sınıf, Word nesne modelindeki <xref:Microsoft.Office.Interop.Word.Document> sınıfla aynı üyeleri sağlar. Belge düzeyi projelerdeki oluşturulan sınıflar hakkında daha fazla bilgi için bkz. [Program belge düzeyi özelleştirmeleri](../vsto/programming-document-level-customizations.md).

 VSTO eklenti projeleri adlı `ThisAddIn`oluşturulan bir sınıf sağlar. Bu sınıf, ana bilgisayar uygulamasının nesne modelindeki bir sınıfa benzemez. Bunun yerine, bu sınıf VSTO eklentisini temsil eder ve konak uygulamasının nesne modeline erişmek ve VSTO eklentileri için kullanılabilen diğer özelliklere erişmek için kullanabileceğiniz Üyeler sağlar. Daha fazla bilgi için bkz. [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md).

 Office projelerindeki tüm oluşturulan sınıflar, ve `Startup` `Shutdown` olay işleyicilerini içerir. Kod yazmaya başlamak için genellikle bu olay işleyicilerine kod eklersiniz. VSTO eklentisini başlatmak için `Startup` olay işleyicisine kod ekleyebilirsiniz. VSTO eklentisi tarafından kullanılan kaynakları temizlemek için `Shutdown` olay işleyicisine kod ekleyebilirsiniz. Daha fazla bilgi için bkz. [Office Projelerindeki Olaylar](../vsto/events-in-office-projects.md).

### <a name="access-the-generated-classes-at-run-time"></a>Çalışma zamanında oluşturulan sınıflara erişin
 Bir Office çözümü yüklendiğinde, [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] projenizdeki her bir oluşturulan sınıfı başlatır. Bu nesnelere, `Globals` sınıfını kullanarak projenizdeki herhangi bir koddan erişebilirsiniz. Örneğin, bir VSTO eklentisinin içindeki bir `Globals` şerit düğmesine ait bir olay işleyicisinden `ThisAddIn` sınıfındaki kodu çağırmak için sınıfını kullanabilirsiniz.

 Daha fazla bilgi için bkz. [Office Projelerindeki Nesnelere Genel erişim](../vsto/global-access-to-objects-in-office-projects.md).

### <a name="namespace-considerations-in-office-solutions"></a>Office çözümlerinde ad alanı konuları
 Projeyi oluşturduktan sonra bir Office projesinin *varsayılan ad alanını* (veya Visual Basic *kök ad alanını* ) değiştiremezsiniz. Varsayılan ad alanı, projeyi oluştururken belirttiğiniz proje adıyla her zaman eşleşmeyecektir. Projenizi yeniden adlandırırsanız, varsayılan ad alanı değişmez. Projelerdeki varsayılan ad alanı hakkında daha fazla bilgi için, bkz. [uygulama sayfası, proje &#40;Tasarımcısı&#35; C](../ide/reference/application-page-project-designer-csharp.md) ve [uygulama sayfası, proje &#40;Tasarımcısı&#41;Visual Basic](../ide/reference/application-page-project-designer-visual-basic.md).

### <a name="change-the-namespace-of-host-item-classes-in-c-projects"></a>C# Projelerdeki konak öğesi sınıflarının ad alanını değiştirme
 Konak `ThisAddIn`öğesi sınıflarının (örneğin `ThisWorkbook`,, veya `ThisDocument` sınıflarının) Visual C# Office projelerinde kendi ad alanları vardır. Varsayılan olarak, projenizdeki konak öğeleri için ad alanı, projeyi oluştururken belirttiğiniz proje adıyla eşleşir.

 Visual C# ofis projesindeki konak öğelerinin ad alanını değiştirmek Için **konak öğesi özelliği için ad alanını** kullanın. Daha fazla bilgi için bkz. [Office projelerindeki Özellikler](../vsto/properties-in-office-projects.md).

## <a name="supported-programming-languages-in-office-projects"></a>Office projelerinde desteklenen programlama dilleri
 Visual Studio 'daki Office proje şablonları yalnızca Visual Basic ve görsel C# programlama dillerini destekler. Bu nedenle, bu proje [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]şablonları yalnızca içindeki **Yeni proje** iletişim kutusunun **Visual Basic** ve  **C# görsel** düğümleri altında kullanılabilir. Daha fazla bilgi için [nasıl yapılır: Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)'da Office projeleri oluşturun.

## <a name="language-choice-and-office-programming"></a>Dil seçimi ve Office programlama
 Microsoft Office ve Visual Basic for Applications (VBA), uygulama özelleştirmenin iş akışını iyileştirmek için birlikte çalışacak şekilde geliştirilmiştir. Visual Basic bu geliştirmelerin bazılarını devraldı. Örneğin, Visual Basic isteğe bağlı parametreleri destekler, bu, Microsoft Office birincil birlikte çalışma derlemesinde bazı yöntemleri çağırırken Visual C#kullandığınızda daha az kod yazabileceğiniz anlamına gelir.

## <a name="program-with-visual-basic-vs-visual-c-in-office-solutions"></a>Visual Basic ile program karşılaştırması Office C# çözümlerinde görsel
 Office çözümlerini Visual Basic veya görseli C#kullanarak oluşturabilirsiniz. Microsoft Office nesne modelleri Microsoft Visual Basic for Applications (VBA) ile kullanılmak üzere tasarlandığından Visual Basic geliştiriciler Microsoft Office uygulamalar tarafından kullanıma sunulan nesnelerle rahatça çalıştırılabilir. Visual C# geliştiricileri Visual Basic geliştiricilerle aynı özelliklerden çoğunu kullanabilir, ancak Office nesne modellerini kullanmak için ek kod yazması gereken bazı durumlar vardır. Ayrıca, Office geliştirme ve Visual Basic ile C#yazılan Yönetilen koddaki temel programlama özellikleri arasında bazı farklılıklar vardır.

<!-- markdownlint-disable MD003 MD020 -->
## <a name="key-differences-between-visual-basic-and-visual-c"></a>Visual Basic ve görsel arasındaki önemli farklılıklarC#
<!-- markdownlint-enable MD003 MD020 -->

Aşağıdaki tabloda Office geliştirmede Visual Basic ve Visual C# arasındaki temel farklılıklar gösterilmektedir.

|Özellik|Açıklama|Visual Basic desteği|Görsel C# destek|
|-------------|-----------------|--------------------------|------------------------|
|İsteğe bağlı parametreler|Birçok Microsoft Office yöntemi, yöntemini çağırdığınızda gerekli olmayan parametrelere sahiptir. Parametresi için hiçbir değer geçirilmemişse, varsayılan bir değer kullanılır.|Visual Basic isteğe bağlı parametreleri destekler.|Visual C# , çoğu durumda isteğe bağlı parametreleri destekler. Daha fazla bilgi için bkz. [Office çözümlerinde Isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md).|
|Parametreleri başvuruya göre geçirme|Microsoft Office birincil birlikte çalışma derlemelerinin büyük bir kısmında isteğe bağlı parametreler, değer ile geçirilebilir. Ancak, bazı birincil birlikte çalışma derlemelerinde, başvuru türlerini kabul eden isteğe bağlı parametrelerin başvuruya göre geçirilmesi gerekir.<br /><br /> Değer ve başvuru türü parametreleri hakkında daha fazla bilgi için bkz. [bağımsız değişkenleri değere göre ve başvuruya &#40;göre&#41; geçirme Visual Basic](/dotnet/visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference) (Visual Basic için) ve [ &#40;parametreleri&#35; C programlama&#41;Kılavuzu](/dotnet/csharp/programming-guide/classes-and-structs/passing-parameters)olarak geçirin.|Parametreleri başvuruya göre geçirmek için ek bir iş gerekmez. Visual Basic derleyici gerektiğinde parametreleri otomatik olarak başvuruya göre geçirir.|Çoğu durumda, Visual C# derleyicisi gerektiğinde parametreleri otomatik olarak başvuruya göre geçirir. Daha fazla bilgi için bkz. [Office çözümlerinde Isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md).|
|Parametreli özellikler|Bazı özellikler parametreleri kabul eder ve salt okuma işlevleri olarak davranır.|Visual Basic, parametreleri kabul eden özellikleri destekler.|Visual C# , parametreleri kabul eden özellikleri destekler.|
|Geç bağlama|Geç bağlama, tasarım zamanında değişkenleri nesne türüne atamak yerine çalışma zamanında nesnelerin özelliklerinin belirlenmesi içerir.|**Kesin seçeneği** kapalı olduğunda Visual Basic geç bağlamayı gerçekleştirir. **Option Strict** açık olduğunda, geç bağlı üyelere erişmek için nesneleri açıkça dönüştürmeniz ve <xref:System.Reflection> ad alanındaki türleri kullanmanız gerekir. Daha fazla bilgi için bkz. [Office çözümlerinde geç bağlama](../vsto/late-binding-in-office-solutions.md).|Görsel C# , [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)]' i hedefleyen projelerde geç bağlamayı gerçekleştirir. Daha fazla bilgi için bkz. [Office çözümlerinde geç bağlama](../vsto/late-binding-in-office-solutions.md).|

## <a name="key-differences-between-office-development-and-managed-code"></a>Office geliştirme ve yönetilen kod arasındaki temel farklılıklar
 Aşağıdaki tabloda Office geliştirme ve Visual Basic veya görselde C#yazılan yönetilen kod arasındaki önemli farklılıklar gösterilmektedir.

|Özellik|Açıklama|Visual Basic ve görsel C# destek|
|-------------|-----------------|-----------------------------------------|
|Dizi dizinleri|Microsoft Office uygulamalardaki koleksiyonların alt dizi sınırı 1 ' den başlar. Visual Basic ve görselde C# 0 tabanlı diziler kullanın. Daha fazla bilgi için bkz [. &#40;Arrays&#35; C programlama&#41; Kılavuzu](/dotnet/csharp/programming-guide/arrays/index) ve [diziler Visual Basic](/dotnet/visual-basic/programming-guide/language-features/arrays/index).|Bir Microsoft Office uygulamasının nesne modelinde bir koleksiyonun ilk öğesine erişmek için, 0 yerine 1 dizinini kullanın.|

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
- [Office Projelerindeki Nesnelere Genel erişim](../vsto/global-access-to-objects-in-office-projects.md)
- [Office Projelerindeki Olaylar](../vsto/events-in-office-projects.md)
- [Nasıl yapılır: Birincil birlikte çalışma Derlemeleriyle Office uygulamalarını hedefleme](../vsto/how-to-target-office-applications-through-primary-interop-assemblies.md)
- [Nasıl yapılır: Office projelerinde olay işleyicileri oluşturma](../vsto/how-to-create-event-handlers-in-office-projects.md)
- [Office çözümlerinde geç bağlama](../vsto/late-binding-in-office-solutions.md)
- [Office çözümlerinin işbirlikçi geliştirmesi](../vsto/collaborative-development-of-office-solutions.md)
