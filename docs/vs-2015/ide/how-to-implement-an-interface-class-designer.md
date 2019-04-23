---
title: 'Nasıl yapılır: Arabirimi uygulama (Sınıf Tasarımcısı) | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- interfaces [Visual Studio], implementing
- interfaces [Visual Studio]
ms.assetid: 81d2cf46-7f60-448c-83e3-1d16bb88ca36
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 0d49d0cb43e4d93c5981aa9000c8ae539bc84879
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60099565"
---
# <a name="how-to-implement-an-interface-class-designer"></a>Nasıl yapılır: Arabirimi uygulama (Sınıf Tasarımcısı)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Sınıf Tasarımcısı'nda, sınıf diyagramı üzerinde arabirim yöntemleri için kod sağlayan bir sınıf bağlanarak bir arabirim uygulayabilir. Sınıf Tasarımcısı, bir arabirim uygulaması oluşturur ve arabirim ve sınıfları arasındaki ilişki devralma ilişkisi görüntüler. Devralım çizgisi sınıf ve arabirim arasında çizim veya sınıf görünümünden arabirimi sürükleyerek bir arabirim uygulayabilir.  
  
> [!TIP]
>  Diğer türleri oluşturma aynı şekilde arabirimleri oluşturabilirsiniz. Arabirimi var, ancak sınıf diyagramı üzerinde görünmesini değil, sonra ilk görüntüleyin. Daha fazla bilgi için [nasıl yapılır: Sınıf Tasarımcısı kullanarak tür oluşturma](../ide/how-to-create-types-by-using-class-designer.md) ve [nasıl yapılır: Varolan türleri görüntüleme (Sınıf Tasarımcısı)](../ide/how-to-view-existing-types-class-designer.md).  
  
### <a name="to-implement-an-interface-by-drawing-an-inheritance-line"></a>Devralım çizgisi çizerek bir arabirim uygulamak için  
  
1. Sınıf diyagramında, arabirimi ve arabirimini uygulayan sınıf görüntüler.  
  
2. Devralım çizgisi, sınıf ve arabirim çizin.  
  
    Lolipop sınıfa iliştirilen görünür ve devralma ilişkisi arabirim adını içeren bir etiket tanımlar. Visual Studio tüm arabirim üyeleri için saplamalar oluşturur.  
  
   Daha fazla bilgi için [nasıl yapılır: (Sınıf Tasarımcısı) türler arasında devralma oluşturma](../ide/how-to-create-inheritance-between-types-class-designer.md).  
  
### <a name="to-implement-an-interface-from-the-class-view-window"></a>Sınıf Görünümü penceresinden bir arabirim uygulamak için  
  
1. Sınıf diyagramı üzerinde arabirim uygulamak istediğiniz sınıf görüntüler.  
  
2. Sınıf Görünümü açın ve arabirimi bulun.  
  
    > [!TIP]
    >  Sınıf Görünümü açık değilse, sınıf görünümünden açın **görünümü** menüsü. Sınıf Görünümü hakkında daha fazla bilgi için bkz: [Viewing Classes and Their Members](http://msdn.microsoft.com/71e9e8f3-261a-4e0c-87bf-5ec48b8bf333).  
  
3. Arabirim düğümü diyagramında sınıf şekline sürükleyin.  
  
     Lolipop sınıfa iliştirilen görünür ve devralma ilişkisi arabirim adını içeren bir etiket tanımlar. Visual Studio tüm arabirim üyeleri için saplamalar oluşturur; Bu noktada, arabirim uygulanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Sınıf Tasarımcısı kullanarak tür oluşturma](../ide/how-to-create-types-by-using-class-designer.md)   
 [Nasıl yapılır: Varolan türleri görüntüleme (Sınıf Tasarımcısı)](../ide/how-to-view-existing-types-class-designer.md)   
 [Nasıl yapılır: (Sınıf Tasarımcısı) türler arasında devralma oluşturma](../ide/how-to-create-inheritance-between-types-class-designer.md)   
 [Sınıfları ve Türleri Yeniden Düzenleme (Sınıf Tasarımcısı)](../ide/refactoring-classes-and-types-class-designer.md)
