---
title: Hata ayıklayıcıda izleme noktalarını kullanma | Microsoft Docs
ms.date: 9/17/2019
ms.topic: conceptual
helpviewer_keywords:
- tracepoints, about tracepoints
author: Sagar-S-S
ms.author: sashe
manager: AndSter
ms.workload:
- multiple
ms.openlocfilehash: 7680b305fad6f8ea1d7961ec5a70ddafd578c77d
ms.sourcegitcommit: 6993bcb0d2b0067b1b7b7899bfba52c31c70b7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2019
ms.locfileid: "71095259"
---
# <a name="use-tracepoints-in-the-visual-studio-debugger"></a>Visual Studio hata ayıklayıcısında izlenesel noktaları kullanma

İzleneme noktaları, kodunuzu değiştirmeden veya durdurmadan, yapılandırılabilir koşullar altındaki çıkış penceresine bilgi günlüğizin verir. Bu özellik hem yönetilen hem de yerel kod için, JavaScript ve C#gibi çeşitli diller için desteklenir.

## <a name="let39s-take-an-example"></a>&#39;Bir örnek alalım

Aşağıdaki örnek program, bir sayaç değişkeni `for` olan ve döngünün başka bir yinelemeyi her çalıştırdığında arttığı basit bir döngüdür.

![Sayaç örneği](../debugger/media/counterexample.png "Sayaç örneği")

## <a name="set-tracepoints-in-source-code"></a>Kaynak kodunda izleme noktalarını ayarlama

**Kesme noktası ayarları** penceresindeki **eylem** onay kutusunun altında bir çıktı dizesi belirterek izleme noktaları ayarlayabilirsiniz.

1. Bir izleme noktası başlatmak için, önce izleme noktasını ayarlamak istediğiniz satır numarasının solundaki cilt paya tıklayın.

   ![Kesme noktası Başlatma](../debugger/media/breakpointinitialization.png "Kesme noktası Başlatma")

2. Kırmızı dairenin üzerine gelin ve ardından dişli simgesine tıklayın.
3. Bu, **kesme noktası ayarları** penceresini açar.

   ![Kesme noktası penceresi](../debugger/media/breakpointwindow.png "Kesme noktası penceresi")

4. **Eylem** onay kutusunu seçin.

   ![Denetlenen Eylemler kutusu](../debugger/media/checkedactionsbox.png "Denetlenen Eylemler kutusu")

   Kırmızı dairenin, bir kesme noktasından izleme noktasına geçtiğine işaret eden bir baklava şeklini nasıl değiştirdiğine dikkat edin.

5. Çıkış Penceresi metin kutusunda **Ileti göster** ' e oturum açmak istediğiniz iletiyi girin (Ayrıntılar için, bu makaledeki sonraki bölümlere bakın).

   İzleme noktanız artık ayarlandı. Her şey için&quot; çıkış penceresi bazı bilgileri günlüğe kaydetmek istiyorsanız Kapatdüğmesinebasın.&quot;

6. İletinizin görüntülenip görüntülenmediğini belirten koşullar eklemek istiyorsanız, **koşullar** onay kutusunu seçin.

   ![Denetlenen koşullar kutusu](../debugger/media/checkedconditionsbox.png "Denetlenen koşullar kutusu")

   Koşullar için üç seçeneğiniz vardır: **Koşullu ifade**, **filtre**ve **isabet sayısı**.

## <a name="actions-menu"></a>Eylemler menüsü

Bu menü, çıkış penceresine bir ileti kaydetmenize izin verir. İleti kutusuna çıktısını almak istediğiniz dizeleri yazın (tırnak işareti gerekmez). Değişkenlerin değerlerini göstermek istiyorsanız, küme ayraçları içine aldığınızdan emin olun.

Örneğin, çıkış konsolundaki `counter` değişkenin değerini göstermek istiyorsanız, ileti metin kutusuna {Counter} yazın.

![Sayaç çıkış iletisi](../debugger/media/counteroutputmessage.png "Sayaç çıkış iletisi")

**Kapat** ' a tıklayıp programda hata ayıklaması yaparsanız (**F5**) çıkış penceresinde aşağıdaki çıktıyı görürsünüz.

![Çıkış penceresi eylemler iletisi](../debugger/media/actionsmessageinoutputwindow.png "Çıkış penceresi eylemler iletisi")

Daha belirli bilgileri göstermek için özel anahtar sözcükler de kullanabilirsiniz. Anahtar sözcüğünü aşağıda gösterildiği gibi tam olarak girin (her anahtar sözcüğünün önünde bir "$" kullanın ve anahtar sözcüğünün kendisi için tüm Cap 'ler).

| Anahtar sözcüğü | Ne görüntülenir |
| --- | --- |
| $ADDRESS | Geçerli yönerge |
| $CALLER | İşlev adı çağırma |
| $CALLSTACK | Çağrı yığını |
| $FUNCTION | Geçerli işlev adı |
| $PID | İşlem kimliği |
| $PNAME | İşlem adı |
| $TID | İş parçacığı kimliği |
| $TNAME   | İş parçacığı adı |
| $TICK | Değer sayısı (Windows GetTickCount 'tan) |

## <a name="conditions-menu"></a>Koşullar menüsü

Koşullar, çıkış iletilerinizi filtrelemenizi sağlar, böylece yalnızca belirli senaryolar altında görüntülenir. Kullanabileceğiniz üç ana koşul türü vardır.

### <a name="conditional-expression"></a>Koşullu ifade
Koşullu bir ifade için, yalnızca belirli koşullar karşılandığında bir çıkış iletisi görüntülenir.

Koşullu ifadeler için, izleme noktasını, belirli bir koşul doğru olduğunda ya da değiştirildiğinde bir iletiyi çıktı olarak ayarlayabilirsiniz. Örneğin, yalnızca `for` döngünün çift yinelemeleri sırasında sayacın değerini göstermek istiyorsanız, **true** seçeneğini seçip ileti metin kutusuna yazabilirsiniz `i%2 == 0` .

![Koşullu Ifade doğru](../debugger/media/conditionalexpressionistrue.png "Koşullu Ifade doğru")

`for` Döngü yinelemesi değiştiğinde sayacın değerini yazdırmak istiyorsanız, **ne zaman değiştirildi** seçeneğini belirleyin ve ileti metin kutusuna yazın `i` .

![Değiştirildiğinde koşullu ifade](../debugger/media/conditionalexpressionwhenchanged.png "Değiştirildiğinde koşullu ifade")

Farklı programlama dilleri için **ne zaman değiştirildi** seçeneğinin davranışı farklıdır.

- Yerel kod için, hata ayıklayıcı koşulun ilk değerlendirmesini bir değişiklik olacak şekilde düşünmez, bu nedenle ilk değerlendirmede izleme noktasına ulaşmaz.
- Yönetilen kod için, hata ayıklayıcı, **değişiklik** seçildikten sonra ilk değerlendirmede izleme noktasını alır.

Koşulları ayarlarken kullanabileceğiniz geçerli ifadelere daha kapsamlı bir bakış için bkz [. Hata Ayıklayıcıdaki İfadeler](expressions-in-the-debugger.md)

### <a name="hit-count"></a>İsabet sayısı
İsabet sayısı koşulu yalnızca izleme noktasının ayarlandığı kod satırıyla belirtilen sayıda yürütülene kadar çıkış göndermenizi sağlar.

İsabet sayısı için, izleme noktasının ayarlandığı kod satırı, ' nin katı olan veya belirtilen isabet sayısı değerinden büyük veya bu değere eşit olan bir dizi kez yürütülebileceği zaman bir iletiyi çıkışı seçebilirsiniz. Gereksinimlerinize en uygun seçeneği belirleyin ve ilgili yinelemeyi temsil eden alana (örneğin, 5) bir tamsayı değeri yazın.

![Koşullu Ifade Isabet sayısı](../debugger/media/conditionalexpressionhitcount.png "Koşullu Ifade Isabet sayısı")

### <a name="filter"></a>Filtrele
Filtre koşulu için, hangi cihazların, işlemlerin veya iş parçacıklarının çıkışın gösterildiğini belirtin.

![Koşullu Ifade filtresi](../debugger/media/conditionalexpressionfilter.png "Koşullu Ifade filtresi")

Filtre ifadeleri listesi:

- MachineName = "name"
- ProcessID = değer
- ProcessName "name" =
- ThreadID = değer
- ThreadName = "name"

Dizeleri (adlar gibi) çift tırnak içine alın. Değerler tırnak işareti olmadan girilebilir. `&` Yan tümceleri (`AND` `||` ),(`NOT`), ()veparantezlerikullanarakbirleştirebilirsiniz.`!` `OR`

## <a name="considerations"></a>Dikkat Edilecekler

İzleme noktaları, temizleyici ve daha sorunsuz bir deneyimde hata ayıklamaya yönelik olarak düşünülirken, bunları kullanmaya ne zaman geldiğini bilmeniz gereken bazı noktalar vardır.

Bazen bir nesnenin bir özelliğini veya özniteliğini incelemenize sonra değeri değişebilir. Bu, izleme noktası özelliğinin kendisinden kaynaklanan bir hata değildir, ancak nesneleri incelemek için izleme noktaları kullanmanın bu yanlışlıkla yapılan değişikliklerden kaçının.

Deyim **eylem** ileti kutusunda değerlendirilme yöntemi, geliştirme için kullanmakta olduğunuz dilden farklı olabilir. Örneğin, bir dizeyi çıkarmak için, normalde veya `Debug.WriteLine()` `console.log()`kullanırken bile bir iletiyi tırnak içine almanız gerekmez. Ayrıca, çıkış ifadelerine küme ayracı sözdizimi`{ }`(), geliştirme dilinizde değer çıktısı için olan kurala göre de farklı olabilir. (Ancak, küme ayraçları (`{ }`) içindeki içerikler hala geliştirme dili sözdizimi kullanılarak yazılmalıdır.

## <a name="see-also"></a>Ayrıca bkz.

- [Hata ayıklıyor?](../debugger/what-is-debugging.md)
- [Daha iyi yazma C# kullanarak Visual Studio code](../debugger/write-better-code-with-visual-studio.md)
- [Hata ayıklama ilk bakış](../debugger/debugger-feature-tour.md)
- [Hata ayıklayıcısındaki ifadeler](expressions-in-the-debugger.md)
- [Kesme noktalarınıullanma](../debugger/using-breakpoints.md)
