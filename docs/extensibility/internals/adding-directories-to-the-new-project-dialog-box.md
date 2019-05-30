---
title: Yeni Proje iletişim kutusuna dizin ekleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- New Project dialog box, extending
ms.assetid: 53b328f5-20bb-49a3-bf9e-1818f4fbdf50
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5e81d09c2a4e97ca5f3da112e593b04b219e6314
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66328001"
---
# <a name="add-directories-to-the-new-project-dialog-box"></a>Yeni Proje iletişim kutusuna dizin ekleme
Yeni proje türleri oluşturduğunuzda, yeni bir dizin de kaydedebilirsiniz **yeni proje** şablon olarak kullanmak için bunları görüntülemek için iletişim kutusu. Aşağıdaki kod örneği, bir düğüm olarak da bilinen yeni bir dizin kaydedilecek açıklanmaktadır. Örnekte, VSPackage tarafından kullanıma sunulan şablonları *CLSID_Package*, kayıtlı. Sonuç olarak, sol tarafındaki **yeni proje** iletişim kutusu sunar eklenen düğümü tarafından belirlenen bir adla *Folder_Label_ResID* kaynak. Bu kaynak VSPackage uydu DLL yüklenir.

 **Klasör** değeri temsil eden bir klasörün altında çalışacağı bir GUID *Folder_Label_ResID* düğümünde görüntülenir. Örnekte, GUID'i temsil **diğer projeleri** klasöründe **proje türleri** bölmesinde **yeni proje** iletişim kutusu. Varsa **diğer projeleri** değeri yok, en üst düzeyinde etiketi konumlandırıldı.

 `TemplatesDir` Değer proje şablonları içeren dizinin tam yolunu belirtir. Bu dosyalar olabilir *.vsz* veya kopyalamak için tipik bir şablon dosyaları.

 Belirtirseniz `TemplatesLocalizedSubDir`, kaynak Kimliğini alt adları bir dize olmalıdır `TemplatesDir` , yerelleştirilmiş şablonları içerir. Çünkü [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] dize kaynağını yükler, yoksa bir uydu DLL farklı bir alt dizin adı her uydu DLL içerebilir. `SortPriority` Değer sıralama önceliği belirtir.

```
NoRemove NewProjectTemplates
{
    NoRemove TemplateDirs
  {
    ForceRemove %CLSID_Package%
    {
      ForceRemove /1 = s '#%Folder_Label_ResID%'
      {
        val Folder = s '{DCF2A94A-45B0-11D1-ADBF-00C04FB6BE4C}'
        val TemplatesDir = s '%Template_Path%'
        val TemplatesLocalizedSubDir = s '#100'
        val SortPriority = d 1000
      }
    }
  }
}
```

## <a name="see-also"></a>Ayrıca bkz.
- [Proje ve öğe şablonlarını kaydetme](../../extensibility/internals/registering-project-and-item-templates.md)
- [Yeni Öğe Ekle iletişim kutusu öğeleri Ekle](../../extensibility/internals/adding-items-to-the-add-new-item-dialog-boxes.md)
- [Yeni Öğe Ekle iletişim kutusuna dizin ekleme](../../extensibility/internals/adding-directories-to-the-add-new-item-dialog-box.md)