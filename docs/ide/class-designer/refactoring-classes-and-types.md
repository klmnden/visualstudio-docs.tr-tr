---
title: Sınıfları ve türleri Sınıf Tasarımcısı'nda taşıyın ve yeniden adlandırma
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
- vs.ClassDesigner.OverrideMembersDialog
helpviewer_keywords:
- members, overriding
- overriding members
- classes [Visual Studio], refactoring
- type members, overriding
- refactoring, types
- types [Visual Studio], refactoring
- Class Designer [Visual Studio], refactoring classes
- refactoring, classes
ms.assetid: dcf07bb4-fa3b-4224-9dec-566fd924a8ce
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e85c4b760bab242ba5aa43f0e1aab0936565af33
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53891472"
---
# <a name="refactor-classes-and-types-in-class-designer"></a>Sınıfları ve Sınıf Tasarımcısı'nda türleri yeniden düzenleme

Kodunu yeniden düzenlediğinizde, daha kolay anlamanız, bakımını yapmak ve daha verimli iç yapısını ve nesnelerini şeklini değiştirerek tasarlanan, dış davranışı. Sınıf Tasarımcısı ve sınıf Ayrıntıları penceresinde yapmanız gereken iş miktarını azaltmaya yönelik düzenlediğinizde, hataları giriş olasılığını kullanın C#, Visual Basic veya C++, Visual Studio projenize kodu.

> [!NOTE]
> Proje kaynak kodu denetiminde olması ve seçeneği işaretlenmezse, başvurulan bir projedir ve kendi dosya diskte salt okunur olarak işaretlenmiş olduğundan proje dosyaları salt okunur olabilir. Bu durumlardan biriyle projesinde çalışırken, projenin durumuna bağlı olarak çalışmanızı kaydetmek için çeşitli yollar sunulur. Bu, kodu yeniden düzenleme ve doğrudan düzenleme gibi başka bir yolla değiştirin kod geçerlidir.

## <a name="common-tasks"></a>Ortak görevler

|Görev|Destekleyici İçerik|
|----------| - |
|**Sınıfları yeniden düzenleme:** Yeniden düzenleme işlemleri, bir sınıfı kısmi sınıflara bölme veya soyut temel sınıf uygulamak için kullanabilirsiniz.|-   [Nasıl Yapılır: Bir sınıfı kısmi sınıflara bölme](how-to-split-a-class-into-partial-classes.md)|
|**Arabirimleri ile çalışma:** Sınıf Tasarımcısı'nda, sınıf diyagramı üzerinde arabirim yöntemleri için kod sağlayan bir sınıf bağlanarak bir arabirim uygulayabilir.|-   [Nasıl Yapılır: Arabirimi uygulama](how-to-implement-an-interface.md)|
|**Yeniden düzenleme türleri, tür üyeleri ve parametreleri:** Sınıf Tasarımcısı kullanarak türleri yeniden adlandırma, tür üyelerini geçersiz kılabilir veya bir türden diğerine taşıyabilirsiniz. Boş değer atanabilir türler de oluşturabilirsiniz.|-   [Yeniden adlandırma türler ve tür üyeleri](#rename-types-and-type-members)<br />-   [Tür üyeleri bir türden diğerine taşıma](#move-type-members-from-one-type-to-another)<br />-   [Nasıl Yapılır: Boş değer atanabilir tür oluşturma](how-to-create-a-nullable-type.md)|

## <a name="rename-types-and-type-members"></a>Yeniden adlandırma türler ve tür üyeleri

Sınıf Tasarımcısı'nda, bir tür veya üye türü sınıf diyagramında veya yeniden adlandırabilirsiniz **özellikleri** penceresi. İçinde **sınıf ayrıntıları** penceresinde üyesi ancak bir tür adını değiştirebilirsiniz. Bir tür veya tür üyesi yeniden adlandırılması, tüm windows ve eski adı burada görünen kod konumlarını yayar.

### <a name="rename-in-the-class-designer"></a>Sınıf Tasarımcısı'nda yeniden adlandır

1. Sınıf diyagramında türe veya üyeye seçin ve adını seçin.

     Üyenin adı düzenlenebilir hale gelir.

2. Türe veya üyeye türü için yeni adı yazın

### <a name="rename-in-the-class-details-window"></a>Sınıf Ayrıntıları penceresinde yeniden adlandır

1. Görüntülenecek **sınıf ayrıntıları** penceresinde tür veya tür üyesi sağ tıklayıp **sınıf ayrıntıları**.

     **Sınıf ayrıntıları** penceresi görüntülenir.

2. İçinde **adı** sütun türü üyesinin adını değiştirme

3. Hücreden odağı taşımak için basın **Enter** anahtar veya uzak bir hücreye tıklayın.

    > [!NOTE]
    > İçinde **sınıf ayrıntıları** penceresinde üyesi ancak bir tür adını değiştirebilirsiniz.

### <a name="rename-in-the-properties-window"></a>Özellikler penceresinde yeniden adlandır

1. Sınıf diyagramında veya **sınıf ayrıntıları** penceresinde, türe veya üyeye sağ tıklayın ve ardından **özellikleri**.

     **Özellikleri** penceresi görüntülenir ve türü veya tür üyesi için özellikleri görüntüler.

2. İçinde **adı** özelliği türü adını değiştirin veya üye türü.

     Tüm windows ve eski adı burada görünen kod konumlarını geçerli projede yeni adı yayar.

## <a name="move-type-members-from-one-type-to-another"></a>Tür üyeleri bir türden diğerine taşıma

Kullanarak **Sınıf Tasarımcısı**, başka bir tür için tür üyesi bir türden diğerine taşıyabilirsiniz. Her iki tür geçerli bir sınıf diyagramında görünür olmalıdır.

1. Tasarım yüzeyinde görünür olan bir tür, başka bir türe taşıyın ve ardından istediğiniz üyeye sağ tıklayarak **Kes**.

2. Hedef türüne sağ tıklayıp **Yapıştır**.

     Özellik kaynak türden kaldırılır ve hedef türünde görünür.

## <a name="see-also"></a>Ayrıca bkz.

- [Sınıfları ve türleri tasarlama](designing-and-viewing-classes-and-types.md)