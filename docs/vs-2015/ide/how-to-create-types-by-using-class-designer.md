---
title: 'Nasıl yapılır: Sınıf Tasarımcısı kullanarak tür oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
f1_keywords:
- VS.Clr.ClrAttributesDialog
helpviewer_keywords:
- custom attributes, applying
- class diagrams, creating types
- classes [Visual Studio], creating with Class Designer
- Class Designer [Visual Studio], creating classes
- types [Visual Studio], class diagrams
- attributes [Visual Studio], applying custom
ms.assetid: 94458c31-28bc-40e2-9737-85868788a0e5
caps.latest.revision: 45
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 3a20a9ecf08c82589fd915fdd4bd60c6144e9d1c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68201816"
---
# <a name="how-to-create-types-by-using-class-designer"></a>Nasıl yapılır: Sınıf Tasarımcısı Kullanarak Tür Oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual C# .NET ve Visual Basic .NET projeleri için yeni türleri tasarımı için bir sınıf diyagramı üzerinde oluşturun. Varolan türleri görmek için bkz: [nasıl yapılır: Varolan türleri görüntüleme (Sınıf Tasarımcısı)](../ide/how-to-view-existing-types-class-designer.md).  
  
- [Yeni tür oluşturma](#CreateType)  
  
- [Bir türe özel bir öznitelik uygulama](#CustAttributeType)  
  
- [Bir tür üyesine özel bir öznitelik uygulama](#CustAttributeMember)  
  
## <a name="CreateType"></a> Yeni tür oluşturma  
  
1. Araç Kutusu'nda, Sınıf Tasarımcısı'nın altında aşağıdakilerden birini bir sınıf diyagramına sürükleyin:  
  
    - **Sınıf** veya **soyut sınıf**  
  
    - **Sabit listesi**  
  
    - **Arabirimi**  
  
    - **Yapı** (VB) veya **yapı** (C#)  
  
    - **Temsilci**  
  
    - **Modül** (yalnızca VB)  
  
2. Türü adlandırın. Daha sonra erişim düzeyini seçin.  
  
3. Tür için başlangıç kodunu eklemek istediğiniz dosyayı seçin:  
  
    - Yeni bir dosya oluşturun ve bunu geçerli projeye eklemek için **yeni dosya oluştur** ve dosyayı adlandırın.  
  
    - Varolan bir dosyaya kod eklemek için seçin **varolan dosyaya ekleme**.  
  
         Çözümünüz birden fazla uygulama kod paylaşan bir proje varsa, yalnızca ilgili sınıf dosyası aynı uygulama projesinde veya paylaşılan projede, ancak uygulama projesinde sınıf diyagramına yeni bir tür ekleyebilirsiniz.  
  
4. Şimdi, türü tanımlamak için diğer öğeleri ekleyin:  
  
    |||  
    |-|-|  
    |**için**|**Add**|  
    |Sınıflar, soyut sınıflar, yapılar veya struct'lar|Yöntemler, özellikler, alanlar, olaylar, yapıcılar (yöntem), yıkıcılar (yöntem) ve türü tanımlayan sabitler|  
    |Numaralandırmalar|Numaralandırmayı oluşturan alan değerleri|  
    |Arabirimler|Yöntemler, özellikler ve arabirimi oluşturan olaylar|  
    |Temsilci|Temsilciyi tanımlayan parametreler|  
    |Modül|Yöntemler, özellikler, alanlar, olaylar, yapıcılar (yöntem) ve modülü tanımlayan sabitler|  
  
     Bkz: [üyeleri oluşturma](../ide/creating-and-configuring-type-members-class-designer.md#CreateMembers).  
  
## <a name="CustAttributeType"></a> Bir türe özel bir öznitelik uygulama  
  
1. Bir sınıf diyagramında türe ait şekle tıklayın.  
  
2. Özellikler penceresinde yanındaki **özel öznitelikler** özellik türü için üç nokta (…) düğmesine tıklayın.  
  
3. Satır başına bir olmak üzere, bir ya da daha fazla özel öznitelik ekleyin. Bunları ayraçlar içine almayın.  
  
     İşiniz bittiğinde özel öznitelikler türe uygulanır.  
  
## <a name="CustAttributeMember"></a> Bir tür üyesine özel bir öznitelik uygulama  
  
1. Bir sınıf diyagramında kendi türünün şeklinde üyenin adına veya Sınıf Ayrıntıları penceresinde satırına tıklayın.  
  
2. Özellikler penceresinde üyeye ait bulma **özel öznitelikler** özelliği.  
  
3. Satır başına bir olmak üzere, bir ya da daha fazla özel öznitelik ekleyin. Bunları ayraçlar içine almayın.  
  
     İşiniz bittiğinde özel öznitelikler türe uygulanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: (Sınıf Tasarımcısı) türler arasında devralma oluşturma](../ide/how-to-create-inheritance-between-types-class-designer.md)   
 [Nasıl yapılır: (Sınıf Tasarımcısı) türler arasında ilişkilendirme oluşturma](../ide/how-to-create-associations-between-types-class-designer.md)   
 [Tür üyeleri (Sınıf Tasarımcısı) oluşturma ve yapılandırma](../ide/creating-and-configuring-type-members-class-designer.md)   
 [Sınıf diyagramları (Sınıf Tasarımcısı) ile çalışma](../ide/working-with-class-diagrams-class-designer.md)   
 [Sınıfları ve Türleri Tasarlama (Sınıf Tasarımcısı)](../ide/designing-classes-and-types-class-designer.md)
