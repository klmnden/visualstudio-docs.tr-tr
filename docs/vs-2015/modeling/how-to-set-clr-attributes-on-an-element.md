---
title: 'Nasıl yapılır: Bir öğede CLR özniteliklerini ayarlama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
f1_keywords:
- vs.dsltools.EditAttributesDialog
helpviewer_keywords:
- Domain-Specific Language, custom attrributes
ms.assetid: b3db3c74-920c-4701-9544-6f75cbe8b7c9
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 54c3bd854f824818d9656a33ccf30391f750a491
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60080728"
---
# <a name="how-to-set-clr-attributes-on-an-element"></a>Nasıl yapılır: Bir Öğede CLR Özniteliklerini Ayarlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Özel öznitelikler, etki alanı öğeleri, şekiller, bağlayıcılar ve diyagramları için eklenen özel öznitelikler bağlıdır. Devralınan herhangi bir öznitelik ekleyebilirsiniz `System.Attribute` sınıfı.  
  
### <a name="to-add-a-custom-attribute"></a>Özel bir öznitelik eklemek için  
  
1. İçinde **DSL Gezgini**, özel bir öznitelik eklemek istediğiniz öğeyi seçin.  
  
2. İçinde **özellikleri** penceresi, sonraki **özel öznitelikler** özelliği, Gözat'a tıklayın (**...** ) simgesi.  
  
     **Düğmeye tıklandığında öznitelikleri Düzenle** iletişim kutusu açılır.  
  
3. İçinde **adı** sütun tıklayın  **\<öznitelik Ekle >** , öznitelik adı yazın. Press ENTER.  
  
4. Öznitelik adı altında satırın parantez gösterir. Parametre türü özniteliği için bu satıra yazın (örneğin, `string`), ve ardından ENTER tuşuna basın.  
  
5. İçinde **Name özelliği** sütun, uygun bir ad yazın örneğin, `MyString`.  
  
6. **Tamam**'ı tıklatın.  
  
     **Özel öznitelikler** özelliği artık şu biçimde öznitelik görüntüler:  
  
     `[` *AttributeName* `(` *ParameterName* `=` *türü* `)]`  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etki alanına özgü dil araçları sözlüğü](http://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)
