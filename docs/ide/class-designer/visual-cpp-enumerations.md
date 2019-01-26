---
title: Sınıf Tasarımcısında Visual C++ Numaralandırmaları
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- Class Designer [Visual Studio], enumerations
ms.assetid: 11e90ba1-18cd-44f8-9e26-e3746a7a19d1
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: d5f02d899c9d81c8dd19aac879bed7ac9c1acdb8
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54946834"
---
# <a name="visual-c-enumerations-in-class-designer"></a>Sınıf tasarımcısında Visual C++ numaralandırmaları

**Sınıf Tasarımcısı** C++ destekler `enum` ve kapsamlı `enum class` türleri. Bir örneği verilmiştir:

```cpp
enum CardSuit {
   Diamonds = 1,
   Hearts = 2,
   Clubs = 3,
   Spades = 4
};

// or...
enum class CardSuit {
   Diamonds = 1,
   Hearts = 2,
   Clubs = 3,
   Spades = 4
};
```

Sınıf diyagramında C++ numaralandırma şekli görünür ve etiketi dışında bir yapı şeklinde çalışır **Enum** veya **sabit listesi sınıfı**, mavi yerine pembe ve sol üst taraftaki renkli kenarlık vardır Kenar boşlukları. Numaralandırma şekilleri ve yapı şekilleri dörtgen köşelerine sahiptir.

Kullanma hakkında daha fazla bilgi için `enum` yazın, bkz: [numaralandırmalar](/cpp/cpp/enumerations-cpp).

## <a name="see-also"></a>Ayrıca bkz.

- [Visual C++ Kodu ile Çalışma](working-with-visual-cpp-code.md)
- [Sabit Listeleri](/cpp/cpp/enumerations-cpp)