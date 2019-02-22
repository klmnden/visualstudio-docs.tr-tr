---
title: Yeni Proje iletişim kutusuna dizin ekleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- New Project dialog box, extending
ms.assetid: 53b328f5-20bb-49a3-bf9e-1818f4fbdf50
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9d8e68413795b7004542ee312dcb27492e55e7f0
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56626199"
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