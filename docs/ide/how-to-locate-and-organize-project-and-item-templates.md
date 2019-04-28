---
title: Şablonları bulun
ms.date: 01/02/2018
ms.topic: conceptual
helpviewer_keywords:
- project templates [Visual Studio], locations
- item templates [Visual Studio], locations
- template locations [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: db74d23cf42e371f00bf25c7edcd8c480f7649d4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62430282"
---
# <a name="how-to-locate-and-organize-project-and-item-templates"></a>Nasıl yapılır: Proje ve öğe şablonlarını bulma ve düzenleme

Şablon dosyalarını, bunların yeni proje ve yeni öğe iletişim kutularında gösterilen sırada bilinen bir konumda yerleştirilmelidir...

::: moniker range="vs-2017"

Kullanıcı şablonu konumu özel alt kategoriler de oluşturabilirsiniz ve kategorileri gösterilir **yeni proje** ve **Yeni Öğe Ekle** iletişim kutuları.

::: moniker-end

## <a name="locate-templates"></a>Şablonları bulun

Yüklü Şablonlar ve kullanıcı şablonları iki farklı konumlarda depolanır.

### <a name="installed-templates"></a>Yüklü Şablonlar

Visual Studio ile yüklü şablonlar varsayılan olarak bulunur:

::: moniker range="vs-2017"

- *% ProgramFiles(x86) %\\Microsoft Visual Studio\\2017\\\<sürümü >\\Common7\IDE\ProjectTemplates\\< dil\>\\< Yerel ayar kimliği\>*

- *% ProgramFiles(x86) %\\Microsoft Visual Studio\\2017\\\<sürümü > \Common7\IDE\ItemTemplates\\< dil\>\\< yerel ayar kimliği\>*

Örneğin, aşağıdaki dizine Visual Basic öğesi şablonları için İngilizce (LCID 1033) vardır:

*C:\\Program dosyaları (x86)\\Microsoft Visual Studio\\2017\\topluluk\\Common7\\IDE\\öğe şablonları\\VisualBasic\\ 1033*

::: moniker-end

::: moniker range=">=vs-2019"

- *% ProgramFiles(x86) %\\Microsoft Visual Studio\\2019\\\<sürümü >\\Common7\IDE\ProjectTemplates\\< dil\>\\< Yerel ayar kimliği\>*

- *% ProgramFiles(x86) %\\Microsoft Visual Studio\\2019\\\<sürümü > \Common7\IDE\ItemTemplates\\< dil\>\\< yerel ayar kimliği\>*

Örneğin, aşağıdaki dizine Visual Basic öğesi şablonları için İngilizce (LCID 1033) vardır:

*C:\\Program dosyaları (x86)\\Microsoft Visual Studio\\2019\\topluluk\\Common7\\IDE\\öğe şablonları\\VisualBasic\\ 1033*

::: moniker-end

### <a name="user-templates"></a>Kullanıcı Şablonları

Sıkıştırılmış eklerseniz (*.zip*) içeren dosyaya bir *.vstemplate* dosya kullanıcı şablon dizinine şablon yeni proje ve yeni öğe iletişim kutularında görüntülenir. Kullanıcı şablonları varsayılan olarak bulunur:

::: moniker range="vs-2017"

- *%USERPROFILE%\Documents\Visual Studio 2017\Templates\ProjectTemplates*

- *%USERPROFILE%\Documents\Visual Studio 2017\Templates\ItemTemplates*

Örneğin, kullanıcı proje şablonları için aşağıdaki dizine sahip C#:

- *C:\Users\UserName\Documents\Visual Studio 2017\Templates\ProjectTemplates\VisualC#*

::: moniker-end

::: moniker range=">=vs-2019"

- *%USERPROFILE%\Documents\Visual Studio 2019\Templates\ProjectTemplates*

- *%USERPROFILE%\Documents\Visual Studio 2019\Templates\ItemTemplates*

Örneğin, kullanıcı proje şablonları için aşağıdaki dizine sahip C#:

- *C:\Users\UserName\Documents\Visual Studio 2019\Templates\ProjectTemplates\Visual C#*

::: moniker-end

> [!TIP]
> Kullanıcı şablonları için bilinen bir konuma değiştirebilirsiniz **Araçları** > **seçenekleri** > **projeler ve çözümler**  >   **Konumları**.

::: moniker range="vs-2017"

## <a name="organize-templates"></a>Şablon düzenleme

Kategorileri **yeni proje** ve **Yeni Öğe Ekle** iletişim kutuları yüklü şablon ve kullanıcı şablonu konumlarda mevcut dizin yapılarını yansıtır. Kullanıcı şablonu dizine yeni klasörler ekleyerek kullanıcı şablonları kendi kategoriler halinde düzenlenebilir. **Yeni proje** ve **Yeni Öğe Ekle** iletişim kutuları, kullanıcı şablonu kategorilere yaptığınız herhangi bir değişiklik gösterir.

> [!NOTE]
> Yeni bir kategori programlama dili düzeyinde oluşturulamıyor. Yeni kategori her bir dilin yalnızca oluşturulabilir.

### <a name="create-new-user-project-template-categories"></a>Yeni kullanıcı proje şablonu kategorileri oluşturma

1. Kullanıcı proje şablonu dizini programlama dili klasörde bir klasör oluşturun. Örneğin, kurmak için bir **HelloWorld** kategorisi için C# proje şablonları, şu dizin oluşturma:

    - *\%USERPROFILE%\Documents\Visual Studio \<sürüm\>\Templates\ProjectTemplates\Visual C#\HelloWorld*

1. Bu kategori için tüm şablonları yeni klasöre yerleştirin.

1. Üzerinde **dosya** menüsünde seçin **yeni** > **proje**.

   **HelloWorld** kategorisi görünür **yeni proje** iletişim kutusunun **yüklü** > **Visual C#** .

### <a name="create-new-user-item-template-categories"></a>Yeni kullanıcı öğe şablonu kategorileri oluşturma

1. Kullanıcı öğesi şablon dizini programlama dili klasörde bir klasör oluşturun. Örneğin, kurmak için bir **HelloWorld** kategorisi için C# öğe şablonları, şu dizin oluşturma:

    - *\%USERPROFILE%\Documents\Visual Studio \<sürüm\>\Templates\ItemTemplates\Visual C#\HelloWorld*

1. Bu kategori için tüm şablonları yeni klasöre yerleştirin.

1. Bir proje oluşturun veya varolan bir projeyi açın. Ardından **proje** menüsünde seçin **Yeni Öğe Ekle**.

   **HelloWorld** kategorisi görünür **Yeni Öğe Ekle** iletişim kutusunun **yüklü** > **Visual C# öğeleri**.

### <a name="display-templates-in-parent-categories"></a>Üst kategoriler görüntüleme şablonları

Alt kategoriler kullanarak kendi üst kategorilerde görüntülenecek şablonlarında etkinleştirebilirsiniz `NumberOfParentCategoriesToRollUp` öğesinde *.vstemplate* dosya. Bu adımları proje şablonları ve öğe şablonları ile aynıdır.

1. Bulun *.zip* şablonu içeren dosya.

1. Ayıklama *.zip* dosya.

1. Açık *.vstemplate* dosyasını Visual Studio'da.

1. İçinde `TemplateData` öğe, Ekle bir `NumberOfParentCategoriesToRollUp` öğesi. Örneğin, aşağıdaki kodu, üst kategori görünür, ancak bundan daha yüksek şablonu sağlar.

    ```xml
    <TemplateData>
        ...
        <NumberOfParentCategoriesToRollUp>
            1
        </NumberOfParentCategoriesToRollUp>
        ...
    </TemplateData>
    ```

1. Kaydet ve Kapat *.vstemplate* dosya.

1. Şablonunuzda dosyaları seçin, seçime sağ tıklayın ve seçin **göndermek** > **sıkıştırılmış (daraltılmış) klasör**.

   Dosyalar sıkıştırılmadan bir *.zip* dosya.

1. Ayıklanan şablon dosyalarını ve eski şablonu silmek *.zip* dosya.

1. Yeni put *.zip* silinmiş olan dizinindeki *.zip* dosya.

::: moniker-end

## <a name="see-also"></a>Ayrıca bkz.

- [Şablonları özelleştirme](../ide/customizing-project-and-item-templates.md)
- [Visual Studio Şablon Şeması Başvurusu (genişletilebilirlik)](../extensibility/visual-studio-template-schema-reference.md)
- [NumberOfParentCategoriesToRollUp (Visual Studio şablonları)](../extensibility/numberofparentcategoriestorollup-visual-studio-templates.md)
- [Nasıl yapılır: Proje şablonları oluşturma](../ide/how-to-create-project-templates.md)
- [Nasıl yapılır: Öğe şablonları oluşturma](../ide/how-to-create-item-templates.md)