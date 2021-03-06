---
title: Visual Studio için Unity için Mac araçları kullanarak
description: Bu kılavuz, Mac araçları için Unity uzantısı için Visual Studio kullanmayı açıklar
author: therealjohn
ms.author: johmil
ms.date: 06/18/2019
ms.assetid: 83FDD7A3-5D16-4B4B-9080-078E3FB5C623
ms.openlocfilehash: daffb7721164ae49888a894bec7cad3ac74801a4
ms.sourcegitcommit: 7fbfb2a1d43ce72545096c635df2b04496b0be71
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/09/2019
ms.locfileid: "67692213"
---
# <a name="using-visual-studio-for-mac-tools-for-unity"></a>Visual Studio için Unity için Mac araçları kullanarak

Bu bölümde, Visual Studio Mac araçları için Unity'nın tümleştirme ve verimlilik özellikleri için nasıl kullanacağınızı ve Mac hata ayıklayıcının Unity geliştirme için Visual Studio kullanmayı öğreneceksiniz.

## <a name="opening-unity-scripts-in-visual-studio-for-mac"></a>Mac için Visual Studio'da Unity betikleri açma

Mac için Visual Studio olduğunda [Unity için dış betik düzenleyicisi olarak](setup-vsmac-tools-unity.md#configure-unity-for-use-with-visual-studio-for-mac), Unity Düzenleyicisi'nden herhangi bir komut dosyası açılırken otomatik olarak başlatılır veya seçilen betik anahtarıyla Mac için Visual Studio'yu açın.

Alternatif olarak, Mac için Visual Studio komut dosyası içermeyen kaynak düzenleyicide açık seçerek açılabilir **C# proje Aç** gelen **varlıklar** Unity menüsünde.

![C# proje Aç](media/using-vsmac-tools-unity-image1.png)

## <a name="unity-documentation-access"></a>Unity belgeleri erişimi

Unity için Araçlar Mac için Visual Studio Unity API belgelerini erişmek için bir kısayol içerir. Mac için Visual Studio Unity API belgelerini erişmek için Unity hakkında bilgi edinin ve basın istediğiniz API imleci **⌘ komut + '** .

## <a name="intellisense-for-unity-messages"></a>Unity özellikleri için IntelliSense
Unity altyapısı MonoBehaviour betikleri, geliştiricilerin OnMouseDown, OnTriggerEnter vb. gibi iletileri tepki verdiğini kod yazmak iletileri yayınlar. Bu temel MonoBehaviour sınıfta sanal yöntemleri olmadığından, Unity iletileri için kod Tamamlama işlevi MonoDevelop gibi bazı IDE özellikleri mevcut değildir.

Ancak, Visual Studio için Unity için Mac araçları Unity iletileri için IntelliSense işlevselliği genişletir. Unity iletilerini Uygula MonoBehaviour betiklerde daha kolay hale getirir ve Unity API öğrenmeye yardımcı olur. Unity iletileri için IntelliSense kullanmak için:

1. MonoBehaviour türetilen bir sınıfın gövdesi içinde yeni bir satıra imleci yerleştirin.

2. Gibi bir Unity adını yazmaya başlama iletisi `OnTriggerEnter`.

3. Harf "**ont**" bir IntelliSense Öneri listesi görünür girilmiş.

   ![IntelliSense Kullanma](media/using-vsmac-tools-unity-image2.png)

4. Seçim listesindeki üç yolla değiştirilebilir:

   * İle **yukarı** ve **aşağı** ok tuşları.

   * İstenen öğe üzerinde fare ile tıklayarak.

   * İstenen öğe adı devam ederek.

5. IntelliSense, tüm gerekli parametreleri de dahil olmak üzere seçili Unity ileti ekleyebilirsiniz:

   * Tuşuna basarak **sekmesini**.

   * Tuşuna basarak **dönüş**.

   * Seçili öğeyi çift tıklayarak.

   ![Unity iletisi IntelliSense'de Ekle](media/using-vsmac-tools-unity-image3.png)

## <a name="adding-new-unity-files-and-folders"></a>Yeni Unity dosyaları ve klasörleri ekleme

Unity Düzenleyicisi'nde bir Unity projesi için her zaman yeni dosyaları ekleyebilirsiniz, ancak yeni Unity betikleri, gölgelendiricilerin, yapılar, numaralandırmalar ve klasörlerinden Visual Studio'dan kolayca oluşturmak için Mac için Visual Studio sağlar.

### <a name="add-a-new-c-monobehaviour-script"></a>Yeni bir C# MonoBehaviour betik Ekle

Yeni bir C# MonoBehaviour komut dosyası eklemek için **varlıklar klasörüne sağ** veya çözüm bölmesi seçip dizinlerinden biri **Ekle > Yeni MonoBehaviour**.

![Yeni MonoBehaviour Ekle](media/using-vsmac-tools-unity-image4.png)

### <a name="add-a-new-unity-shader"></a>Yeni bir Unity gölgelendirici ekleme

Yeni bir Unity gölgelendirici eklemek için **varlıklar klasörüne sağ** veya bir alt çözüm bölmesi seçip **Ekle > Yeni gölgelendirici**.

### <a name="add-a-new-folder"></a>Yeni bir klasör Ekle

Yeni bir klasör eklemek için **varlıklar klasörüne sağ** veya bir alt çözüm bölmesi seçip **Ekle > Yeni klasör**.

Bu eklemeler, Unity editor proje penceresinde yansıtılır.

### <a name="to-rename-a-file-or-folder"></a>Bir dosya veya klasörü yeniden adlandırmak için
**sağ** seçin ve çözümde yeniden adlandırmak için öğeye paneli **yeniden adlandır...** .

> [!NOTE]
> Betik ile yeni bir Unity projesi varsa ve varlıklar klasörü Visual Studio'da Çözüm panelinde Mac için görünmez, bir ilk C# betiği Unity editor'ı ekleyin.

## <a name="unity-debugging"></a>Unity hata ayıklama

Mac için Visual Studio ile Unity projeleri ayıklanabilir

### <a name="start-debugging"></a>Hata Ayıklamayı Başlat

Hata ayıklamayı başlatmak için:

1. Tıklayarak, Unity için Visual Studio connect **Play** düğmesini veya türü **Command + Return**, veya **F5**.

   ![Visual Studio'da Yürüt'e tıklayın](media/using-vsmac-tools-unity-image5.png)

2. Geçiş'i tıklatın ve Unity ile **Play** Düzenleyici'de oyuna çalıştırmak için düğme.

   ![Unity Yürüt'e tıklayın](media/using-vsmac-tools-unity-image6.png)

3. Oyun bağlıyken, Visual Studio için Unity Düzenleyicisi'nde çalışırken karşılaşılan herhangi bir kesme noktası oyun yürütülmesini Duraklat ve burada oyun Mac için Visual Studio'da kesme noktası isabet kod satırının getirecek

### <a name="start-debugging-in-a-single-step"></a>Tek bir adımda hata ayıklamayı Başlat

Başlangıç hata ayıklama ve Unity editor yürütmeyi tamamlanabileceğini tek bir adımda Visual Studio'dan doğrudan Mac için seçerek **ekleme Unity ve Yürüt** yapılandırma.

![Unity ve Play seçin ekleyin](media/using-vsmac-tools-unity-image8.png)

### <a name="stop-debugging"></a>Hata ayıklamayı Durdur

Hata ayıklamayı durdurmak için:

1. Tıklayın **Durdur** düğmesine basın veya Mac için Visual Studio'daki **Shift + Command + dönüş**.

   ![Visual Studio'da Durdur'u tıklatın](media/using-vsmac-tools-unity-image7.png)

> [!NOTE]
> Kullanarak hata ayıklama başlattıysanız **ekleme Unity ve Yürüt** Yapılandırması **Durdur** düğmesi de Unity durdurun.

Mac için Visual Studio'da hata ayıklama hakkında daha fazla bilgi için bkz: [hata ayıklayıcıyı kullanma](debugging.md).
