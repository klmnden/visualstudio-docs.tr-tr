---
title: 'Nasıl yapılır: Arabirimi uygulama (Sınıf Tasarımcısı)'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- interfaces [Visual Studio], implementing
- interfaces [Visual Studio]
ms.assetid: 81d2cf46-7f60-448c-83e3-1d16bb88ca36
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f070e3224dcc683d766da556512f285751c37ca4
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55923923"
---
# <a name="how-to-implement-an-interface-in-class-designer"></a>Nasıl yapılır: Sınıf Tasarımcısı'nda arabirimi uygulama

İçinde **Sınıf Tasarımcısı**, arabirim yöntemleri için kod sağlayan bir sınıf bağlanarak, sınıf diyagramı üzerinde bir arabirim uygulayabilir. **Sınıf Tasarımcısı** bir arabirim uygulaması oluşturur ve arabirim ve sınıfları arasındaki ilişki devralma ilişkisi görüntüler. Devralım çizgisi sınıf ve arabirim arasında çizim veya sınıf görünümünden arabirimi sürükleyerek bir arabirim uygulayabilir.

> [!TIP]
> Diğer türleri oluşturma aynı şekilde arabirimleri oluşturabilirsiniz. Arabirimi var, ancak sınıf diyagramı üzerinde görünmesini değil, sonra ilk görüntüleyin. Daha fazla bilgi için [nasıl yapılır: Sınıf Tasarımcısı kullanarak tür oluşturma](how-to-create-types.md) ve [nasıl yapılır: Varolan türleri görüntüleme](how-to-view-existing-types.md).

## <a name="to-implement-an-interface-by-drawing-an-inheritance-line"></a>Devralım çizgisi çizerek bir arabirim uygulamak için

1.  Sınıf diyagramında, arabirimi ve arabirimini uygulayan sınıf görüntüler.

2.  Devralım çizgisi, sınıf ve arabirim çizin.

     Lolipop sınıfa iliştirilen görünür ve devralma ilişkisi arabirim adını içeren bir etiket tanımlar. Visual Studio tüm arabirim üyeleri için saplamalar oluşturur.

Daha fazla bilgi için [nasıl yapılır: Türler arasında devralma oluşturma](how-to-create-inheritance-between-types.md).

## <a name="to-implement-an-interface-from-the-class-view-window"></a>Sınıf Görünümü penceresinden bir arabirim uygulamak için

1.  Sınıf diyagramı üzerinde arabirim uygulamak istediğiniz sınıf görüntüler.

2.  Açık **sınıf görünümü** arabirimi bulun.

    > [!TIP]
    > Varsa **sınıf görünümü** açık, açık olmayan **sınıf görünümü** gelen **görünümü** menü veya basın **Ctrl**+**Shift** + **C**.

3.  Arabirim düğümü diyagramında sınıf şekline sürükleyin.

     Lolipop sınıfa iliştirilen görünür ve devralma ilişkisi arabirim adını içeren bir etiket tanımlar. Visual Studio tüm arabirim üyeleri için saplamalar oluşturur; Bu noktada, arabirim uygulanır.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Sınıf Tasarımcısı kullanarak tür oluşturma](how-to-create-types.md)
- [Nasıl yapılır: Varolan türleri görüntüleme](how-to-view-existing-types.md)
- [Nasıl yapılır: Türler arasında devralma oluşturma](how-to-create-inheritance-between-types.md)
- [Sınıfları ve Türleri Yeniden Düzenleme](refactoring-classes-and-types.md)