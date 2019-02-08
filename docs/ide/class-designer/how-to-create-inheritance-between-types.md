---
title: 'Nasıl yapılır: (Sınıf Tasarımcısı) türler arasında devralma oluşturma'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.classdesigner.inheritanceline
helpviewer_keywords:
- inheritance, relationship defining
- relationships, defining inheritance
ms.assetid: 3786a21c-8022-4bf5-9d13-740fd354e93c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8060f17277a5e80a139ee8d6406fb40d0a84ec71
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55915931"
---
# <a name="how-to-create-inheritance-between-types-in-class-designer"></a>Nasıl yapılır: Sınıf tasarımcısında türler arasında devralma oluşturma

Kullanarak bir sınıf diyagramı üzerindeki iki tür arasında devralma ilişkisi oluşturamadığınız için **Sınıf Tasarımcısı**, temel türü kendi türetilmiş bir türü veya türleri ile bağlanın. İki sınıf arasındaki, bir sınıf ve arabirim arasında veya iki arabirim arasında bir devralma ilişkisi olabilir.

## <a name="to-create-an-inheritance-between-types"></a>Bir türler arasında devralma oluşturma

1.  İçinde projenizden **Çözüm Gezgini**, bir sınıf diyagramı (.cd) dosyası açın.

     Bir sınıf diyagramı yoksa, oluşturun. Bkz: [nasıl yapılır: Projelere sınıf diyagramları ekleme](how-to-add-class-diagrams-to-projects.md).

2.  İçinde **araç kutusu**altında **Sınıf Tasarımcısı**, tıklayın **devralma**.

3.  Sınıf diyagramında devralım çizgisi başlayarak, istediğiniz türlerini arasında Çiz:

    -   Temel sınıfın türetilmiş bir sınıf

    -   Uygulanan arabirimi uygulayan sınıfı

    -   Genişletilmiş arabirimi için bir genişletme arabirimi

4.  İsteğe bağlı olarak, genel bir türden türetilmiş bir tür olduğunda, devralım çizgisi tıklayın. İçinde **özellikleri** penceresinde **tür bağımsız değişkenleri** genel tür için istediğiniz türüyle eşleşecek şekilde özelliği.

    > [!NOTE]
    > Ardından tüm soyut üye bir soyut sınıfı en az bir soyut üye içermesi durumunda, soyut olmayan devralma sınıfları olarak uygulanır.
    >
    >  Varolan genel türleri görselleştirebilir olsa da, yeni genel türler oluşturulamıyor. Ayrıca, varolan genel türler için tür parametrelerini değiştiremezsiniz.

## <a name="see-also"></a>Ayrıca bkz.

- [Devralma](/dotnet/csharp/programming-guide/classes-and-structs/inheritance)
- [Devralma Temelleri](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)
- [Nasıl yapılır: Türler arasında devralmayı görüntüleme](how-to-view-inheritance-between-types.md)
- [Sınıf Tasarımcısında Visual C++ Sınıfları](visual-cpp-classes.md)