---
title: 'Nasıl Yapılır: Bir Öğede CLR Özniteliklerini Ayarlama'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.dsltools.EditAttributesDialog
helpviewer_keywords:
- Domain-Specific Language, custom attrributes
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: 5b9a96f70febc6a33d80557a09cc8bc8e1adf2f4
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53938088"
---
# <a name="how-to-set-clr-attributes-on-an-element"></a>Nasıl Yapılır: Bir Öğede CLR Özniteliklerini Ayarlama
Özel öznitelikler, etki alanı öğeleri, şekiller, bağlayıcılar ve diyagramları için eklenen özel öznitelikler bağlıdır. Devralınan herhangi bir öznitelik ekleyebilirsiniz `System.Attribute` sınıfı.

### <a name="to-add-a-custom-attribute"></a>Özel bir öznitelik eklemek için

1.  İçinde **DSL Gezgini**, özel bir öznitelik eklemek istediğiniz öğeyi seçin.

2.  İçinde **özellikleri** penceresi, sonraki **özel öznitelikler** özelliği, Gözat'a tıklayın (**...** ) simgesi.

     **Düğmeye tıklandığında öznitelikleri Düzenle** iletişim kutusu açılır.

3.  İçinde **adı** sütun tıklayın  **\<öznitelik Ekle >** , öznitelik adı yazın. ENTER tuşuna basın.

4.  Öznitelik adı altında satırın parantez gösterir. Parametre türü özniteliği için bu satıra yazın (örneğin, `string`), ve ardından ENTER tuşuna basın.

5.  İçinde **Name özelliği** sütun, uygun bir ad yazın örneğin, `MyString`.

6.  **Tamam**'ı tıklatın.

     **Özel öznitelikler** özelliği artık şu biçimde öznitelik görüntüler:

     `[` *AttributeName* `(` *ParameterName* `=` *türü* `)]`

## <a name="see-also"></a>Ayrıca Bkz.

- [Etki alanına özgü dil araçları sözlüğü](https://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)