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
ms.openlocfilehash: f9af25934a40c01c6b4cfd48dcd7419bddf322d3
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65698023"
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
 [Etki alanına özgü dil araçları sözlüğü](https://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)
