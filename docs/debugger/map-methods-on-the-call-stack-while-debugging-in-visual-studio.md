---
title: Çağrı yığınının görsel haritasını oluşturun | Microsoft Docs
ms.date: 11/26/2018
ms.topic: conceptual
f1_keywords:
- vs.progression.debugwithcodemaps
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- call stacks, code maps
- Call Stack window, mapping calls
- debugging [Visual Studio], diagramming the call stack
- call stacks, mapping
- Call Stack window, visualizing
- debugging code visually
- debugging [Visual Studio], mapping the call stack
- call stacks, visualizing
- debugging, code maps
- Call Stack window, tracing calls visually
- Call Stack window, show on code map
- debugging [Visual Studio], tracing the call stack visually
- debugging [Visual Studio], visualizing the call stack
ms.assetid: d6a72e5e-f88d-46fc-94a3-1789d34805ef
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 62fb77590a20b0e31648cab10f310851fd65820e
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70179999"
---
# <a name="create-a-visual-map-of-the-call-stack-while-debugging-c-visual-basic-c-javascript"></a>Hata ayıklarken çağrı yığınının görsel haritasını oluşturma (C#, Visual Basic, C++JavaScript)

Hata ayıklarken çağrı yığınını görsel olarak izlemek için bir kod Haritası oluşturun. Kodun ne yaptığını izlemek için haritada Not oluşturabilir, böylece hataları bulmaya odaklanırsınız.

İzlenecek yol için şu videoyu izleyin: [Video Kod Haritası hata ayıklayıcısı tümleştirmesiyle görsel hata ayıkla (Channel 9)](http://go.microsoft.com/fwlink/?LinkId=293418)

Kod haritaları ile kullanabileceğiniz komutların ve eylemlerin ayrıntıları için bkz. [kod haritalarını inceleyin ve yeniden düzenleyin](../modeling/browse-and-rearrange-code-maps.md).

>[!IMPORTANT]
>Yalnızca [Visual Studio Enterprise sürümünde](https://visualstudio.microsoft.com/downloads)kod haritaları oluşturabilirsiniz.

İşte bir kod haritasına hızlı bakış:

 ![Kod haritalarına çağrı yığınları ile hata ayıklama](../debugger/media/debuggermap_overview.png "DebuggerMap_Overview")

## <a name="MapStack"></a> Çağrı yığınını eşleme

1. C#Bir Visual Studio Enterprise, Visual Basic C++, veya JavaScript projesinde hata **Ayıkla** > başlatma hata**ayıklamayı Başlat** ' ı seçerek veya **F5**tuşuna basarak hata ayıklamayı başlatın.

1. Uygulamanız kesme moduna girdiğinde veya bir işleve adımladıktan sonra, **hata ayıklama** >  **`** **kod Haritası**' nı seçin veya **CTRL**+**SHIFT**+tuşuna basın.

   Geçerli çağrı yığını yeni bir kod haritası üzerinde turuncu renkte görüntülenir:

   ![Bkz: kod haritasında çağrı yığınını](../debugger/media/debuggermap_seeundocallstack.png "DebuggerMap_SeeUndoCallStack")

Kod eşleme, hata ayıklamaya devam ederken otomatik olarak güncelleştirilir. Harita öğelerini veya yerleşimini değiştirmek kodu herhangi bir şekilde etkilemez. Haritadaki herhangi bir şeyi rahatça yeniden adlandırabilir, taşıyabilir veya kaldırabilirsiniz.

Bir öğe hakkında daha fazla bilgi edinmek için, üzerine gelin ve öğenin araç ipucuna bakın. Her simgenin ne anlama geldiğini öğrenmek için araç çubuğunda **gösterge** ' ı da seçebilirsiniz.

![Kod Haritası göstergesi](../debugger/media/debuggermap_showlegend.png "Kod Haritası göstergesi")

>[!NOTE]
>Diyagramda, kod eşlemesinin en üstündeki **kodun eski bir sürümünü temel alan bir** ileti, Haritayı son güncelleştirdikten sonra kodun değişmiş olabileceği anlamına gelir. Örneğin, harita üzerindeki bir çağrı artık kodda bulunmayabilir. İletiyi kapatın ve haritayı yeniden güncelleştirmeden önce çözümü yeniden oluşturmayı deneyin.

## <a name="map-external-code"></a>Dış kod eşleme

Varsayılan olarak, yalnızca kendi kodunuzu harita üzerinde görüntülenir. Haritada dış kodu görmek için:

- **Çağrı yığını** penceresine sağ tıklayın ve **dış kodu göster**' i seçin:

  ![Çağrı yığını penceresini kullanarak dış kod görüntüleme](../debugger/media/debuggermap_callstackmenu.png "DebuggerMap_CallStackMenu")
- Ya da Visual Studio **araçlarında** **yalnızca kendi kodum etkinleştir** seçimini kaldırın (veya **hata ayıklama**) > **Seçenekler** > **hata ayıklama**:

  ![Seçenekler iletişim kutusunu kullanarak dış Kodu Göster](../debugger/media/debuggermap_debugoptions.png "DebuggerMap_DebugOptions")

## <a name="control-the-maps-layout"></a>Haritanın yerleşimini denetleme

Haritanın düzeninin değiştirilmesi, kodu herhangi bir şekilde etkilemez.

Haritanın yerleşimini denetlemek için harita araç çubuğunda **Düzen** menüsünü seçin.

**Düzen** menüsünde şunları yapabilirsiniz:

- Ekran düzenini değiştirin.
- **Hata ayıklama sırasında otomatik olarak düzen**seçimini kaldırarak Haritayı otomatik olarak yeniden düzenlemeyi durdurun.
- **Artımlı düzenin**seçimini kaldırarak eşlemeyi öğe eklediğinizde mümkün olduğunca az yeniden düzenleyin.

## <a name="MakeNotes"></a> Kodla ilgili notlar alın

Kodda neler olduğunu izlemek için yorum ekleyebilirsiniz.

Bir açıklama eklemek için, kod haritasına sağ tıklayın ve**Yeni yorumu** **Düzenle** > ' yi seçin ve ardından yorumu yazın.

Açıklamaya yeni bir satır eklemek için **SHIFT**+**ENTER**tuşuna basın.

 ![Kod haritasında çağrı yığını için açıklama ekleme](../debugger/media/debuggermap_addcomment.png "DebuggerMap_AddComment")

## <a name="UpdateMap"></a> Sonraki çağrı yığını ile eşlemeyi güncelleyin

Uygulamanızı sonraki kesme noktasında çalıştırdığınız veya bir işleve adımla, eşleme otomatik olarak yeni çağrı yığınları ekler.

![Sonraki çağrı yığını ile güncelleştirme kod Haritası](../debugger/media/debuggermap_addclearcallstack.png "DebuggerMap_AddClearCallStack")

Haritanın otomatik olarak yeni çağrı yığınları eklemesini durdurmak için, kod haritasında ![çağrı yığınını göster]' i seçerek kod Haritası araç çubuğunda kod eşlemesinde(../debugger/media/debuggermap_automaticupdateicon.gif "çağrı yığınını") otomatik olarak göster ' i seçin. Eşleme, varolan çağrı yığınlarını vurgulamaya devam eder. Geçerli çağrı yığınını eşlemeye el ile eklemek için basın **Ctrl**+**Shift**+ **`** .

## <a name="AddRelatedCode"></a> Eşlemeye ilgili kodu ekleyin

C# Ya da Visual Basic bir haritanız olduğuna göre, kodda neler olduğunu izlemek için alanlar, Özellikler ve diğer yöntemler gibi öğeleri de ekleyebilirsiniz.

Koddaki yöntemin tanımına gitmek için haritadaki yönteme çift tıklayın veya seçin, **F12**tuşuna basın veya sağ tıklayın ve **Tanıma Git**' i seçin.

![Kod haritasında bir yöntem için kod tanımı Git](../debugger/media/debuggermap_gotocodedefinition.png "DebuggerMap_GoToCodeDefinition")

Haritaya izlemek istediğiniz öğeleri eklemek için bir yönteme sağ tıklayın ve izlemek istediğiniz öğeleri seçin. En son eklenen öğeler yeşil görünür.

![Metoda çağrı yığınını kod haritasında ilgili alanları](../debugger/media/debuggermap_showedfields.png "DebuggerMap_ShowedFields")

>[!NOTE]
>Varsayılan olarak, öğeleri haritaya ekleme sınıfı, ad alanı ve derlemeye gibi üst düğümleri gruplandırma ekler. Kod Haritası araç çubuğunda **üst öğeleri dahil et** düğmesini seçerek veya öğe eklerken **CTRL** tuşuna basarak bu özelliği devre dışı bırakabilirsiniz.

![Çağrı yığınını kod Haritası üzerinde bir yöntemi alanları gösterin](../debugger/media/debuggermap_showfields.png "DebuggerMap_ShowFields")

Daha fazla kod görmek için haritayı oluşturmaya devam edin.

 ![Bir alanı kullanan yöntemlerine bakın: çağrı yığınını kod Haritası](../debugger/media/debuggermap_findallreferences.png "DebuggerMap_FindAllReferences")

 ![Çağrı yığınını kod haritasında bir alanı kullanan yöntemleri](../debugger/media/debuggermap_foundallreferences.png "DebuggerMap_FoundAllReferences")

## <a name="FindBugs"></a> Eşlemeyi kullanarak hataları bulun
 Kodunuzu görselleştirmeniz, hataları daha hızlı şekilde bulmanıza yardımcı olabilir. Örneğin, bir çizim uygulamasında bir hatayı araştırdığınızı varsayalım. Bir çizgi çizip geri almayı denediğinizde, başka bir çizgi çizinceye kadar hiçbir şey olmaz.

 Kesme noktaları ayarlamak için `clear`, `undo`, ve `Repaint` yöntemleri, hata ayıklamayı başlatmak ve bunun gibi bir harita oluşturur:

 ![Başka bir çağrı yığınını kod Haritası eklemek](../debugger/media/debuggermap_addpaintobjectcallstack.png "DebuggerMap_AddPaintObjectCallStack")

 Harita çağrısında tüm kullanıcı hareketlerine dikkat edin `Repaint`, dışında `undo`. Yaramamasının nedeni `undo` hemen işe yaramaz.

 Hatayı düzelttikten ve uygulamayı çalıştırmaya devam ettikten sonra, eşleme kaynağından `undo` `Repaint`yeni çağrıyı ekler:

 ![Yeni yöntemi çağrısı için çağrı yığınını kod haritasında eklemek](../debugger/media/debuggermap_addnewcallforrepaint.png "DebuggerMap_AddNewCallForRepaint")

## <a name="share-the-map-with-others"></a>Haritayı başkalarıyla paylaşma

Bir Haritayı dışarı aktarabilir, Microsoft Outlook ile başka bir kişiye gönderebilir, çözümünüze kaydedebilir ve sürüm denetimine iade edebilirsiniz.

Haritayı paylaştırmak veya kaydetmek için, kod Haritası araç çubuğunda **paylaşma** ' yı kullanın.

![Çağrı yığını kod haritasını başkalarıyla paylaşma](../debugger/media/debuggermap_sharewithothers.png "Çağrı yığını kod haritasını başkalarıyla paylaşma")

## <a name="see-also"></a>Ayrıca bkz.
[Çözümlerinizdeki bağımlılıkları eşleme](../modeling/map-dependencies-across-your-solutions.md)

[Uygulamalarınızda hata ayıklamak için kod haritalarını kullanma](../modeling/use-code-maps-to-debug-your-applications.md)

[Kod haritası çözümleyicilerini kullanarak olası sorunları bulma](../modeling/find-potential-problems-using-code-map-analyzers.md)

[Kod haritalarına göz atma ve bunları yeniden düzenleme](../modeling/browse-and-rearrange-code-maps.md)
