---
title: Mevcut proje öğesi şablonları güncelleştirme
ms.date: 01/02/2018
ms.topic: conceptual
helpviewer_keywords:
- item templates, updating
- Visual Studio templates, updating
- project templates, updating
- updating templates [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 57e457224d47e278df169b931c6e9cf6b8ae25e1
ms.sourcegitcommit: 3201da3499051768ab59f492699a9049cbc5c3c6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/22/2019
ms.locfileid: "58355396"
---
# <a name="how-to-update-existing-templates"></a>Nasıl yapılır: Mevcut şablonları güncelleştirme

Bir şablon oluşturmak ve içine dosyaları sıkıştır sonra bir *.zip* dosyası şablonu değiştirmek isteyebilirsiniz. Şablon dosyaları el ile değiştirerek veya yeni bir şablonu dışarı aktarma şablonu temel alan bir projeden bunu yapabilirsiniz.

## <a name="use-the-export-template-wizard"></a>Şablonu Dışarı Aktarma Sihirbazı'nı kullanma

Visual Studio sağlar bir **şablonu Dışarı Aktarma Sihirbazı** mevcut bir şablonu güncellemek için kullanılabilir:

1. Seçin **dosya** > **yeni** > **proje** menü çubuğundan.

1. Güncelleştirme ve yeni proje oluşturma adımlarında size devam etmek için kullanmak istediğiniz şablonu seçin.

1. Visual Studio'da proje değiştirin. Örneğin, çıktı türünü değiştirin veya yeni bir dosya projeye ekleyin.

1. Üzerinde **proje** menüsünde seçin **şablonu dışarı aktar**.

    **Şablonu Dışarı Aktarma Sihirbazı** açılır.

1. Şablon olarak dışarı aktarmak için sihirbazdaki istemleri izleyerek bir *.zip* dosya.

1. (İsteğe bağlı) Bir yerde *.zip* dosyası aşağıdaki dizinde: *%USERPROFILE%\Documents\Visual Studio \<sürüm\>\Templates\ProjectTemplates* için kullanılabilir hale getirmek için Seçimi. Seçeneğini seçmediyseniz, bu adımı gerçekleştirmeniz gerekecektir **otomatik olarak şablonu Visual Studio'ya içeri aktarma** içinde **şablonu Dışarı Aktarma Sihirbazı**.

1. Eski Şablonu Sil *.zip* dosya.

## <a name="manually-update-an-existing-template"></a>Mevcut bir şablonu el ile güncelleştirme

Mevcut bir şablonu kullanmadan güncelleştirebilirsiniz **şablonu Dışarı Aktarma Sihirbazı**, sıkıştırılmış dosyalarda değiştirerek *.zip* dosya.

### <a name="to-manually-update-an-existing-template"></a>Mevcut bir şablonu el ile güncelleştirmek için

1. Bulun *.zip* şablonu içeren dosya. Kullanıcı proje şablonları konumu *%USERPROFILE%\Documents\Visual Studio \<sürüm\>\Templates\ProjectTemplates*.

1. Ayıklama *.zip* dosya.

1. Değiştirmek ya da geçerli şablon dosyaları silin veya şablona yeni dosyalar ekleyin.

1. Açık, değiştirebilir ve Kaydet *.vstemplate* güncelleştirilmiş davranışı ya da yeni dosyaları işlemek için XML dosyası.

    Hakkında daha fazla bilgi için *.vstemplate* şema bakın [Visual Studio Şablon Şeması Başvurusu (genişletilebilirlik)](../extensibility/visual-studio-template-schema-reference.md). Kaynak dosyalarında parametreleştirebilirsiniz hakkında daha fazla bilgi için bkz. [şablon parametreleri](../ide/template-parameters.md).

1. Dosyaları şablonunuzdaki ve sağ tıklayın veya bağlam menüsünü seçin ve seçin **göndermek** > **sıkıştırılmış (daraltılmış) klasör**.

    Seçtiğiniz dosyalar sıkıştırılmadan bir *.zip* dosya.

1. Yeni put *.zip* eski ile aynı dizinde dosya *.zip* dosya.

1. Ayıklanan şablon dosyalarını ve eski şablonu silmek *.zip* dosya.

## <a name="see-also"></a>Ayrıca bkz.

- [Şablonları özelleştirme](../ide/customizing-project-and-item-templates.md)
- [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)
- [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)
- [Şablon parametreleri](../ide/template-parameters.md)