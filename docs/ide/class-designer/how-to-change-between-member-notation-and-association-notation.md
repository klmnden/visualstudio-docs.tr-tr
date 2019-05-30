---
title: Üye & ilişkilendirme gösterimi (Sınıf Tasarımcısı) arasında değiştirme
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- notation, member
- association notation
- member notation
- notation, association
ms.assetid: 65881c5a-d251-4a36-ad0d-73d088436092
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 17bda235f0fb5781b19a3b1384b86ae58543edf3
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66261208"
---
# <a name="how-to-change-between-member-notation-and-association-notation-in-class-designer"></a>Nasıl yapılır: Üye gösterimi ile ilişkilendirme gösterimi arasında sınıf tasarımcısında değiştirme

İçinde **Sınıf Tasarımcısı**, sınıf diyagramı temsil eden iki türden ilişkilendirme gösterimi ve bunun tersi de üye gösterimi arasında bir ilişkilendirme ilişkisi şeklini değiştirebilirsiniz. Üyeleri ilişkilendirme çizgileri genellikle görüntülenen türleri nasıl ilişkili olduğunu, kullanışlı bir görselleştirme sağlar.

> [!NOTE]
> İlişkilendirme ilişkileri bir üye özelliği veya alanı gösterilebilir. Üye gösterimi ilişkilendirme gösterimi değiştirmek için bir tür, başka bir tür üyesi olmalıdır. Üye gösterimi ilişkilendirme gösterimi değiştirmek için iki tür tarafından bir ilişkilendirme çizgisi bağlanması gerekir. Daha fazla bilgi için [nasıl yapılır: İlişkilendirme bBetween türleri oluşturma](how-to-create-associations-between-types.md). Projenizi içeren birden fazla sınıf diyagramı, diyagram ilişkilendirme ilişkileri görüntüler şekilde yaptığınız değişiklikler yalnızca o diyagramı etkiler. Başka bir diyagrama ilişkilendirme ilişkileri görüntüleme biçimini değiştirmek için açın veya bu diyagramı görüntüleyin ve aşağıdaki adımları gerçekleştirin.

## <a name="to-change-member-notation-to-association-notation"></a>Üye gösterimi ilişkilendirme gösterimi değiştirmek için

1. Çözüm Gezgini'nde proje düğümü aracılığıyla, sınıf diyagramı (.cd) dosyası açın.

2. Üye özellik veya alan ilişkisini temsil eden içinde tür şeklini sınıf diyagramı'nda, sağ tıklatın ve seçin **ilişkilendirmesi olarak göster**.

    > [!TIP]
    > Hiçbir özelliklerle veya alanlarla türü şeklinde görünür durumdaysa, bölmeleri şeklinde daraltılmış olabilir. Tür şeklini genişletmek için bölme adına çift tıklayın veya türü şekle sağ tıklayın ve seçin **genişletme**.

    Bölme türü şeklinde üyenin kaybolur ve iki tür bağlanmak için bir ilişkilendirme çizgisi görüntülenir. İlişkilendirme çizgisi, özelliği veya alanı adıyla etiketlenir.

## <a name="to-change-association-notation-to-member-notation"></a>Üye gösterimi ilişkilendirme gösterimi değiştirmek için

Sınıf diyagramı'nda ilişkilendirme çizgisi sağ tıklatın ve seçin **Göster özelliği olarak** veya **alan olarak göster** uygun şekilde. İlişkilendirme çizgisi kaybolur, ve tür şeklini diyagramda içinde uygun bölme özelliği görüntülenir.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Türler arasında devralma oluşturma](how-to-create-inheritance-between-types.md)
- [Nasıl yapılır: Türler arasında devralmayı görüntüleme](how-to-view-inheritance-between-types.md)
- [Türleri ve İlişkileri Görüntüleme](designing-and-viewing-classes-and-types.md)
- [Nasıl yapılır: Koleksiyon ilişkilendirmesini Görselleştirme](how-to-visualize-a-collection-association.md)