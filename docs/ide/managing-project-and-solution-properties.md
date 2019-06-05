---
title: Proje ve çözüm özelliklerini yönetme
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a3d5b1150c67eeb5d47741ed9331dcdc11a82582
ms.sourcegitcommit: 5483e399f14fb01f528b3b194474778fd6f59fa6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/05/2019
ms.locfileid: "66714948"
---
# <a name="manage-project-and-solution-properties"></a>Proje ve çözüm özelliklerini yönetme

Proje derleme, hata ayıklama, test etme ve dağıtma birçok yönüyle yönetir özelliklere sahiptir. Bazı özellikler tüm proje türleri arasında ortak olan ve belirli dillerde veya platformlarda için benzersiz bazılarıdır. Proje Özellikleri'nde proje düğümüne sağ tıklayarak erişim **Çözüm Gezgini** seçip **özellikleri** veya yazarak **özellikleri** kartındaki arama kutusuna menü çubuğu ve seçme **Özellikler penceresi** sonuçlarından.

![Proje bağlam menüsü](../ide/media/vs2015_proj_prop_menu.gif)

.NET projelerine proje ağacında, kendisini özellikler düğümü sahip olabilir.

![Çözüm Gezgini ağacındaki özellikler düğümü](../ide/media/vs2015_props_se.png)

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [çözüm ve proje özelliklerini (Mac için Visual Studio) yönetme](/visualstudio/mac/managing-solutions-and-project-properties).

## <a name="project-properties"></a>Proje Özellikleri

Proje Özellikleri gruplar halinde düzenlenir ve her grubun kendi özellik sayfası vardır. Sayfalar, farklı diller ve proje türleri için farklı olabilir.

### <a name="c-visual-basic-and-f-projects"></a>C#, Visual Basic ve F# projeleri

İçinde C#, Visual Basic ve F# projeleri özellikleri içinde sunulur **Proje Tasarımcısı**. Aşağıdaki çizimde gösterildiği **derleme** bir WPF projesi özellik sayfasında C#:

![Visual Studio Proje Tasarımcısı](../ide/media/vs2015_proppage_build.png)

Her özellik sayfaları'nda hakkında bilgi için **Proje Tasarımcısı**, bkz: [proje özellikleri başvurusu](../ide/reference/project-properties-reference.md).

> [!TIP]
> Çözüm birkaç özellik vardır ve bu nedenle proje öğeleri; Bu özelliklere erişir [Özellikler penceresi](../ide/reference/properties-window.md)değil **Proje Tasarımcısı**.

### <a name="c-and-javascript-projects"></a>C++ ve JavaScript projeleri

C++ ve JavaScript projeleri, proje özelliklerini yönetmek için farklı kullanıcı arabirimi vardır. Bu resimde C++ proje özellik sayfası (JavaScript sayfaları benzer):

![Visual C&#43; &#43; proje özellikleri](../ide/media/vs2015_projprops_cpp.png)

C++ proje özellikleri hakkında daha fazla bilgi için bkz. [(C++) proje özellikleriyle çalışma](/cpp/build/working-with-project-properties). JavaScript özellikleri hakkında daha fazla bilgi için bkz. [özellik sayfaları, JavaScript](../ide/reference/property-pages-javascript.md).

## <a name="solution-properties"></a>Çözüm özellikleri

Çözümdeki özelliklere erişmek için sağ ndeki çözüm düğümüne tıklayın **Çözüm Gezgini** ve **özellikleri**. İletişim kutusunda, proje yapılandırmaları için ayarlanmış **hata ayıklama** veya **yayın** yapıları seçin hangi projelerin başlangıç olmalıdır ne zaman proje **F5** basılı ve kod ayarlayın Çözümleme seçenekleri.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da projeler ve çözümler](../ide/solutions-and-projects-in-visual-studio.md)
- [Çözüm ve proje özelliklerini (Mac için Visual Studio) yönetme](/visualstudio/mac/managing-solutions-and-project-properties)
