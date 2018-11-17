---
title: Görüntüleme veri değerlerini DataTips Kod Düzenleyicisi'nde | Microsoft Docs
ms.custom: ''
ms.date: 07/14/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- debugging [Visual Studio], DataTips
- DataTips tool
ms.assetid: ffa7bd18-439b-4685-a9b3-c7884b5de41f
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: afb318c8aa327345b3cd76ee16b718db1e0386aa
ms.sourcegitcommit: 331dbb12e11fcd7f5d15fab05f3c861e48126e43
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2018
ms.locfileid: "51826771"
---
# <a name="view-data-values-in-datatips-in-the-code-editor"></a>Kod Düzenleyicisi'nde veri değerlerini görüntüleme datatips
DataTips, hata ayıklama sırasında programınızdaki değişkenleri hakkında daha fazla bilgi görüntülemek için kullanışlı bir yol sağlar. DataTips, sadece kesme modunda ve yalnızca yürütme geçerli kapsamdaki değişkenler çalışın. Bu, kodda hata ayıklamak için girişimde ilk kez ise, okumak isteyebilirsiniz [daha iyi yazma C# Visual Studio kullanarak kod](../debugger/write-better-code-with-visual-studio.md) ve [yeni başlayanlar için hata ayıklama](../debugger/debugging-absolute-beginners.md) bu makalede geçmeden önce.
  
### <a name="to-display-a-datatip"></a>Bir DataTip görüntülemek için  
  
1. Bir kesme noktası ayarlayın ve hata ayıklamayı Başlat (basın **F5**).

2. Hata ayıklayıcısında duraklatıldıktan olduğunda, geçerli kapsamdaki herhangi bir değişken üzerinde fare işaretçisi yerleştirin.
  
     Bir DataTip görünür.
  
3.  Fare işaretçisi kaldırdığınızda DataTip kaybolur. Açık kalması DataTip sabitlemek için tıklayın **kaynağına PIN** simgesi veya bir değişken üzerinde sağ tıklatın ardından **kaynağına PIN**.

    ![Bir veri ipucunda sabitleme](../debugger/media/dbg-tips-data-tips-pinned.png "PinningDataTip")

    > [!NOTE]
    > Veri ipuçları, her zaman yürütmesi askıya alınır ve imleç değil geldiği yerde bağlamında değerlendirilir. Geçerli bağlam içinde bir değişken olarak aynı ada sahip başka bir işlev bir değişkende üzerine gelin, diğer işlev değişkenin değeri geçerli bağlamda değişkeninin değeri olarak görüntülenir.
  
### <a name="to-unpin-a-datatip-and-make-it-float"></a>Bir DataTip kaldırın ve kolaylaştırmak için Kaydır  
  
-   Sabitlenmiş bir DataTip içinde tıklayın **kaynağından Unpın** simgesi.  
  
     Raptiye simgesini sabitlenmemiş konuma değişir. DataTip artık açık pencerelerin kayar. Hata ayıklama oturumu sona erdiğinde kayan DataTip kapatır.  
  
### <a name="to-repin-a-floating-datatip"></a>Kayan bir DataTip Görselden için  
  
-   Bir DataTip içinde Raptiye simgesine tıklayın.  
  
     Raptiye simgesini sabitlenmiş konumuna değiştirir. Kaynak penceresi dışında DataTip ise Raptiye simgesini devre dışıdır ve DataTip sabitlenemez.  
  
### <a name="to-close-a-datatip"></a>Bir DataTip kapatmak için  
  
-   Fare işaretçisini bir DataTip üzerinde getirin ve ardından **Kapat** simgesi.  
  
### <a name="to-close-all-datatips"></a>Tüm veri ipuçlarını kapatmak için  
  
-   Üzerinde **hata ayıklama** menüsünde tıklatın **Temizle tüm veri ipuçlarını**.  
  
### <a name="to-close-all-datatips-for-a-specific-file"></a>Belirli bir dosya için tüm veri ipuçlarını kapatmak için  
  
-   Üzerinde **hata ayıklama** menüsünde tıklatın **Temizle tüm veri ipuçlarını sabitlenmiş için** *dosya*.  
  
## <a name="expand-and-edit-information"></a>Genişletin ve bilgilerini Düzenle  
 DataTips, bir dizi, yapı veya üyelerini görüntülemek için bir nesne genişletmek için kullanabilirsiniz. Bir DataTip değişkeninden değerini de düzenleyebilirsiniz.  
  
#### <a name="to-expand-a-variable-to-see-its-elements"></a>Bir değişken öğeleri görmek için genişletin  
  
-   Fare işaretçisini bir DataTip içinde yerleştirin **+** değişken adından önce gelen oturum.  
  
    Öğeleri ağaç biçiminde göstermek için değişkeni genişletir.

    ![Bir veri ipucunda görüntülemek](../debugger/media/dbg-tour-data-tips.gif "bir veri ipucunda görüntüleyin")
  
    Değişken genişletildiğinde klavyenizde yukarı ve aşağı taşımak için ok tuşlarını kullanabilirsiniz. Alternatif olarak, fare kullanabilirsiniz.  
  
#### <a name="to-edit-the-value-of-a-variable-using-a-datatip"></a>Bir DataTip kullanarak bir değişkenin değerini düzenlemek için  
  
1.  Bir DataTip içinde değere tıklayın. Bu salt okunur değerleri için devre dışıdır.  
  
2.  Yeni bir değer yazın ve ENTER tuşuna basın.  
  
## <a name="making-a-datatip-transparent"></a>Bir DataTip saydam hale getirme  
 Bir DataTip kod görmek istiyorsanız, DataTip geçici olarak saydam olarak yapabilirsiniz. Bu sabitlenmiş veya kayan DataTips için geçerli değildir.  
  
#### <a name="to-make-a-datatip-transparent"></a>Bir DataTip saydam yapmak için  
  
-   Bir DataTip içinde CTRL tuşuna basın.  
  
     CTRL tuşunu basılı tutun sürece DataTip saydam olarak kalır.  
  
## <a name="visualize-complex-data-types"></a>Karmaşık veri türleri görselleştirin  
 Bir değişken adı bir veya daha fazla bir DataTip içinde bir Büyüteç simgesinin yanında, [görselleştiriciler](../debugger/create-custom-visualizers-of-data.md), gibi [dize görselleştiriciler](../debugger/string-visualizer-dialog-box.md), söz konusu veri türündeki değişkenler için kullanılabilir. Görselleştirici, genellikle grafik daha anlamlı bir şekilde bilgileri görüntülemek için kullanabilirsiniz.
  
#### <a name="to-view-the-contents-of-a-variable-using-a-visualizer"></a>Görselleştirici kullanarak değişkenlerin içeriğini görüntülemek için  
  
-   Büyüteç simgesine tıklayarak ![VisualizerIcon](../debugger/media/dbg-tips-visualizer-icon.png "Görselleştirici simgesi") veri türü için varsayılan Görselleştirici'ı seçin.  
  
     veya  
  
     Veri türü için uygun görselleştiriciler bir listesinden seçmek için Görselleştirici yanındaki açılır oka tıklayın.  
  
     Görselleştirici bilgileri görüntüler.  
  
## <a name="add-information-to-a-watch-window"></a>İzle penceresine bilgilerini ekleyin  
 Bir liste görünümünde bir değişken izlemek devam etmek istiyorsanız, bir değişkene ekleyebilirsiniz **Watch** bir DataTip penceresinde.  
  
#### <a name="to-add-a-variable-to-the-watch-window"></a>İzle penceresine bir değişken eklemek için  
  
-   Bir DataTip sağ tıklayın ve ardından **Gözcü Ekle**.  
  
     Değişken eklenir **Watch** penceresi. Birden çok destekleyen bir sürüm kullanıyorsanız **Watch** windows, değişkenin eklendiği **Watch 1.**  
  
## <a name="import-and-export-datatips"></a>İçeri aktarma ve veri ipuçlarını Dışarı Aktar  
 Bir iş arkadaşınızla paylaşılabilir veya bir metin düzenleyicisi kullanarak düzenlenebilir bir XML dosyasına veri ipuçlarını dışarı aktarabilirsiniz.  
  
#### <a name="to-export-datatips"></a>Veri ipuçlarını dışarı aktarmak için  
  
1.  Hata Ayıklama menüsünde **veri ipuçlarını dışarı aktar**.  
  
     **Veri ipuçlarını dışarı aktar** iletişim kutusu görüntülenir.  
  
2.  XML dosyasını, dosyasında için bir ad yazın istediğiniz konuma gitmek için standart dosya teknikleri kullanın **dosya adı** kutusuna ve ardından **Tamam**.  
  
#### <a name="to-import-datatips"></a>Veri ipuçlarını içeri aktarmak için  
  
1.  Hata Ayıklama menüsünde **alma DataTips**.  
  
     **Alma DataTips** iletişim kutusu görüntülenir.  
  
2.  İletişim kutusunu açıp istediğiniz XML dosyasını bulmak için kullanın **Tamam**.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklıyor?](../debugger/what-is-debugging.md)  
 [Daha iyi yazma C# kullanarak Visual Studio code](../debugger/write-better-code-with-visual-studio.md)  
 [Hata ayıklama sırasında ilk bakış](../debugger/debugger-feature-tour.md) [hata ayıklayıcısı verilerini görüntüleme](../debugger/viewing-data-in-the-debugger.md)   
 [İzleme ve QuickWatch Windows](../debugger/watch-and-quickwatch-windows.md)   
 [Özel Görselleştirici Oluşturma](../debugger/create-custom-visualizers-of-data.md)   