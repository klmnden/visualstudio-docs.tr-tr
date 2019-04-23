---
title: '4. Adım: Her etikete Click olay işleyicisi ekleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: 16bdbc7c-4129-411d-bace-f4a3e5375975
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 9f23d0593129cae2732c8b4df14b3f5e2d5a69f7
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60051381"
---
# <a name="step-4-add-a-click-event-handler-to-each-label"></a>4. Adım: Her Etikete Bir Tıklama Olayı İşleyicisi Ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Eşleştirme oyunu aşağıdaki gibi çalışır:  
  
1. Oyuncu gizli simge içeren karelerden birini seçtiğinde, program simge rengini siyaha dönüştürerek bu simgeyi oyuncuya gösterir.  
  
2. Oyuncu daha sonra başka bir gizli simge seçer.  
  
3. Simgeler eşleşirse görünür olarak kalırlar. Aksi takdirde iki simge de tekrar gizlenir.  
  
   Programınızın bu şekilde çalışmasını sağlamak için, seçilen etiketin rengini değiştiren bir Tıklama olayı işleyicisi eklersiniz.  
  
### <a name="to-add-a-click-event-handler-to-each-label"></a>Her etikete bir Tıklama olayı işleyicisi eklemek için  
  
1. Formu Windows Form Tasarımcısı'nda açın. Çözüm Gezgini'nde Form1.cs veya Form1.vb öğesini seçin. Menü çubuğunda, **görünümü**, **Tasarımcısı**.  
  
2. İlk etiket denetimini belirleyip seçin. Ardından CTRL tuşunu basılı tutarken diğer etiketleri tek tek belirleyip seçin. Her etiketin seçildiğinden emin olun.  
  
3. Seçin **olayları** araç çubuğunda düğme **özellikleri** penceresini görüntülemek için **olayları** sayfasını **özellikleri** penceresi. Ekranı aşağı kaydırarak **tıklayın** olay girin **label_Click** kutusunda, aşağıdaki resimde gösterildiği gibi.  
  
     ![Click gösteren Özellikler penceresi olay](../ide/media/express-labelclick.png "Express_labelClick")  
Tıklama olayını gösteren Özellikler penceresi  
  
4. ENTER tuşunu seçin. IDE adında bir tıklama olayı işleyicisi ekler `label_Click()` koda ve bunu formdaki etiketlerin her kancaları.  
  
5. Kodun geri kalanını aşağıdaki gibi doldurun:  
  
     [!code-csharp[VbExpressTutorial4Step2_3_4#4](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial4step2_3_4/cs/form1.cs#4)]
     [!code-vb[VbExpressTutorial4Step2_3_4#4](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial4step2_3_4/vb/form1.vb#4)]  
  
    > [!NOTE]
    >  Kopyalar ve yapıştırırsanız `label_Click()` varolan değiştirdiğinizden emin kodu el ile girmek yerine kod bloğunu `label_Click()` kod. Aksi takdirde, yinelenen bir kod bloğu ile karşı karşıya kalırsınız.  
  
    > [!NOTE]
    >  Size tanıdık gelebilir `object sender` olarak kullanılan hizmet örneğiyle aynı olay işleyicisinin üst [öğretici 2: Bir zaman aşımına matematik sınavı oluşturma](../ide/tutorial-2-create-a-timed-math-quiz.md) öğretici. Tek bir olay işleyicisi yöntemine farklı etiket denetimi Tıklama olayı tutturduğunuzdan, kullanıcının seçtiği etiket hangisi olursa olsun aynı yöntem çağrılır. Olay işleyicisi yöntemi adı kullanması için hangi etiketin seçildiğini bilmesi gerekir **gönderen** etiket denetimini tanımlamak için. Yöntemin ilk satırında program, olmayan genel bir nesne, ancak özellikle bir etiket denetimi olduğunu ve adını kullandığını söyler **clickedLabel** etiketin özelliklerine ve yöntemlere erişmek için.  
  
     Bu yöntem ilk denetler olmadığını **clickedLabel** başarıyla dönüştürüldü (bir nesneden bir etiket kontrolüne atama). Başarısız bir değeri olup olmadığını `null` (C#) veya `Nothing` (Visual Basic) ve yöntemde kodun geri kalanını yürütmek istemiyorsanız. Ardından, yöntem etiketin kullanarak seçilen etiketin metin rengini denetler **ForeColor** özelliği. Etiketin metin rengi siyah ise, simge zaten seçilmiş ve yöntem bitmiş demektir. (Budur `return` deyiminin yaptığı: Bu programa yöntemi yürütmeyi durdurmasını söyler.) Aksi takdirde simge seçilmemiş demektir ve dolayısıyla program etiketin metin rengini siyah olarak değiştirir.  
  
6. Menü çubuğunda, **dosya**, **Tümünü Kaydet** ilerlemenizi kaydedin ve ardından menü çubuğunda, **hata ayıklama**, **hata ayıklamayı Başlat** çalıştırmak için programınızı. Mavi arka planlı boş bir form görmeniz gerekir. Formdaki hücrelerden herhangi birini seçtiğinizde, simgelerden birinin görünür hale gelmesi gerekir. Formda farklı yerler seçmeye devam edin. Siz simgeleri seçtikçe görünmeleri gerekir.  
  
### <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için  
  
- Sonraki öğretici adımına gitmek için bkz: [5. adım: Etiket başvuruları ekleme](../ide/step-5-add-label-references.md).  
  
- Önceki öğretici adımına dönmek için bkz: [3. adım: Her etikete rasgele simge atama](../ide/step-3-assign-a-random-icon-to-each-label.md).
