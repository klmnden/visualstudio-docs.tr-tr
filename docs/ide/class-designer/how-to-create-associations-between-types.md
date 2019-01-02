---
title: 'Nasıl Yapılır: (Sınıf Tasarımcısı) türler arasında ilişkilendirme oluşturma'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
- vs.classdesigner.associationline
helpviewer_keywords:
- types [Visual Studio], associations
- association lines, defining (Class Designer)
- defining association lines (Class Designer)
- associations, types
- association lines
ms.assetid: adccb9c8-2f8a-4086-9fa9-f70f99fb6e00
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 77f957e112835c138a84accbdc7070f1217fc963
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53916607"
---
# <a name="how-to-create-associations-between-types-in-class-designer"></a>Nasıl Yapılır: Sınıf tasarımcısında türler arasında ilişkilendirme oluşturma

İlişkilendirme satırları **Sınıf Tasarımcısı** bir diyagramdaki sınıfların nasıl ilişkili olduğunu gösterir. İlişkilendirme çizgisi, projenizdeki başka bir sınıfın özellik veya alan türü olan bir sınıfı temsil eder. İlişkilendirme çizgileri genellikle, projenizdeki sınıflar arasında en önemli ilişkileri göstermek için kullanılır.

Tüm alanları ve özellikleri ilişkilendirmeler halinde görüntüleyebilirsiniz; bununla birlikte diyagramda vurgulamak istediğiniz unsura bağlı olarak yalnızca önemli üyeleri ilişkilendirme olarak göstermek daha anlamlı olur. (Daha az önemli üyeleri normal üye olarak gösterebilir veya bütünüyle gizleyebilirsiniz.)

> [!NOTE]
> **Sınıf Tasarımcısı** yalnızca tek yönlü ilişkilendirmeleri destekler.

## <a name="to-define-an-association-line-in-the-class-diagram"></a>Sınıf Diyagramı'nda bir ilişkilendirme çizgisi tanımlamak için

1. Araç Kutusu'nda, altında **Sınıf Tasarımcısı**seçin **ilişkilendirme**.

2. İlişkilendirme ile bağlamak istediğiniz iki şekil arasına bir çizgi çizin.

     İlk sınıfta yeni bir özellik oluşturulur. Bu özellik varsayılan ada sahip bir ilişkilendirme çizgisi görüntüler (şekildeki bir bölme içinde özellik olarak değil). Türü ise, ilişkilendirme çizgisinin işaret ettiği şekildir.

## <a name="to-change-the-name-of-an-association"></a>İlişkilendirmenin adını değiştirmek için

Diyagram yüzeyinde ilişkilendirme çizgisinin etiketine tıklayın ve etiketi düzenleyin.

Alternatif olarak, aşağıdaki adımları izleyin:

1. İlişkilendirme olarak gösterilen özelliği içeren şekle seçin.

   Şekil odağı alır ve üyeleri görüntülemek **sınıf ayrıntıları** ve **özellikleri** windows.

2. Her ikisinde **sınıf ayrıntıları** veya **özellikleri** penceresinde, bu özellik ve ENTER tuşuna için ad alanını Düzenle **Enter**.

   Adı güncelleştirilmiştir **sınıf ayrıntıları** penceresinde, ilişkilendirme satır **özellikleri** penceresinde ve kod.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Üye gösterimi ile ilişkilendirme gösterimi arasında geçiş](how-to-change-between-member-notation-and-association-notation.md)
