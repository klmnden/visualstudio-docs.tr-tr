---
title: Proje ve öğe şablonlarını Name parametreleri ekleme
ms.date: 01/02/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- template parameters
- template parameters, substituting
- Visual Studio templates, using parameters
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: fa06783acf3feaa863b788c3c0b976b0c762d0c8
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53986914"
---
# <a name="how-to-substitute-parameters-in-a-template"></a>Nasıl Yapılır: Bir şablonda parametreleri ikame etme

Şablon parametreleri bir şablondan bir dosya oluşturulduğunda tanımlayıcıları sınıf adları ve ad alanları gibi değiştirmenizi sağlar. Şablon parametreleri için var olan şablonları ekleyin veya şablon parametreleri ile kendi şablonlarınızı oluşturabilirsiniz.

Şablon parametreleri biçimi $ yazılır*parametre*$. Şablon parametreleri tam bir listesi için bkz. [şablon parametreleri](../ide/template-parameters.md).

Aşağıdaki bölümde "güvenli proje adı" ile bir ad alanı adını değiştirmek için bir şablonu nasıl değiştireceğiniz gösterilmektedir.

## <a name="to-use-a-parameter-to-replace-the-namespace-name"></a>Ad alanı adı değiştirmek için bir parametre kullanmak için

1. Bir veya daha fazla kod dosyaları şablonda parametre ekleyin. Örneğin:

    ```csharp
    namespace $safeprojectname$
    ```

1. İçinde *vstemplate* dosya şablonu, bulun `ProjectItem` bu dosyayı içeren öğe.

1. Ayarlama `ReplaceParameters` özniteliğini `true` için `ProjectItem` öğesi:

    ```xml
    <ProjectItem ReplaceParameters="true">Class1.cs</ProjectItem>
    ```

## <a name="see-also"></a>Ayrıca bkz.

- [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)
- [Şablon parametreleri](../ide/template-parameters.md)
- [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)
- [ProjectItem öğesi (Visual Studio öğe şablonları)](../extensibility/projectitem-element-visual-studio-item-templates.md)