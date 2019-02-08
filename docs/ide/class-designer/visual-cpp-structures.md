---
title: Sınıf Tasarımcısında Visual C++ Yapılandırmaları
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Class Designer [Visual Studio], structures
ms.assetid: bad18ab6-d956-47a6-a413-811cc26db5f5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: e9b8e81ee25e081a324a8520317fa57a1314ccd0
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55954536"
---
# <a name="visual-c-structures-in-class-designer"></a>Sınıf tasarımcısında Visual C++ yapılandırmaları

**Sınıf Tasarımcısı** anahtar sözcüğü ile bildirilen C++ yapıları destekleyen `struct`. Bir örneği verilmiştir:

```cpp
struct MyStructure
{
   char a;
   int i;
   long j;
};
```

Kullanma hakkında daha fazla bilgi için `struct` yazın, bkz: [yapı](/cpp/cpp/struct-cpp).

Sınıf diyagramında C++ yapı şeklinde görünür ve etiketi dışında sınıf şeklinin gibi çalışır **yapı** ve yuvarlak köşeler yerine dörtgen köşelerine sahiptir.

|Kod öğesi|Sınıf Tasarımcısı görünümü|
|------------------| - |
|`struct StructureName {};`|**StructureName**<br /><br /> Yapı|

## <a name="see-also"></a>Ayrıca bkz.

- [Visual C++ Kodu ile Çalışma](working-with-visual-cpp-code.md)
- [Sınıflar ve Yapılar](/cpp/cpp/classes-and-structs-cpp)
- [struct](/cpp/cpp/struct-cpp)