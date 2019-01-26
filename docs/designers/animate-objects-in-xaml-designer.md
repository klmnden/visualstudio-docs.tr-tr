---
title: XAML Tasarımcısı’nda nesnelere animasyon ekleme
ms.date: 04/11/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: fb88fa26-e835-47f5-9771-2f279441c83c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- uwp
ms.openlocfilehash: f6fbeceeb0c9943e561c5bd4e353551005be23a4
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54960210"
---
# <a name="animate-objects-in-xaml-designer"></a>XAML Tasarımcısı’nda nesnelere animasyon ekleme

Nesneleri taşıma kısa animasyonlar oluşturma veya içeri ve dışarı Soldurma.

Başlamak için oluşturun bir *film şeridi*. Bir veya daha fazla görsel taslak içeren *zaman çizelgeleri*. Ayarlama *ana kareleri* özellik değişiklikleri işaretlemek için bir zaman çizelgesi üzerinde. Ardından, animasyon çalıştırdığınızda, Blend özellik değişikliklerini belirtilen süre içindeki ilişkilendirir. Sorunsuz bir geçiş sonucudur. Bir nesneye ait herhangi bir özelliğine animasyon, görsel olmayan özelliklere bile yapabilirsiniz.

Adlı bir görsel taslak aşağıdaki çizimde **MoveUp**. Bir dikdörtgen X ve Y konumunu işaretleyen ana kareleri Zaman Çizelgesi içerir. Bu animasyonu çalıştırdığında, dikdörtgen bir konumdan diğerine sorunsuz bir şekilde taşır.

![XAML Tasarımcısı'nda MoveUp film şeridi](../designers/media/982f031a-74a3-414a-abc2-a0f41a741075.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio için Blend’i kullanarak kullanıcı arabirimi oluşturma](../designers/creating-a-ui-by-using-blend-for-visual-studio.md)