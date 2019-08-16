---
title: Word çözümleri
ms.date: 08/14/2019
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- solutions [Office development in Visual Studio], Word
- Office projects [Office development in Visual Studio], Word
- application-level add-ins [Office development in Visual Studio], Word
- Word [Office development in Visual Studio]
- projects [Office development in Visual Studio], Word
- Word [Office development in Visual Studio], about Word solutions
- Office solutions [Office development in Visual Studio], Word
- Word [Office development in Visual Studio], application-level add-ins
- documents [Office development in Visual Studio], Word
- Office development in Visual Studio, Word solutions
- add-ins [Office development in Visual Studio], Word
- Word [Office development in Visual Studio], document-level customizations
- user interfaces [Office development in Visual Studio], Word
- Office documents [Office development in Visual Studio, Word
- document-level customizations [Office development in Visual Studio], Word
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 5c8837c1c95dc5f032a10773645f93a46ec29662
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69551213"
---
# <a name="word-solutions"></a>Word çözümleri
  Visual Studio, Microsoft Office Word için belge düzeyi özelleştirmeler ve VSTO eklentileri oluşturmak için kullanabileceğiniz proje şablonları sağlar. Bu çözümleri, Word 'Ü otomatikleştirmek, Word özelliklerini genişletmek ve Word Kullanıcı arabirimini (UI) özelleştirmek için kullanabilirsiniz. Belge düzeyi özelleştirmeleri ve VSTO eklentileri arasındaki farklar hakkında daha fazla bilgi için bkz. [Office çözümleri geliştirmesine genel bakış &#40;VSTO&#41;](../vsto/office-solutions-development-overview-vsto.md).

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

[!include[Add-ins note](includes/addinsnote.md)]

 Bu konuda, aşağıdaki bilgiler sağlanmaktadır:

- [Word 'Ü otomatikleştirin](#automating).

- [Word için belge düzeyi özelleştirmeleri geliştirin](#doclevel).

- [Word IÇIN VSTO eklentileri geliştirin](#applevel).

- [Word 'ün Kullanıcı arabirimini özelleştirin](#UI).

## <a name="automating"></a>Word 'Ü Otomatikleştir
 Word nesne modeli, Word 'Ü otomatikleştirebilmek için kullanabileceğiniz birçok türü ortaya çıkarır. Örneğin, programlama yoluyla tablo oluşturabilir, belgeleri biçimlendirebilir ve metin aralıklarını ve paragrafları ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Word nesne modeline genel bakış](../vsto/word-object-model-overview.md).

 Visual Studio 'da Word çözümleri geliştirirken, çözümlerinizde *konak öğelerini* ve *konak denetimlerini* de kullanabilirsiniz. Bunlar, <xref:Microsoft.Office.Interop.Word.Document> ve <xref:Microsoft.Office.Interop.Word.ContentControl> nesneleri gibi Word nesne modelinde yaygın olarak kullanılan belirli nesneleri genişleten nesnelerdir. Genişletilmiş nesneler, temel aldığı Word nesneleri gibi davranır, ancak nesnelere ek olaylar ve veri bağlama özellikleri ekler. Daha fazla bilgi için bkz. [genişletilmiş nesneleri kullanarak Word 'Ü otomatikleştirme](../vsto/automating-word-by-using-extended-objects.md).

## <a name="doclevel"></a>Word için belge düzeyi özelleştirmeleri geliştirme
 Microsoft Office Word için belge düzeyi özelleştirmesi, belirli bir belgeyle ilişkili bir derlemeden oluşur. Derleme, genellikle, Kullanıcı arabirimini özelleştirerek ve Word 'Ü otomatikleştirerek belgeyi genişletir. Word ile ilişkili olan VSTO eklentisinin aksine, bir özelleştirmeye uyguladığınız işlevsellik yalnızca ilişkili belge Word 'de açık olduğunda kullanılabilir.

 Word için belge düzeyi özelleştirme projesi oluşturmak için, Visual Studio 'nun **Yeni proje** Iletişim kutusundaki Word belgesi veya Word şablonu proje şablonları ' nı kullanın. Daha fazla bilgi için [nasıl yapılır: Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)'da Office projeleri oluşturun.

 Belge düzeyi özelleştirmelerinin nasıl çalıştığı hakkında daha fazla bilgi için [belge düzeyi özelleştirmelerinin mimarisi](../vsto/architecture-of-document-level-customizations.md).

### <a name="word-customization-programming-model"></a>Word özelleştirme programlama modeli
 Word için belge düzeyi projesi oluşturduğunuzda, Visual Studio çözümünüzün temeli olan adlı `ThisDocument`bir sınıf oluşturur. Bu sınıf, çözümünüzle ilişkili belgeyi temsil eder ve kodunuzu yazmak için bir başlangıç noktası sağlar.

 Belge düzeyi projede kullanabileceğiniz `ThisDocument` sınıf ve diğer özellikler hakkında daha fazla bilgi için, bkz. [Program belge düzeyi özelleştirmeleri](../vsto/programming-document-level-customizations.md).

## <a name="applevel"></a>Word için VSTO eklentileri geliştirme
 Microsoft Office Word için VSTO eklentisi Word tarafından yüklenen bir derlemeden oluşur. Derleme tipik olarak, Kullanıcı arabirimini özelleştirerek ve Word 'Ü otomatikleştirerek Word 'Ü genişletir. Belirli bir belgeyle ilişkili olan belge düzeyi özelleştirmesinden farklı olarak, bir VSTO eklentisi içinde uyguladığınız işlevsellik tek bir belgeyle sınırlı değildir.

 Word için VSTO eklentisi projesi oluşturmak için, Visual Studio 'nun **Yeni proje** Iletişim kutusundaki Word eklentisi proje şablonlarını kullanın. Daha fazla bilgi için [nasıl yapılır: Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)'da Office projeleri oluşturun.

 VSTO eklentileri nasıl çalıştığı hakkında genel bilgi için bkz. [mimarisi, VSTO eklentileri](../vsto/architecture-of-vsto-add-ins.md).

### <a name="word-add-in-programming-model"></a>Word eklenti programlama modeli
 Word VSTO eklenti projesi oluşturduğunuzda, Visual Studio çözümünüzün temeli olan adlı `ThisAddIn`bir sınıf oluşturur. Bu sınıf, kodunuzun yazılması için bir başlangıç noktası sağlar ve aynı zamanda VSTO eklentinize Word nesne modelini de gösterir.

 VSTO eklentilerinde kullanabileceğiniz `ThisAddIn` sınıf ve diğer özellikler hakkında daha fazla bilgi için bkz. [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md).

## <a name="UI"></a>Word 'ün Kullanıcı arabirimini özelleştirme
 Word 'ün Kullanıcı arabirimini özelleştirmenin birkaç farklı yolu vardır. Bazı seçenekleri tüm proje türleri için kullanılabilir ve diğer seçenekleri yalnızca VSTO eklentileri veya belge düzeyi özelleştirmeleri için kullanılabilir.

### <a name="options-for-all-project-types"></a>Tüm proje türleri için Seçenekler
 Aşağıdaki tabloda, hem belge düzeyi özelleştirmeleri ve VSTO eklentileri için kullanılabilen seçenekleri listeler.

|Görev|Daha fazla bilgi için|
|----------|--------------------------|
|Şeridi özelleştirme.|[Şerite Genel Bakış](../vsto/ribbon-overview.md)|
|Özelleştirilmiş belgeye (belge düzeyi özelleştirmesi için) veya herhangi bir açık belgeye (VSTO eklentisi için) Windows Forms denetimleri veya genişletilmiş sözcük denetimleri ekleyin.|[Nasıl yapılır: Office belgelerine Windows Forms denetimleri ekleme](../vsto/how-to-add-windows-forms-controls-to-office-documents.md)<br /><br /> [Nasıl yapılır: Word belgelerine içerik denetimleri ekleme](../vsto/how-to-add-content-controls-to-word-documents.md)<br /><br /> [Nasıl yapılır: Word belgelerine yer işareti denetimleri ekleme](../vsto/how-to-add-bookmark-controls-to-word-documents.md)|

### <a name="options-for-document-level-customizations"></a>Belge düzeyi özelleştirmeleri seçenekleri
 Aşağıdaki tabloda, yalnızca belge düzeyi özelleştirmeleri tarafından kullanılabilen seçenekleri listeler.

|Görev|Daha fazla bilgi için|
|----------|--------------------------|
|Belgeye bir eylemler bölmesi ekleyin.|[Eylemler bölmesine genel bakış](../vsto/actions-pane-overview.md)<br /><br /> [Nasıl yapılır: Word belgelerine veya Excel çalışma kitaplarına eylemler bölmesi ekleme](../vsto/how-to-add-an-actions-pane-to-word-documents-or-excel-workbooks.md)|
|Belge yüzeyine genişletilmiş XMLNode ve XMLNodes denetimleri ekleyin.|[Nasıl yapılır: Word belgelerine XMLNode denetimleri ekleme](../vsto/how-to-add-xmlnode-controls-to-word-documents.md)<br /><br /> [Nasıl yapılır: Word belgelerine XMLNodes denetimleri ekleme](../vsto/how-to-add-xmlnodes-controls-to-word-documents.md)|

### <a name="options-for-vsto-add-ins"></a>VSTO eklentileri için seçenekleri
 Aşağıdaki tabloda yalnızca VSTO eklentileri için kullanılabilen seçenekleri listeler.

|Görev|Daha fazla bilgi için|
|----------|--------------------------|
|Özel görev bölmesi oluşturun.|[Özel görev bölmeleri](../vsto/custom-task-panes.md)|

### <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[Word nesne modeline genel bakış](../vsto/word-object-model-overview.md)|Word nesne modeli tarafından sağlanan ana türlere genel bir bakış sağlar.|
|[Genişletilmiş nesneleri kullanarak Word 'Ü otomatikleştirme](../vsto/automating-word-by-using-extended-objects.md)|Word çözümlerinde kullanabileceğiniz Genişletilmiş nesneler (tarafından [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]sağlanan) hakkında bilgiler sağlar.|
|[Windows Forms denetimlerine Office belgeleri genel bakış](../vsto/windows-forms-controls-on-office-documents-overview.md)|Word belgelerine nasıl Windows Forms denetimleri ekleyebileceğiniz açıklanmaktadır.|
|[İzlenecek yol: Word için ilk belge düzeyi özelleştirmeyi oluşturma](../vsto/walkthrough-creating-your-first-document-level-customization-for-word.md)|Word için temel bir belge düzeyi özelleştirmesi oluşturmayı gösterir.|
|[İzlenecek yol: Word için ilk VSTO eklentisini oluşturma](../vsto/walkthrough-creating-your-first-vsto-add-in-for-word.md)|Word için temel bir VSTO eklentisinin nasıl oluşturulacağını gösterir.|
|[İzlenecek yol: VSTO eklentisinin çalışma zamanında belgeye denetim ekleme](../vsto/walkthrough-adding-controls-to-a-document-at-run-time-in-a-vsto-add-in.md)|VSTO eklentisi kullanılarak çalışma zamanında bir Windows Forms düğme ve <xref:Microsoft.Office.Tools.Word.RichTextContentControl> bir belgeye nasıl ekleneceğini gösterir.|
|[Office geliştirmede Word 2010](http://go.microsoft.com/fwlink/?LinkId=199020)|Word çözümleri geliştirme (Visual Studio kullanarak Office geliştirmeye özgü değil) hakkındaki makalelere ve başvuru belgelerine bağlantılar sağlar.|
