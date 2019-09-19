---
title: '2\. Adım: Rastgele bir nesne ve simge listesi ekleme'
ms.date: 11/04/2016
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
dev_langs:
- CSharp
- VB
ms.assetid: 95faea28-eddc-4cfa-95fb-3b34b5a976d7
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 31058afee1dc9fc0c9f24c773b9bdc3e5d1fb49a
ms.sourcegitcommit: 6eed0372976c0167b9a6d42ba443f9a474b8bb91
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71118943"
---
# <a name="step-2-add-a-random-object-and-a-list-of-icons"></a>2\. Adım: Rastgele bir nesne ve simge listesi ekleme
Bu adımda, oyun için bir grup eşleşen simge oluşturuyorsunuz. Her simge, form üzerindeki TableLayoutPanel denetiminde rasgele iki hücreye eklenir. Bunu yapmak için iki nesne oluşturmak üzere `new` iki deyim kullanırsınız. Birincisi, matematik sınavından kullandığınız gibi bir <xref:System.Random> nesnedir. Bu koddaki kullanım amacıysa, TableLayoutPanel denetiminde rasgele hücre seçmektir. Sizin için yeni olabilecek ikinci nesne, rastgele seçilmiş sembolleri depolamak için kullanılan <xref:System.Collections.Generic.List%601> bir nesnedir.

## <a name="to-add-a-random-object-and-a-list-of-icons"></a>Rastgele bir nesne ve simge listesi eklemek için

1. **Çözüm Gezgini**, Visual C#kullanıyorsanız *Form1.cs* ' i veya Visual Basic kullanıyorsanız *Form1. vb* öğesini seçin ve ardından menü çubuğunda**kodu** **görüntüle** > ' yi seçin. Alternatif olarak, **F7** tuşunu seçebilir veya **Çözüm Gezgini**içinde **Form1** ' e çift tıklayatıklayabilirsiniz.

     Böylece Form1'in arkasındaki kod modülü görüntülenir.

2. Varolan kod içine aşağıdaki kodu ekleyin.

     [!code-csharp[VbExpressTutorial4Step2_3_4#1](../ide/codesnippet/CSharp/step-2-add-a-random-object-and-a-list-of-icons_1.cs)]
     [!code-vb[VbExpressTutorial4Step2_3_4#1](../ide/codesnippet/VisualBasic/step-2-add-a-random-object-and-a-list-of-icons_1.vb)]

     Görsel C#kullanıyorsanız, kodu açılış küme ayracından sonra ve Sınıf bildiriminden hemen sonra (`public partial class Form1 : Form`) yerleştirdiğinizden emin olun. Visual Basic kullanıyorsanız, kodu Sınıf bildiriminden (`Public Class Form1`) hemen sonra koyun.

3. Liste nesnesi eklenirken, açılan **IntelliSense** penceresine dikkat edin. Aşağıdaki bir Visual C# örneği olmakla birlikte, Visual Basic'te liste eklediğinizde de benzer bir metin görüntülenir.

     ![Click olayı](../ide/media/express_listintellisense.png) IntelliSense penceresini gösteren Özellikler penceresi

    > [!NOTE]
    > IntelliSense penceresi yalnızca el ile kod girdiğinizde görünür. Kodu kopyalayıp yapıştırırsanız görünmez.

     Kodu (ve açıklamaları) küçük bölümler halinde incelerseniz anlaması daha kolay olur. Programlarınız, birçok farklı öğe türünü izlemek için liste nesnelerini kullanabilir. Bir liste; sayıları, doğru/yanlış değerlerini, metinleri veya diğer nesneleri barındırabilir. Diğer Liste nesnelerini tutan bir liste nesneniz bile olabilir. Bir listedeki öğelere öğeler denir ve her liste yalnızca bir öğe türü tutar. Öyleyse, bir sayı listesi yalnızca sayıları tutabilir; bu listeye metin ekleyemezsiniz. Benzer şekilde, doğru/yanlış değerlerini içeren bir listeye sayı ekleyemezsiniz.

     `List` Bir`new` ifade kullanarak bir nesne oluşturduğunuzda, içinde depolamak istediğiniz veri türünü belirtmeniz gerekir. **IntelliSense** penceresinin en üstündeki araç ipucu, listedeki öğe türlerini gösterir. Ayrıca, bu, `List<string>` (görselde C#) ve `List(Of String)` (Visual Basic) olarak şu anlama gelir: Bu, `List` `string` veri türü öğelerini tutan bir nesnedir. Bir dize, programınızın metin depolamak için kullandığı şeydir. Bu, **IntelliSense** penceresinin sağındaki araç ipucu sizi size söylemiş olur.

4. Visual Basic'te önce geçici bir dizin oluşturulması gerekmesine karşın, Visual C# ortamında listenin tek bir deyimle oluşturulabilmesinin nedenini bir düşünün. Bunun nedeni, görsel C# dilin *koleksiyon başlatıcıları*olduğundan, listeyi değerleri kabul edecek şekilde hazırlar. Visual Basic'te bir koleksiyon başlatıcısı kullanabilirsiniz. Ancak, önceki Visual Basic sürümü ile uyumluluk açısından önceki kodu kullanmanızı öneririz.

     Bir `new` koleksiyon başlatıcısı kullandığınızda, yeni liste nesnesi oluşturulduktan sonra, program bunu küme ayraçları içinde verdiğiniz verilerle doldurur. Bu durumda, simgeler adlı dizelerin bir listesini alırsınız ve bu liste altı harfli dizeler içerecek şekilde başlatılır. Bu dizelerin her biri tek bir harftir ve bunların tümü etiketlerde yer alacak simgelere karşılık gelir. Dolayısıyla, oyunda bir çift ünlem işareti, bir çift büyük N harfi, bir çift virgül vs. olacaktır. (Bu karakterler Webdings yazı tipine ayarlandığında, otobüs, bisiklet, örümcek vb. simgeler olarak görünür.) Liste nesneniz, TableLayoutPanel panelindeki her hücre için bir tane olmak üzere on altı dizeye sahip olacaktır.

    > [!NOTE]
    > Visual Basic, aynı sonucu alırsınız, ancak önce dizeler geçici bir diziye konur, bu daha sonra bir liste nesnesine dönüştürülür. Örneğin, dizilerin sabit boyutlu oluşturulması dışında, dizi bir listeye benzer. Listelerin gerektiğinde daralabilmesi ve genişleyebilmesi bu programda önem taşır.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına geçmek için, bkz [. Adım 3: Her etikete](../ide/step-3-assign-a-random-icon-to-each-label.md)rastgele bir simge atayın.

- Önceki öğretici adımına dönmek için bkz [. Adım 1: Bir proje oluşturun ve formunuza](../ide/step-1-create-a-project-and-add-a-table-to-your-form.md)tablo ekleyin.
