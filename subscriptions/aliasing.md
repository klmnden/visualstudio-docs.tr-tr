---
title: Visual Studio abonelikleri için oturum açma başarısız olabilir diğer adlar kullanırken | Microsoft Docs
author: evanwindom
ms.author: jaunger
manager: evelynp
ms.date: 01/02/2018
ms.topic: conceptual
description: Diğer ad veya kolay adlar kullanılması durumunda oturum açma başarısız olabilir
searchscope: VS Subscription
ms.openlocfilehash: ac3f9df365e0b7924b615c2ae8cbb70d93d04948
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60041391"
---
# <a name="signing-in-to-visual-studio-subscriptions-may-fail-when-using-aliases"></a>Visual Studio abonelikleri için oturum açarken diğer adlar kullanırken başarısız olabilir

Oturum açmak için kullanılan hesap türüne bağlı olarak, mevcut abonelikler düzgün açarken görüntülenmeyebilir [ https://my.visualstudio.com ](https://my.visualstudio.com?wt.mc_id=o~msft~docs). Olası bir nedeni "diğer" veya "kolay adlar" abonelik atandığı oturum açma yerine kimliktir. Bu, "diğer ad kullanımı" olarak adlandırılır.

## <a name="what-is-aliasing"></a>Diğer ad kullanımı nedir?

"Diğer ad kullanımı" terimi farklı kimliklere sahip olmasını, kullanıcıların Windows (veya Active Directory'nizde) oturum açmak ve e-postaya erişmeye ifade eder.

Diğer ad kullanımı ile bir şirket Microsoft çevrimiçi hizmeti için kendi directory oturum açma gibi olduğunda karşılaşılabilir JohnD@contoso.com, ancak kullanıcılar diğer adları veya kolay adlar gibi kullanarak e-posta hesaplarına erişim John.Doe@contoso.com. Kendi aboneliklerini Toplu Lisanslama hizmeti Merkezi (VLSC) aracılığıyla yöneten birçok müşteri için bu bir başarısız oturum açma deneyimine e-posta adresi olarak sağlanan neden olabilir (John.Doe@contoso.com) ile dizin adresinin eşleşmiyor (JohnD@contoso.com) "İş veya Okul hesabı" seçeneği aracılığıyla başarılı kimlik doğrulaması için gereklidir.

## <a name="as-an-administrator-what-options-do-i-have"></a>Yönetici olarak, hangi seçenekleri zorundayım?

Yönetici olarak, abonelerinize sahip başarılı bir oturum açma deneyimi sağlamak için iki seçenek vardır [ https://my.visualstudio.com ](https://my.visualstudio.com?wt.mc_id=o~msft~docs).
- İlk seçenek (önerilir), Toplu Lisanslama hizmeti Merkezi (VLSC) olarak atanan adresi olarak dizin hesabı yararlanmasına gelir. Başvurmak [bir dizin hesabı atama abonelere](#assigning-subscribers-to-a-directory-account) daha fazla ayrıntı için bu makaledeki bir bölüm.
- (Daha az güvenlidir), ikinci seçenek olur (yani), "Kişisel" hesap "İş veya Okul" e-posta adresine ilişkilendirilecek abonelerinize izin vermek için Microsoft hesabı veya MSA). Başvurmak [kişisel bir hesap bir iş veya Okul hesabı tanımlama](#defining-a-work-or-school-account-as-a-personal-account) daha fazla ayrıntı için bu makaledeki bir bölüm.

> [!NOTE]
> Yeni Visual Studio abonelikleri için şirketinizin geçirildikten sonra [Yönetim Portalı](https://manage.visualstudio.com), bir parçası olarak sağlanacak hem dizin ve e-posta adreslerini sağlayan yeni bir yönetim deneyimi yararlanmak mümkün olacaktır abonenin profili. Daha fazla bilgi edinin [geçiş](https://support.microsoft.com/help/4013930/visual-studio-subscriptions-administrator-migration-details).

## <a name="as-a-subscriber-what-options-do-i-have"></a>Abone olarak, hangi seçenekleri zorundayım?

Abone açısından bakıldığında, ilk iş yöneticinize, şirketinizin kimlik yapılandırması anlamak için önemlidir. Gerekirse, Yönetici hesap ayarlarınızı, Yönetim Portalı'ndan güncelleştirmeniz gerekebilir veya şirket e-posta adresinizi kullanarak bir Microsoft hesabı (MSA) oluşturmanız gerekebilir. Bir MSA oluşturmak için adımları gerçekleştirmeden önce tüm ilkeleri veya bu eylemi gerçekleştirmeden sorunları ile ilgili yöneticinizle konuşun. Başvurmak [kişisel bir hesap bir iş veya Okul hesabı tanımlama](#defining-a-work-or-school-account-as-a-personal-account) daha fazla ayrıntı için bu makaledeki bir bölüm.

## <a name="assigning-subscribers-to-a-directory-account"></a>Bir dizin hesabına abonelerin atama

Tüm durumlarda, Toplu Lisanslama hizmeti Merkezi (VLSC) içinde Abonelik Yöneticisi ile dizin adresinin yeni aboneleri için kullanabilir veya "var" aboneler için e-posta adresini güncelleştirmek gerekir. Dizin adresinin kullanarak herhangi bir yeni aboneler Hoş Geldiniz e-posta almaz ve yönetici bildirmek için bir abonelik atanmış abone gerekecek anlamına gelir olduğunu unutmayın. Sonra aşağıdaki adımları, lütfen ayrıca e-posta araştırmalarında [şablon](#notifying-your-subscribers-with-directory-addresses) abonelerinize bildirmek ve oturum açma işleminde size yardımcı olmak için.

### <a name="adding-new-subscribers"></a>Yeni aboneler ekleme

Lütfen bir dizin hesabıyla yeni aboneleri eklemek için bu adımları izleyin.

1. Ziyaret [Toplu Lisanslama Hizmet Merkezi](https://www.microsoft.com/Licensing/servicecenter/default.aspx) (VLSC) ve oturum açın.
2. VLSC yönetici sayfasından tıklatın **abonelikleri** ardından **Visual Studio abonelikleri**.

    > [!div class="mx-imgBorder"]
    > ![Abonelik menü](_img//vlsc/vlsc-subscriptions.png)

3. Tıklayın **anlaşma numarası** Visual Studio aboneliği ile ilişkili.

    > [!div class="mx-imgBorder"]
    > ![Sözleşme seçin](_img/vlsc/vlsc-agreement.png)

4. Tıklayın **atama, aboneliğini**.
5. İstenen seçin **abonelik düzeyi**.
6. Doğrulama abonelikleri atamak ve kullanılabilir olan **sonraki**.
7. Abone ayrıntıları ve dizin adresinin e-posta adres alanına girin ve tıklayın **sonraki**.
8. Abone bilgisi doğrulamak ve tıklayın **son**.
9. Abone, aboneliğini kullanarak sağlandığını bildir aşağıda [şablon](#notifying-your-subscribers-with-directory-addresses).

### <a name="updating-an-existing-subscriber"></a>Mevcut bir abone güncelleştiriliyor

Lütfen mevcut bir abone directory hesabıyla güncelleştirmek için aşağıdaki adımları.

1. Ziyaret [Toplu Lisanslama Hizmet Merkezi](https://www.microsoft.com/Licensing/servicecenter/default.aspx) (VLSC) ve oturum açın.
2. VLSC Yöneticisi sayfalarından tıklayın **abonelikleri** ardından **Visual Studio abonelikleri**.
3. Tıklayın **anlaşma numarası** Visual Studio aboneliği ile ilişkili.
4. Tıklayın **aşağı ok** arama çubuğundaki.
5. "E-posta adresi" alanını kullanarak aboneyi arayın.
6. Sonuç listesinden tıklayın **Soyadı** abonenin.
7. **Düzenle**‘ye tıklayın.
8. İstenen dizine adresine e-posta adresi alanından değiştirin ve **Kaydet**.
9. Abone, aboneliğini kullanarak sağlandığını bildirim e-posta şablonu aşağıda.

### <a name="notifying-your-subscribers-with-directory-addresses"></a>Abonelerinize directory adresleriyle bildirme

Hoş Geldiniz e-posta başarıyla abonenizi ulaşarak olduğundan, Lütfen kopyalama ve yapıştırma aşağıda iletiye bir e-posta ve abonenizi Gönder. Word'ün % her abone için uygun bilgi ile değiştirin.

```
----------- Copy Below (Ctrl+C) -----------

Hello %SUBSCRIBER NAME%

You have been assigned a Visual Studio subscription. Please visit https://my.visualstudio.com, and log in with your %DIRECTORY ADDRESS% address to activate and access your subscription.

If you’re having trouble, please contact the support team (https://visualstudio.microsoft.com/subscriptions/support/).

At the bottom of the page, select the following:
   - Accounts, Subscriptions, and Billing Support
   - From Issue, choose Subscription sign in support
   - Choose the appropriate Country
   - Select the desired Assisted Support option

----------- End Copy -----------
```

## <a name="defining-a-work-or-school-account-as-a-personal-account"></a>Bir iş veya Okul hesabı kişisel bir hesap tanımlama

Lütfen bölümünde açıklanan yönergeleri yararlanarak [bir dizin hesabı atama abonelere](#assigning-subscribers-to-a-directory-account) yeni bir kullanıcı eklemek veya bir kullanıcının e-posta adresi Toplu Lisanslama hizmeti Merkezi (VLSC) içinde güncelleştirmek için bölüm.  Burada e-posta adresi directory tarafından tanınmıyor durumlarda, kullanıcının e-posta adresi bir kişisel hesap tanımlamak için yeni bir hesap oluşturma işlemi adım adım gerekir.  Kısa vadede için Visual Studio abonelikleri ekibi, aşağıda tanımlanan Kimlik İlkesi bir muafiyet güvenli var. ancak Biz bu ilkeyi kaldırmak gerekli özellikleri yatırım yapıyor.

> [!WARNING]
> Microsoft, "İş veya Okul" kimlik "Kişisel" kimliklerle birleştirme önermez.  Bu eylem kuruluş sahipliği ve denetimi hesabının kaybetmenize neden olur ve çalışan şirket ayrıldıktan sonra belirli bir ürün veya hizmetler erişmeye devam edebilirsiniz.  Lütfen bu başvuru [blog gönderisi](https://blogs.technet.microsoft.com/enterprisemobility/2016/09/15/cleaning-up-the-azure-ad-and-microsoft-account-overlap/), ek bilgi için Microsoft Identity ekibinin.

### <a name="defining-an-email-address-as-a-personal-account"></a>Kişisel bir hesap bir e-posta adresi tanımlama

Aboneye abonelik atandıktan sonra bunları ziyaret etmek isteyen bir e-posta alırsınız [ https://my.visualstudio.com ](https://my.visualstudio.com?wt.mc_id=o~msft~docs) , abonelik avantajlarının yararlanmak için.  Çalışırken oturum açma, Visual Studio aboneliği oturum açma bir hesap tanınmıyor belirten hata ile başarısız olur.  Önce oturum içinde [ https://my.visualstudio.com ](https://my.visualstudio.com?wt.mc_id=o~msft~docs) deneyimi, aşağıdaki yönergeleri izleyin, abonenin isteyin.  Gerekirse, bunu kullanıp kullanamayacağını [şablon](#notifying-your-subscribers-using-personal-accounts) abonelik atandıktan sonra abone bildirir.

1. Gidin https://my.visualstudio.com, tıklatıp **yeni bir Microsoft hesabı oluşturun**.

2. Alanları doldurun:
   - Hoş Geldiniz e-postada alınan e-posta adresi girin Someone@example.com kutusu
   - Parola oluşturma
   - Promosyon ayarlarınızı seçin
   - **İleri**'ye tıklayın.

3. Doğrulama adımları tamamlayın ve tıklayın **sonraki**.

4. Yeni kullanıcılar, Visual Studio profili gerçekleştirmeniz gerekebilir.

5. Abonelik ve avantajları artık görünür olmalıdır.

### <a name="notifying-your-subscribers-using-personal-accounts"></a>Abonelerinize kişisel hesapları bildirme

Yukarıda özetlenen senaryo, abonenin "Hoş Geldiniz e" alırsınız, ancak diğer ad kullanımı nedeniyle oturum açamıyor oldukları oldukları fark edebilirsiniz.  Kullanabileceğiniz aşağıdaki abonenizi yukarıdaki adımların bildirim ve destek seçenekleri gerekirse önermek için metni.  Word'ün % her abone için uygun bilgi ile değiştirin.

```
----------- Copy Below (Ctrl+C) -----------

Hello %SUBSCRIBER NAME%

You have been assigned a Visual Studio subscription, and may have been directed to log into https://my.visualstudio.com based on your Welcome email.  While this is the correct website for consuming benefits, our organization requires you to take a few extra steps before you can access the site.  Please follow the below instructions to help you create a “Microsoft Account” that is tied to our corporate email address.  Once these steps are completed, you will use your email address to access the Subscription benefits.
1. Visit https://my.visualstudio.com

2. Click Create new Microsoft Account on the right hand side

3. Complete the Form:
   - Use your corporate email address in the someone@example.com box
   - Enter a password
   - Select your promotional preference
   - Click Next

4. Complete the account validation steps

5. If necessary, complete the Visual Studio profile

6. You should now see your benefits

Note:  When visiting https://my.visualstudio.com in the future, you may be prompted to select which account you’d like to use (e.g. “Work or School Account” or “Personal Account”).  After following the steps above, you will need to leverage the “Personal Account” option.

If you’re having trouble, please contact the support team (https://visualstudio.microsoft.com/subscriptions/support/).

At the bottom of the page, select the following:
   - Accounts, Subscriptions, and Billing Support
   - From Issue, choose Subscription sign in support
   - Choose the appropriate Country
   - Select the desired Assisted Support option

----------- End Copy -----------
```
