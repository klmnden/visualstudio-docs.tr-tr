---
title: Klavye kısayollarını tanımlama ve özelleştirme
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- VS.ToolsOptionsPages.Environment.Keyboard
helpviewer_keywords:
- keyboard shortcuts [Visual Studio], customizing
- importing shortcut keys [Visual Studio]
- shortcut key combinations [Visual Studio]
- commands [Visual Studio], shortcut keys
- custom shortcut keys [Visual Studio]
- customizing keyboard shortcuts [Visual Studio]
- exporting shortcut keys [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 140a11e7d118b6ceae98dba4290eba89a500ac5e
ms.sourcegitcommit: 9753c7544cec852ca5efd0834e0956d9e53a5734
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67043386"
---
# <a name="identify-and-customize-keyboard-shortcuts-in-visual-studio"></a>Tanımlamak ve Visual Studio'daki klavye kısayollarını özelleştirme

Visual Studio komutları için kısayollar tanımlayabilir, bu kısayolları özelleştirebilir ve başkalarının kullanması için dışarı aktarabilirsiniz. Birçok kısayol her zaman aynı komutları çağırır, ancak kısayolun davranışı aşağıdaki koşullara göre değişebilir:

- Hangi varsayılan ortam ayarlarını ilk kez, seçtiğiniz Visual Studio'yu açın&mdash;genel geliştirme veya Visual C#. (Değiştirme veya sıfırlama ayarlarınızı hakkında daha fazla bilgi için bkz: [ortam ayarları](environment-settings.md).)

- Kısayolun davranışını özelleştirip özelleştirmediğiniz.

- Kısayolu seçtiğiniz anda içinde bulunduğunuz bağlam. Örneğin, **F2** kısayol çağırır `Edit.EditCell` kullanıp kullanmadığınızı komutu **ayarlar Tasarımcısı** ve çağırdığı `File.Rename` kullanıp kullanmadığınızı komutu **Takım Gezgini** .

Ayarları, özelleştirme ve bağlam bağımsız olarak her zaman bulabilir ve klavye kısayolu Değiştir **seçenekleri** iletişim kutusu. Birkaç düzine komutlar için varsayılan klavye kısayolları da arayabilirsiniz [popüler klavye kısayolları](../ide/default-keyboard-shortcuts-for-frequently-used-commands-in-visual-studio.md). Tüm varsayılan kısayolların tam listesi için (temel **genel geliştirme** ayarları), bkz: [tüm klavye kısayolları](../ide/default-keyboard-shortcuts-in-visual-studio.md).

Bir kısayol bir komuta atanmışsa *genel* bağlam ve diğer bağlamlarda, ilgili kısayol her zaman bu komutu çağırır. Ancak bir kısayol, Genel bağlamda bir komuta ve özel bağlamda farklı bir komuta atanabilir. Böyle bir komutu özel bağlamda kullanırsanız, özel bağlama ilişkin komutu çağırır (Genel bağlama ilişkin komutu çağırmaz).

> [!NOTE]
> Ayarlarınıza ve Visual Studio sürümünüze göre, menü komutlarının adları ve konumları ve iletişim kutularında görünen seçenekler değişik olabilir. Bu sayfa dayanır **genel geliştirme** ayarları profili.

## <a name="identify-a-keyboard-shortcut"></a>Klavye kısayolu tanımlama

1. Menü çubuğunda, **Araçları** > **seçenekleri**.

2. Genişletin **ortam**ve ardından **klavye**.

   ![Seçenekler iletişim kutusundaki görüntüleme klavye kısayolları](../ide/media/optionskeyboard.png)

3. İçinde **içeren komutları göster** kutusuna, boşluk olmadan komutun adını bir kısmını veya tamamını girin.

   Örneğin, için komutları bulabilirsiniz `solutionexplorer`.

4. Listede doğru komutu seçin.

    Örneğin, seçebileceğiniz `View.SolutionExplorer`.

5. Komutun bir klavye kısayolu varsa görünür **seçili komut için kısayollar** listesi.

   ![Belirtilen komut için bir kısayol görüntüleyin](../ide/media/viewshortcut.png)

## <a name="customize-a-keyboard-shortcut"></a>Klavye kısayolunu özelleştirme

1. Menü çubuğunda, **Araçları** > **seçenekleri**.

2. Genişletin **ortam**ve ardından **klavye**.

3. İsteğe bağlı: Adı, boşluk olmadan komut bir kısmını veya tamamını girerek komutların listesini filtrelemek **içeren komutları göster** kutusu.

4. Listede, klavye kısayolu atamak istediğiniz komutu seçin.

   İçinde **kullanım yeni kısayolu şunun içinde** listesinde, kısayolu kullanmak istediğiniz özellik alanını seçin.

   Örneğin, seçebileceğiniz **genel** kısayolun her bağlamda çalışmasını istiyorsanız. Başka bir düzenleyicide Genel olarak eşlenmemiş herhangi bir kısayolu kullanabilirsiniz. Aksi takdirde düzenleyici kısayolu geçersiz kılar.

   > [!NOTE]
   > Bir klavye kısayolunu parçası olarak şu tuşları atayamazsınız **genel**:
   >
   > - Sekme, Caps Lock girin
   > - Ekran/Sys Rq, Scroll Lock, Pause/Break yazdırma
   > - INSERT, Home, End, Page Up, Page Down
   > - Windows logosu tuşu, uygulama anahtarı herhangi bir ok tuşları
   > - Num Lock, Delete veya sayısal tuş takımındaki temizleyin
   > - Ctrl + Alt + Delete tuş bileşimi

6. İçinde **kısayol tuşlarına basın** kutusunda, kullanmak istediğiniz kısayolu girin.

    > [!NOTE]
    > Bir harf ile birleştiren bir kısayol oluşturabilirsiniz **Alt** anahtar **Ctrl** tuşu veya her ikisi de. Birleştiren bir kısayol da oluşturabilirsiniz **Shift** anahtarı ve bir harf ile **Alt** anahtar **Ctrl** tuşu veya her ikisi de.

     Bir kısayol zaten başka bir komuta atanmışsa görünür **şu anda kullandığı kısayolunu** kutusu. Bu durumda, seçin **geri** başka bir denemeden önce kısayolu silmek için anahtar.

    ![Bir komut için farklı bir kısayol belirtin](../ide/media/reassignshortcut.png)

7. Seçin **atama** düğmesi.

    > [!NOTE]
    > Bir komut için farklı bir kısayol belirtirseniz, tıklayın **atama**ve ardından **iptal** iletişim kutusunu kapatmak için size atanmış kısayol alınmaz.

## <a name="share-custom-keyboard-shortcuts"></a>Özel klavye kısayollarını paylaşma

Özel klavye kısayollarınızı bir dosyaya dışarı aktararak ve verileri içeri aktarabilmeleri için bu dosyayı başkalarına vererek, klavye kısayollarınızı paylaşabilirsiniz.

### <a name="to-export-only-keyboard-shortcuts"></a>Yalnızca klavye kısayollarını dışarı aktarmak için

1. Menü çubuğunda, **Araçları** > **içeri ve dışarı aktarma ayarları**.

2. Seçin **seçili ortam ayarlarını dışarı aktar**ve ardından **sonraki**.

3. Altında **hangi ayarları dışarı aktarmak istiyor musunuz?** temizleyin **tüm ayarlar** onay kutusunu işaretleyin, genişletme **seçenekleri**ve ardından **ortam**.

4. Seçin **klavye** onay kutusunu işaretleyin ve ardından **sonraki**.

   ![Yalnızca özel klavye kısayollarını dışarı aktarma](../ide/media/exportshortcuts.png)

5. İçinde **ne ayarlar dosyanıza ad verin istiyorsanız** ve **ayarlarımı bu dizinde Store** kutularında ya da varsayılan değerleri bırakın veya farklı değerler belirtin ve ardından **son** .

::: moniker range="vs-2017"

Varsayılan olarak, kısayollarınızı bir dosyaya kaydedilir *%USERPROFILE%\Documents\Visual Studio 2017\Settings* klasör. Dosyanın adı ayarları dışarı aktardığınız ve uzantı tarihi yansıtır *.vssettings*.

::: moniker-end

::: moniker range=">=vs-2019"

Varsayılan olarak, kısayollarınızı bir dosyaya kaydedilir *%USERPROFILE%\Documents\Visual Studio 2019\Settings* klasör. Dosyanın adı ayarları dışarı aktardığınız ve uzantı tarihi yansıtır *.vssettings*.

::: moniker-end

### <a name="to-import-only-keyboard-shortcuts"></a>Yalnızca klavye kısayollarını içeri aktarmak için

1. Menü çubuğunda, **Araçları** > **içeri ve dışarı aktarma ayarları**.

2. Seçin **seçili ortam ayarlarını içeri aktarma** seçenek düğmesini ve ardından **sonraki**.

3. Seçin **Hayır, sadece yeni ayarları, geçerli ayarlarımı alma** seçenek düğmesini ve ardından **sonraki**.

4. Altında **ayarlarım**, içeri aktarma veya seçmek istediğiniz kısayolları içeren dosyayı seçin **Gözat** doğru dosyayı bulmak için düğme.

5. Seçin **sonraki**.

6. Altında **hangi ayarları içeri aktarmak istiyor musunuz?** temizleyin **tüm ayarlar** onay kutusunu işaretleyin, genişletme **seçenekleri**ve ardından **ortam**.

7. Seçin **klavye** onay kutusunu işaretleyin ve ardından **son**.

   ![Yalnızca özel klavye kısayollarını içeri aktarma](../ide/media/importshortcuts.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'nun erişilebilirlik özellikleri](../ide/reference/accessibility-features-of-visual-studio.md)