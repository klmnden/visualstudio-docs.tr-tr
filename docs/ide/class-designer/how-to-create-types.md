---
title: 'Nasıl yapılır: Sınıf Tasarımcısı kullanarak tür oluşturma'
ms.date: 11/04/2016
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
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: abee206f67aa019476fcd5085b4ff872338b4d1f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62975274"
---
# <a name="how-to-create-types-by-using-class-designer"></a>Nasıl yapılır: Sınıf Tasarımcısı kullanarak tür oluşturma

İçin yeni türleri tasarımı için C# ve Visual Basic projeleri, bunları bir sınıf diyagramı üzerinde oluşturun. Varolan türleri görmek için bkz: [nasıl yapılır: Varolan türleri görüntüleme](how-to-view-existing-types.md).

## <a name="CreateType"></a> Yeni tür oluşturma

1. İçinde **araç kutusu**altında **Sınıf Tasarımcısı**, aşağıdakilerden birini bir sınıf diyagramına sürükleyin:

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

     Bkz: [üyeleri oluşturma](creating-and-configuring-type-members.md#create-members).

## <a name="CustAttributeType"></a> Bir türe özel bir öznitelik uygulama

1. Bir sınıf diyagramında türe ait şekle tıklayın.

2. İçinde **özellikleri**yanındaki **özel öznitelikler** özellik türü için üç nokta (…) düğmesine tıklayın.

3. Satır başına bir olmak üzere, bir ya da daha fazla özel öznitelik ekleyin. Bunları ayraçlar içine almayın.

   Özel öznitelikler türe uygulanır.

## <a name="CustAttributeMember"></a> Bir tür üyesine özel bir öznitelik uygulama

1. Bir sınıf diyagramında kendi türünün şeklinde üyenin adına veya Sınıf Ayrıntıları penceresinde satırına tıklayın.

2. İçinde **özellikleri**, üyenin Bul **özel öznitelikler** özelliği.

3. Satır başına bir olmak üzere, bir ya da daha fazla özel öznitelik ekleyin. Bunları ayraçlar içine almayın.

   Özel öznitelikler türe uygulanır.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Türler arasında devralma oluşturma](how-to-create-inheritance-between-types.md)
- [Nasıl yapılır: Türler arasında ilişkilendirme oluşturma](how-to-create-associations-between-types.md)
- [Tür Üyeleri Oluşturma ve Yapılandırma](creating-and-configuring-type-members.md)
- [Sınıfları ve türleri tasarlama](designing-and-viewing-classes-and-types.md)
