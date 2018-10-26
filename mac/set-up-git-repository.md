---
title: Bir Git deposu ayarlama
description: Git, Subversion Mac için Visual Studio kullanarak
author: conceptdev
ms.author: crdun
ms.date: 05/06/2018
ms.assetid: E992FA1D-B2AD-4A28-ADC6-47E4FC471060
ms.openlocfilehash: aafa410352be27084f2febecc734c68e4f316d6f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49827967"
---
# <a name="setting-up-a-git-repository"></a>Bir Git deposu ayarlama

Git takımlar aynı belgelerde aynı anda çalışmasına izin veren bir dağıtılmış sürüm denetim sistemidir. Bu, tüm dosyaları içeren tek bir sunucu yoktur, ancak bu kaynaktan bir depo kullanıma her deponun tamamı makinenizde yerel olarak kopyalanmış olan anlamına gelir.

GitHub ancak yaygın bir ana bilgisayardır sürüm denetimi için Git ile çalışmanıza olanak tanıyan çok uzak ana vardır. Aşağıdaki örnek, bir GitHub konak kullanır, ancak Mac için Visual Studio'da sürüm denetimi için herhangi bir Git ana kullanabilirsiniz

GitHub kullanmak istiyorsanız, bir hesap oluşturulur ve bu makaledeki adımları izlemeden önce yapılandırılmış olduğundan emin olun. 

## <a name="creating-a-remote-repo-on-github"></a>GitHub üzerinde uzak bir depo oluşturma

Aşağıdaki örnek, bir GitHub konak kullanır, ancak Mac için Visual Studio'da sürüm denetimi için herhangi bir Git ana kullanabilirsiniz

Bir Git deposu ayarlama için aşağıdaki adımları uygulayın:

1. Github.com yeni Git deposu oluşturun:

    ![Yeni git deposu oluşturma](media/version-control-git1-sml.png)

2. Depo adı, açıklama ve gizlilik ayarlayın. Yapmak **değil** depo başlatın. .Gitignore ve lisans hiçbiri olarak ayarlayın:

    ![Git deposunun kümesi ayrıntıları](media/version-control-git2.png)

3. Sonraki sayfada görüntülemek ve HTTPS ya da SSH adresi oluşturduğunuz depoyu kopyalamak için bir seçenek sunar:

    ![görüntüleme ve kopyalama adresi](media/version-control-git3.png)

   Mac için bu depoya noktası Visual Studio için HTTPS adresi gerekir.


## <a name="publishing-an-existing-project"></a>Mevcut bir projeyi yayımlama

Mevcut bir proje varsa _değil_ zaten sürüm denetiminde Git'te ayarlamak için aşağıdaki adımları kullanın:

4.  Mac için Visual Studio'da Çözüm bölmesi çözüm adı seçin 

5. Menü çubuğunda **sürüm denetimi > sürüm denetiminde Yayımla...** Görüntülenecek **depo seçin** iletişim:

    ![Mac için Visual Studio'da kullanıma almayı başlatma](media/version-control-git4-sml.png)

    Bu menü öğesi menüde gri renkte görünür, çözüm adı seçtiğinizden emin olun.  

6. Seçin **kayıtlı depoları** sekmesi ve ENTER tuşuna **Ekle** düğmesi:

    ![](media/version-control-git5.png)

7. Yerel olarak görüntülemek ve #3. adımdaki URL'yi yapıştırın istediğiniz deponun adını girin. Depo yapılandırması iletişim aşağıdakine benzer görünmelidir. Tamam'a basın: 

    ![Git Ayrıntıları iletişim girin](media/version-control-git6.png)

    Git'e bağlanmak için SSH kullanmak da mümkündür unutmayın.

8. Uygulama için Git yayımlamayı denerse için depoyu seçin ve emin her ikisi de **modül adı** ve **ileti** metin alanları tamamlanır:

    ![Proje için git yayımlamayı denerse](media/version-control-git7.png)

9. Tıklayın **Tamam**, ardından **Yayımla** uyarı iletişim.

10. Git kimlik bilgilerinizi Visual Studio'da Mac tercihleri için girdiğiniz değil, şimdi girin. İlk olarak, bir erişim bir parola yerine kullanılan belirteç, oluşturmanız gerekir. Bir erişim belirteci oluşturmadıysanız, Git adımları [erişim belirteci](https://help.github.com/articles/creating-an-access-token-for-command-line-use/) belgeleri.

11. Kullanıcı adı ve kişisel erişim belirteci, girin ve basın **Tamam**:

    ![Git için kullanıcı adı ve parola girin](media/version-control-git9-sml.png)

12. Birkaç saniye sonra çözümü ile ilk alt işleme yayımlanması gerekir. Pek çok seçenek ile doldurulmuş artık sürüm denetimi menü öğesi göz atarak yayımlandı onaylayın: 

    ![Sürüm denetimi menüsü](media/version-control-git10.png)

13. Ek değişiklikler yapmak başlattıktan sonra seçin **değişiklikleri Gönder...**  değişiklikleri göndermek için **uzak** depo. Bu, üzerinde github.com görüntülemek uygun tüm kullanıcılara izin verir: 

    ![Değişiklikleri uzak depoya gönderin](media/version-control-git11.png)

## <a name="publishing-a-new-project"></a>Yeni bir proje yayımlama

Yeni Proje iletişim kutusu, git kullanarak yeni bir proje yayımlamak için kullanılabilir. Bunu etkinleştirmek için işaretleyin **sürüm denetimi için Git'i kullanabilirsiniz.** Aşağıdaki ekran görüntüsünde gösterildiği gibi onay kutusu. Deponuzu başlatmak ve isteğe bağlı bir .gitignore dosyası ekleyin:

![Değişiklikleri uzak depoya gönderin](media/version-control-git12.png)

## <a name="checkout-an-existing-repository"></a>Varolan bir depo kullanıma alma

Yerel makinenizde olmayan uzak yalnızca var olan bir GitHub deposu ile çalışmak zorunda kalırsınız neredeyse kesindir. Mac için Visual Studio, kullanıma alma için bu deponun hızlı bir şekilde sağlar. Makinenize kopyalamak için aşağıdaki adımları izleyin:

1. Menü çubuğunda **sürüm denetimi > kullanıma alma...** :

2. Bu görüntüler **depo Bağlan** sekmesinde:

    ![Girilen ayrıntılarla depo sekmesinde bağlanma](media/version-control-git13.png)

3. Uzak deponun GitHub sayfasında basın **Kopyala veya indir** düğmesi ve sağlanan URL'yi kopyalayın:

    ![Görüntülenen github URL'si](media/version-control-git14.png)

4. Tüm metni değiştirin **URL** giriş alanına **depo Bağlan** sekmesi. Bu en diğer alanları bu sekme, #2. adımdaki resimde gösterildiği gibi doldurur.

5. Depoyu kopyalamak ve basın istediğiniz dizini girin **kullanıma alma**.

> [!NOTE]
> Depo 4 GB boyutunda ise sorunlarla karşılaşabilirsiniz.

## <a name="troubleshooting"></a>Sorun giderme

Boş bir uzak depo projenizle başlatma sorunları varsa, aşağıdaki adımları deneyebilirsiniz:

- Çözüm klasörünüze gidin.
- Tuşuna `Command + Shift + . ` gizli dosya ve klasörleri gösterilecek.
- Varsa bir **.git** klasörünü silin.
- Varsa bir **da gitignore** dosya, silin.
- Tuşuna `Command + Shift + . ` dosyaları ve klasörleri gizlemek için.
- Mac için VS çözümünüzü açın
- Çözüm panelinde, çözüm düğümü seçin.
- Sürüm denetimi menüsüne göz atıp seçin **sürüm denetiminde Yayımla**.
- Adım 6 ' itibaren yukarıdaki öğreticideki adımları izleyin.