---
title: Sınıf Tasarımcısı'nı kullanın
ms.date: 05/08/2018
ms.topic: conceptual
f1_keywords:
- vs.classdesigner.diagram
helpviewer_keywords:
- Class Designer [Visual Studio]
- Class Designer, about Class Designer
- types [Visual Studio], viewing
- classes [Visual Studio], viewing
- class designer
ms.assetid: 40ed2c9d-0ce0-4b95-ad78-5dec2065ccea
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ee4910471693a2941ec9548773a2f50e443a639b
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55910746"
---
# <a name="design-and-view-classes-and-types-with-class-designer"></a>Tasarım ve görünüm sınıfları ve Sınıf Tasarımcısı ile türleri

Tasarım, görselleştirin ve sınıfları ve diğer türleri ile kodunuzu yeniden düzenleyin **Sınıf Tasarımcısı** Visual Studio'da. Sınıf diyagramları oluşturmak ve sınıflarda düzenlemek için kullanın, C#, Visual Basic veya C++ projesi. Sınıf diyagramları, kodunuzu yeniden düzenleyin veya Proje yapısı daha iyi anlamak için de kullanabilirsiniz.

## <a name="what-you-can-do-with-class-diagrams"></a>Sınıf diyagramları ile yapabilecekleriniz

- **Tasarım**: Proje kodunuzun sınıf diyagramına düzenleyerek düzenleyin. Yeni öğeler eklemek ve istemediklerinizi silin. Yaptığınız değişiklikleri, kod içinde yansıtılır.

- **Görselleştirme**: Diyagram üzerinde projenizdeki sınıflar görüntüleyerek projenizin yapıyı anlayın. Böylece, en çok önem verdiğiniz proje ayrıntılarını odaklanabilirsiniz diyagramınızı özelleştirin. Diyagram tanıtım veya belge için daha sonra kullanmak üzere kaydedin.

- **Yeniden düzenleme**: Geçersiz kılma yöntemleri, tanımlayıcıları, yeniden düzenleme parametreleri yeniden adlandırın ve arabirimleri ve soyut sınıflar uygular.

## <a name="view-types-and-relationships"></a>Türleri ve ilişkileri görüntüleme

Sınıf diyagramları, türleri, örneğin, bağlı üyeleri ve aralarındaki ilişkilerin ayrıntılarını göster. Bu varlıkların görselleştirme, kodun içine dinamik bir görünümüdür. Bu tasarımcıda türlerini düzenlemek ve yansıtılan varlığın kaynak kodunda yaptığınız düzenlemeleri bakın anlamına gelir. Benzer şekilde, sınıf diyagramı kod dosyalarında yapılan değişiklikler ile eşitlenmiş tutulur.

> [!NOTE]
> Proje türü için yapı kadar sınıf diyagramına bir sınıf diyagramı projenizi içeren ve projeniz başka bir projede bulunan bir türe başvuruyor, başvurulan tür göstermez. Benzer şekilde, bu varlık için projeyi yeniden kadar diyagramda değişiklikler dış varlık için kodu görüntülemez.

## <a name="class-diagram-workflow"></a>Sınıf diyagramı iş akışı

Sınıf diyagramları, projelerin sınıf yapısı anlamanıza yardımcı olabilir. Bu projelerin diğer geliştiriciler tarafından oluşturulmuş olabilir veya kendi başınıza oluşturduğunuz bir projenin tazelemek yeterlidir. Sınıf diyagramlarını özelleştirme, paylaşmak ve başkalarıyla proje bilgi sunmak için kullanabilirsiniz.

Proje bilgileri sunan ilk adımı, göstermek istediğiniz görüntüleyen bir sınıf diyagramı oluşturmaktır. Daha fazla bilgi için [bir sınıf diyagramı eklemek](how-to-add-class-diagrams-to-projects.md). Proje, projenin türü seçilen bir alt veya seçilen üyelerin bir alt kümesini türlerinin ayrı bir görünümünü görüntülemek için kullanılan bir proje için birden fazla sınıf diyagramları oluşturabilirsiniz.

Her sınıf diyagramını gösterir ne tanımlanmasına ek olarak, bilgi sunulan bir şekilde değiştirebilir; Daha fazla bilgi için [nasıl yapılır: Sınıf diyagramlarını özelleştirme](how-to-customize-class-diagrams.md).

Bir veya daha fazla sınıf diyagramları ince ayar sonra Microsoft Office belgelerine kopyalamak ve yazdırmak veya görüntü dosyaları olarak dışarı. Daha fazla bilgi için [nasıl yapılır: Bir Microsoft Office belgesine sınıf diyagramı öğeleri kopyalama](how-to-copy-class-diagram-elements-to-a-microsoft-office-document.md), [nasıl yapılır: Sınıf diyagramlarını yazdırma](how-to-print-class-diagrams.md) ve [nasıl yapılır: Sınıf diyagramlarını görüntü olarak dışarı aktarma](how-to-export-class-diagrams-as-images.md).

> [!NOTE]
> Sınıf Tasarımcısı proje şekilde değiştirilmesi, kaynak dosyalarının konumunu izlemez veya proje kaynak dosyalarında taşımanız, Sınıf Tasarımcısı'nın türü, özellikle kaynak türü bir tür tanımı, temel sınıflar veya ilişki türlerini kaybetmesine neden olabilir. Gibi bir hata alabilirsiniz **Sınıf Tasarımcısı bu türü görüntüleyemiyor**. Bunu yaparsanız, değiştirilmiş ya da yeni yerlerine kaynak kodu yeniden görüntülemek için sınıf diyagramına sürükleyin.

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Düzenleyicisi özellikleri](../writing-code-in-the-code-and-text-editor.md)
- [Çözümlerinizdeki bağımlılıkları eşleme](../../modeling/map-dependencies-across-your-solutions.md)