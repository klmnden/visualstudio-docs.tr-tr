---
title: 'Nasıl Yapılır: Varolan türleri görüntüleme (Sınıf Tasarımcısı)'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: conceptual
f1_keywords:
- vs.classdesigner.CannotShowBaseType
helpviewer_keywords:
- types [Visual Studio], visualizing
- types [Visual Studio], class diagrams
- class diagrams, types
ms.assetid: de110a4e-5b51-4a40-9dee-615df4d8f999
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 16e1c31585296913647b5c3d641126c3abca22a8
ms.sourcegitcommit: 935e341a02dba1c2aa3b6e89469388aa6e626f7f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53684450"
---
# <a name="how-to-view-existing-types-in-class-designer"></a>Nasıl Yapılır: Sınıf Tasarımcısı'nda varolan türleri görüntüleme

Varolan bir türünü ve üyelerini görmek için bir sınıf diyagramına şeklini ekleyin.

Yerel ve başvurulan türleri görebilirsiniz. Yerel bir tür o anda açık olan projede mevcuttur ve okunur/yazılır. Başvurulan tür başka bir projede ya da başvurulan bir derlemede bulunur ve salt okunur özelliktedir.

Sınıf diyagramları üzerinde yeni türleri tasarımı için bkz: [nasıl yapılır: Sınıf Tasarımcısı kullanarak tür oluşturma](how-to-create-types.md).

## <a name="to-see-types-in-a-project-on-a-class-diagram"></a>Projedeki türleri bir sınıf diyagramı üzerinde görmek için

1.  İçinde bir projeden **Çözüm Gezgini**, var olan bir sınıf diyagramı (.cd) dosyası açın. Ya da hiçbir sınıf diyagramı yoksa, projeye yeni bir sınıf diyagramı ekleyin. Bkz: [nasıl yapılır: Projelere sınıf diyagramları ekleme](how-to-add-class-diagrams-to-projects.md).

2.  Projesi ile **Çözüm Gezgini**, bir kaynak kodu dosyasını sınıf diyagramına sürükleyin.

    > [!NOTE]
    > Çözümünüz birden fazla uygulama kod paylaşan bir proje varsa, bir sınıf diyagramına dosyaları veya kodu yalnızca şu kaynaklardan sürükleyebilirsiniz:
    >
    > - Diyagramı içeren uygulama projesi
    > - Uygulama projesi tarafından içeri aktarılan bir paylaşılan proje
    > - Başvurulan bir proje
    > - Bir derleme

    Kaynak kodu dosyasında tanımlı türleri temsil eden şekiller, diyagram üzerinde dosyayı sürüklediğiniz konumda görünür.

Proje düğümünden bir veya daha fazla türleri sürükleyerek projedeki türleri görüntüleyebilirsiniz **sınıf görünümü** sınıf diyagramına.

> [!TIP]
> Varsa **sınıf görünümü** açık, açık olmayan **sınıf görünümü** gelen **görünümü** menüsü.

Türleri diyagram üzerinde varsayılan konumlarda görüntülemek için bir veya daha fazla türleri seçin **sınıf görünümü**, seçili türlere sağ tıklayın ve seçme **sınıf diyagramını görüntüle**.

> [!NOTE]
> Türü içeren bir kapalı sınıf diyagramı projede zaten varsa, sınıf diyagramı açılarak tür şeklini görüntüler. Ancak, hiçbir sınıf diyagramı içeren projede türü var **Sınıf Tasarımcısı** projede yeni bir sınıf diyagramı oluşturur ve görüntü türü için açar.

Bir türü diyagram üzerinde ilk kez görüntülediğinizde, bu türe ait şekil varsayılan olarak daraltılmış görünür. Şekli genişleterek içeriğini görüntüleyebilirsiniz.

### <a name="to-display-the-contents-of-a-project-in-a-class-diagram"></a>Bir sınıf diyagramında bir projeyi içeriğini görüntülemek için

İçinde **Çözüm Gezgini** veya **sınıf görünümü**, projeye sağ tıklayıp seçin **görünümü**, ardından **sınıf diyagramını görüntüle**. Otomatik olarak doldurulan bir Sınıf Diyagramı oluşturulur.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Türler arasında devralmayı görüntüleme](how-to-view-inheritance-between-types.md)
- [Nasıl yapılır: Sınıf diyagramlarını özelleştirme](how-to-customize-class-diagrams.md)
- [Türleri ve İlişkileri Görüntüleme](designing-and-viewing-classes-and-types.md)