---
title: Sınıf Tasarımcısında Visual C++ Typedefs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.classdesigner.typedef
- vs.classdesigner.aliasofline
helpviewer_keywords:
- Class Designer [Visual Studio], typedefs
ms.assetid: c1984108-71fc-4d3a-b4d4-3eac2c6b4ebf
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 328235e5be2ac62caa427c9f77bd33654275e72a
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55907717"
---
# <a name="visual-c-typedefs-in-class-designer"></a>Sınıf tasarımcısında Visual C++ typedefs

[TypeDef](/cpp/cpp/aliases-and-typedefs-cpp#typedefs) deyimleri, bir veya daha fazla katman bir ad ve temel alınan türü arasında bir yöneltme oluşturun. **Sınıf Tasarımcısı** anahtar sözcüğü ile bildirilen C++ typedef türlerini destekler `typedef`, örneğin:

```cpp
typedef class coord
{
   void P(x,y);
   unsigned x;
   unsigned y;
} COORD;
```

Ardından bu tür bir örneği bildirmek için de kullanabilirsiniz:

`COORD OriginPoint;`

## <a name="class-and-struct-shapes"></a>Sınıf ile yapı şekilleri

İçinde **Sınıf Tasarımcısı**, bir C++ typedef typedef içinde belirtilen tür şeklini sahiptir. Kaynak bildirirse `typedef class`, şeklin köşe ve etiket yuvarlanmış **sınıfı**. İçin `typedef struct`, Şekil köşeler ve etikete sahiptir **yapı**.

Bunların içinde bildirilen iç içe geçmiş tür tanımları, sınıfları ve yapıları olabilir. İçinde **Sınıf Tasarımcısı**, sınıf ve yapı şekilleri iç içe geçmiş typedef bildirimleri gibi iç içe geçmiş şekillere gösterebilir.

TypeDef şekilleri Destek **ilişkilendirmesi olarak göster** ve **koleksiyon ilişkilendirmesi olarak göster** komutları sağ tıklama menüsünde (bağlam menüsü).

### <a name="class-typedef-example"></a>Sınıf typedef örneği

```cpp
class B {};
typedef B MyB;
```

![Sınıf Tasarımcısı'nda C++ sınıfı typedef](media/cpp-class-typedef.png)

### <a name="struct-typedef-example"></a>Yapı typedef örneği

```cpp
typedef struct mystructtag
{
    int   i;
    double f;
} mystruct;
```

![Sınıf Tasarımcısı'nda C++ yapı typedef](media/cpp-struct-typedef.png)

## <a name="unnamed-typedefs"></a>Adsız tür tanımları

Bir ad olmadan bir typedef bildirebilirsiniz rağmen **Sınıf Tasarımcısı** belirttiğiniz etiket adını kullanmaz. **Sınıf Tasarımcısı** adını kullanır, **sınıf görünümü** oluşturur. Örneğin, aşağıdaki bildirimi geçerlidir, ancak görünür **sınıf görünümü** ve **Sınıf Tasarımcısı** adlı bir nesne olarak **__unnamed**:

```cpp
typedef class coord
{
   void P(x,y);
   unsigned x;
   unsigned y;
};
```

> [!NOTE]
> **Sınıf Tasarımcısı** tür tanımları, kaynak türü, işlev işaretçisi olan görüntülemez.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual C++ kodu ile çalışma](working-with-visual-cpp-code.md)
- [Tür tanımları](/cpp/cpp/aliases-and-typedefs-cpp#typedefs)