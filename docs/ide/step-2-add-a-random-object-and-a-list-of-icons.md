---
title: '2. Adım: Rasgele nesne ve simge listesi ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 95faea28-eddc-4cfa-95fb-3b34b5a976d7
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5ee92ad3c65c81849e70f7e76b93b9a3b6195156
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60046064"
---
# <a name="step-2-add-a-random-object-and-a-list-of-icons"></a>2. Adım: Rasgele nesne ve simge listesi ekleme
Bu adımda, oyun için bir grup eşleşen simge oluşturuyorsunuz. Her simge, form üzerindeki TableLayoutPanel denetiminde rasgele iki hücreye eklenir. Bunu yapmak için iki kullandığınız `new` deyimleri iki nesne oluşturmak için. İlki bir <xref:System.Random> matematik sınavı oyununda kullanılan gibi bir nesne. Bu koddaki kullanım amacıysa, TableLayoutPanel denetiminde rasgele hücre seçmektir. İçin yeni olabilecek ikinci nesne bir <xref:System.Collections.Generic.List%601> rasgele seçilen simgeleri depolamak için kullanılan nesne.

## <a name="to-add-a-random-object-and-a-list-of-icons"></a>Rasgele nesne ve simge listesi eklemek için

1. İçinde **Çözüm Gezgini**, seçin *Form1.cs* Visual kullanıyorsanız C#, veya *Form1.vb* Visual Basic kullanıyorsanız ve menü çubuğunda, ardından**Görünümü** > **kod**. Alternatif olarak, seçtiğiniz **F7** anahtar veya çift **Form1** içinde **Çözüm Gezgini**.

     Böylece Form1'in arkasındaki kod modülü görüntülenir.

2. Varolan kod içine aşağıdaki kodu ekleyin.

     [!code-csharp[VbExpressTutorial4Step2_3_4#1](../ide/codesnippet/CSharp/step-2-add-a-random-object-and-a-list-of-icons_1.cs)]
     [!code-vb[VbExpressTutorial4Step2_3_4#1](../ide/codesnippet/VisualBasic/step-2-add-a-random-object-and-a-list-of-icons_1.vb)]

     Visual C# kullanıyorsanız olması emin yerleştirdiğiniz kodu açılış kaşlı ayracından sonra ve yalnızca sınıf bildiriminden sonra (`public partial class Form1 : Form`). Visual Basic kullanıyorsanız sınıf bildiriminden hemen sonra kod yerleştirin (`Public Class Form1`).

3. Liste nesnesi eklerken, fark **IntelliSense** açılır pencere. Aşağıdaki bir Visual C# örneği olmakla birlikte, Visual Basic'te liste eklediğinizde de benzer bir metin görüntülenir.

     ![Click gösteren Özellikler penceresi olay](../ide/media/express_listintellisense.png) IntelliSense penceresi

    > [!NOTE]
    >  IntelliSense penceresi yalnızca kodu el ile girdiğinizde, görünür. Kodu kopyalayıp yapıştırırsanız görünmez.

     Kodu (ve açıklamaları) küçük bölümler halinde incelerseniz anlaması daha kolay olur. Programlarınızın liste nesneleri, farklı türlerde öğeler izlemek için kullanabilirsiniz. Bir liste; sayıları, doğru/yanlış değerlerini, metinleri veya diğer nesneleri barındırabilir. Hatta diğer liste nesneleri içeren bir liste nesnesi olabilir. Bir listedeki öğeler öğe olarak adlandırılır ve her liste yalnızca öğesi bir tür tutar. Öyleyse, bir sayı listesi yalnızca sayıları tutabilir; bu listeye metin ekleyemezsiniz. Benzer şekilde, doğru/yanlış değerlerini içeren bir listeye sayı ekleyemezsiniz.

     Oluştururken bir `List` kullanarak nesne bir `new` deyimi içinde depolamak istediğiniz veri türünü belirtmeniz gerekir. İşte bu nedenle en üstündeki araç ipucu **IntelliSense** penceresi listesinde öğelerin türlerini gösterir. Ayrıca, budur `List<string>` (görselde C#) ve `List(Of String)` (Visual Basic'te) anlamına gelir: Bu bir `List` öğelerini tutan nesne `string` veri türü. Programınızın metin depolamak için kullandığı bir dizedir hangi sağındaki araç ipucu olduğu **IntelliSense** penceresi, unsurdur.

4. Visual Basic'te önce geçici bir dizin oluşturulması gerekmesine karşın, Visual C# ortamında listenin tek bir deyimle oluşturulabilmesinin nedenini bir düşünün. Visual C# diline sahip olmasıdır *koleksiyon başlatıcıları*, liste değerleri kabul etmek için hazırlayın. Visual Basic'te bir koleksiyon başlatıcısı kullanabilirsiniz. Ancak, önceki Visual Basic sürümü ile uyumluluk açısından önceki kodu kullanmanızı öneririz.

     Bir koleksiyon Başlatıcısı kullandığınızda bir `new` deyimi, yeni liste nesnesi oluşturulduktan sonra program doldurur, kaşlı ayraçlar içinde sağladığınız verilerle. Bu durumda, simgeler adlı dizelerinin listesini almak ve bu liste on altı dize içeren başlatılır. Bu dizelerin her biri tek bir harftir ve bunların tümü etiketlerde yer alacak simgelere karşılık gelir. Dolayısıyla, oyunda bir çift ünlem işareti, bir çift büyük N harfi, bir çift virgül vs. olacaktır. (Bu karakterler Webdings yazı tipine ayarlandığında, otobüs, bisiklet, örümcek vb. simgeler olarak görünür.) Liste nesnenizin TableLayoutPanel panelindeki her hücreye tüm, on altı dize olacaktır.

    > [!NOTE]
    >  Visual Basic'te aynı sonucu elde etmek, ancak dizeler ardından bir liste nesnesine dönüştürülür geçici bir dizinin ilk şekilde yerleştirilir. Örneğin, dizilerin sabit boyutlu oluşturulması dışında, dizi bir listeye benzer. Listelerin gerektiğinde daralabilmesi ve genişleyebilmesi bu programda önem taşır.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz: [3. adım: Her etikete rasgele simge atama](../ide/step-3-assign-a-random-icon-to-each-label.md).

- Önceki öğretici adımına dönmek için bkz: [1. adım: Proje oluşturma ve formunuza tablo ekleme](../ide/step-1-create-a-project-and-add-a-table-to-your-form.md).
