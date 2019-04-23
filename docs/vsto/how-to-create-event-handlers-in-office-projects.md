---
title: 'Nasıl yapılır: Office projelerinde olay işleyicileri oluşturma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Visual Basic [Office development in Visual Studio], event handlers
- event handlers [Office development in Visual Studio]
- Visual C# [Office development in Visual Studio], event handlers
- events [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 577b12be220e2a695609db6c508d7aaf69c79f92
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60054527"
---
# <a name="how-to-create-event-handlers-in-office-projects"></a>Nasıl yapılır: Office projelerinde olay işleyicileri oluşturma
  Visual Basic'te olay işleyicileri oluşturmanın birkaç yolu vardır ve C#. Tasarım görünümünde, varsayılan olay işleyicileri denetimleri için denetimi çift tıklayarak oluşturabilir, veya olayları bölmesini kullanarak **özellikleri** herhangi bir olay işleyicileri denetimi oluşturmak için pencere. Ancak, kod Görünümü'nde, bir olay işleyicisi oluşturmak için Tasarım görünümüne geçiş yapmak istemeyebilirsiniz.

 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]

 [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]

### <a name="to-create-an-event-handler-in-visual-basic"></a>Visual Basic'te bir olay işleyicisi oluşturmak için

1. Gelen **sınıf adı** Kod Düzenleyicisi'nin üst aşağı açılan listesinde, istediğiniz nesneyi seçin için bir olay işleyicisi oluşturun.

    > [!NOTE]
    >  Olay işleyicileri oluşturmak istiyorsanız `ThisDocument` veya `ThisWorkbook`, seçmelisiniz **(ThisDocument olayları)** veya **(ThisWorkbook olayları)** içinde **sınıf adı**aşağı açılan listesi

2. Gelen **yöntem adı** açılır listede Kod Düzenleyicisi'nin en üstünde, olayı seçin.

     Visual Studio, olay işleyicisi oluşturur ve yeni oluşturulan olay işleyicisi ekleme noktasını taşır. Olay işleyicisi zaten varsa, ekleme noktasını varolan olay işleyicisine taşır.

### <a name="to-create-an-event-handler-in-c"></a>C dilinde bir olay işleyicisi oluşturmak için\#

1. Olay temsilcisini oluşturmak **başlangıç** olay sınıfının ardından bir boşluk tam olay adını yazarak ve ardından yazarak **+=** ardından boşluk. Örneğin:

     `this.<object name>.<event name> +=`

2. Kod satırının sonunda iki kez SEKME tuşuna basın.

     Visual Studio otomatik olarak kod satırının tamamlanır, olay işleyicisi oluşturur ve yeni oluşturulan olay işleyicisi ekleme noktasını taşır.

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümlerinde kod yazma](../vsto/writing-code-in-office-solutions.md)
- [İzlenecek yol: NamedRange denetimi olaylarına karşı programlama](../vsto/walkthrough-programming-against-events-of-a-namedrange-control.md)
- [Office çözümleri oluşturun](../vsto/building-office-solutions.md)
