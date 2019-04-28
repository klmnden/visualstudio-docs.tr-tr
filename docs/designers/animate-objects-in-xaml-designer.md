---
title: XAML Tasarımcısı’nda nesnelere animasyon ekleme
ms.date: 04/11/2018
ms.topic: conceptual
ms.assetid: fb88fa26-e835-47f5-9771-2f279441c83c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- uwp
ms.openlocfilehash: a5bd9c24351201d066f9055554468939df02b33e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62927042"
---
# <a name="animate-objects-in-xaml-designer"></a>XAML Tasarımcısı’nda nesnelere animasyon ekleme

Nesneleri taşıma kısa animasyonlar oluşturma veya içeri ve dışarı Soldurma.

Başlamak için oluşturun bir *film şeridi*. Bir veya daha fazla görsel taslak içeren *zaman çizelgeleri*. Ayarlama *ana kareleri* özellik değişiklikleri işaretlemek için bir zaman çizelgesi üzerinde. Ardından, animasyon çalıştırdığınızda, Blend özellik değişikliklerini belirtilen süre içindeki ilişkilendirir. Sorunsuz bir geçiş sonucudur. Bir nesneye ait herhangi bir özelliğine animasyon, görsel olmayan özelliklere bile yapabilirsiniz.

Adlı bir görsel taslak aşağıdaki çizimde **MoveUp**. Bir dikdörtgen X ve Y konumunu işaretleyen ana kareleri Zaman Çizelgesi içerir. Bu animasyonu çalıştırdığında, dikdörtgen bir konumdan diğerine sorunsuz bir şekilde taşır.

![XAML Tasarımcısı'nda MoveUp film şeridi](../designers/media/982f031a-74a3-414a-abc2-a0f41a741075.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio için Blend’i kullanarak kullanıcı arabirimi oluşturma](../designers/creating-a-ui-by-using-blend-for-visual-studio.md)