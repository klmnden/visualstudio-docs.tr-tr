---
title: Diğer adlar kullanılırken Visual Studio aboneliklerinde oturum açma başarısız olabilir | Microsoft Docs
author: evanwindom
ms.author: lank
manager: lank
ms.date: 07/19/2019
ms.topic: conceptual
description: Diğer adlar veya kolay adlar kullanılıyorsa oturum açma başarısız olabilir
ms.openlocfilehash: 392b86699b1116f45ca75df3b611fff6a2aebc62
ms.sourcegitcommit: 485881e6ba872c7b28a7b17ceaede845e5bea4fe
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/22/2019
ms.locfileid: "68378028"
---
# <a name="signing-in-to-visual-studio-subscriptions-may-fail-when-using-aliases"></a>Diğer adlar kullanılırken Visual Studio aboneliklerinde oturum açma başarısız olabilir
Oturum açmak için kullanılan hesap türüne bağlı olarak, kullanılabilir abonelikler ' de [https://my.visualstudio.com](https://my.visualstudio.com?wt.mc_id=o~msft~docs)oturum açarken doğru görüntülenmeyebilir. Olası bir neden, aboneliğin atandığı oturum açma kimliği yerine "diğer adlar" veya "kolay adlar" in kullanılması olabilir. Bu "diğer ad" olarak adlandırılır.

## <a name="what-is-aliasing"></a>Diğer ad nedir?
"Diğer ad" terimi, Windows 'da (veya Active Directory) oturum açmak ve e-postaya erişmek için farklı kimliklere sahip kullanıcılar anlamına gelir.

Şirket, 'JohnD@contoso.com' gibi dizin oturum açma işlemi için Microsoft Online hizmetine sahip olsa da diğer adlara ve kullanıcılara 'John.Doe@contoso.com' gibi diğer adlar veya kolay adlar kullanarak e-posta hesaplarına erişebilirler. Toplu Lisanslama hizmeti Merkezi (VLSC) aracılığıyla aboneliklerini yöneten birçok müşteri için, bu, girilenJohn.Doe@contoso.come-posta adresi (' ') dizin adresiyle ('JohnD@contoso.com') eşleşmediğinden başarısız oturum açma deneyimine yol açabilir. ) "Iş veya okul hesabı" seçeneği aracılığıyla başarılı kimlik doğrulaması için gereklidir.

## <a name="as-an-administrator-what-options-do-i-have"></a>Yönetici olarak hangi seçeneklere sahip mıyım?
Yönetici olarak, abonelerinizin üzerinde [https://my.visualstudio.com](https://my.visualstudio.com?wt.mc_id=o~msft~docs)başarılı bir oturum açma deneyimine sahip olmasını sağlamak için iki seçenek vardır.
- İlk seçenek (önerilir), Toplu Lisanslama hizmeti Merkezi 'ndeki (VLSC) atanan adres olarak dizin hesabından faydalanır. Daha fazla bilgi için bu makalenin [bir dizin hesabına abone atama](#assigning-subscribers-to-a-directory-account) bölümüne bakın.
- İkinci seçenek (daha az güvenli), abonelerin "Iş veya okul" e-posta adresini bir "kişisel" Hesapla (deyişle Microsoft hesabı veya MSA). Daha fazla bilgi için bu makaledeki [bir iş veya okul hesabını kişisel hesap olarak tanımlama](#defining-a-work-or-school-account-as-a-personal-account) bölümüne bakın.

> [!NOTE]
> Şirketiniz yeni Visual Studio abonelikleri [Yönetim portalına](https://manage.visualstudio.com)geçirildikten sonra, her iki dizin ve e-posta adresinin abonenin bir parçası olarak sağlanmasını sağlayan yeni yönetim deneyiminden yararlanabilirsiniz. profilinizi. [Geçiş](https://support.microsoft.com/help/4013930/visual-studio-subscriptions-administrator-migration-details)hakkında daha fazla bilgi edinin.

## <a name="assigning-subscribers-to-a-directory-account"></a>Bir dizin hesabına aboneler atama
Her durumda, Toplu Lisanslama hizmeti Merkezi 'ndeki (VLSC) abonelik yöneticisinin yeni aboneler için Dizin adresini kullanması veya "mevcut" aboneler için e-posta adresini güncelleştirmesi gerekir. Dizin adresinin kullanılması, yeni abonelerin bir hoş geldiniz e-postası almayacağını ve yöneticinin aboneye bir abonelik atandığını bilgilendirmesini gerektiren anlamına geldiğini unutmayın. Aşağıdaki adımları uyguladıktan sonra, abonelere bildirimde bulunan e-posta [şablonunu](#notifying-your-subscribers-with-directory-addresses) kullanmayı ve oturum açma sürecinde yardımcı olmaya de göz ayırın.

### <a name="adding-new-subscribers"></a>Yeni aboneler ekleme
Bir dizin hesabı ile yeni bir abone eklemek için lütfen bu adımları izleyin.

1. [Toplu Lisanslama hizmeti Merkezi 'ni](https://www.microsoft.com/Licensing/servicecenter/default.aspx) (VLSC) ziyaret edin ve oturum açın.
2. VLSC admin sayfasından **abonelikler** ' e ve ardından **Visual Studio abonelikleri**' ne tıklayın.

    > [!div class="mx-imgBorder"]
    > ![Abonelikler menüsü](_img//vlsc/vlsc-subscriptions.png)

3. Visual Studio aboneliğiyle ilişkili **sözleşme numarasına** tıklayın.

    > [!div class="mx-imgBorder"]
    > ![Anlaşma seçin](_img/vlsc/vlsc-agreement.png)

4. **Abonelik ata**' ya tıklayın.
5. İstenen **abonelik düzeyini**seçin.
6. Atanacak abonelikleriniz olduğunu doğrulayın ve **İleri**' ye tıklayın.
7. Abone ayrıntılarını ve Dizin adresini e-posta adresi alanına girip **İleri**' ye tıklayın.
8. Abone bilgilerini doğrulayın ve **son**' a tıklayın.
9. Aşağıdaki [şablonu](#notifying-your-subscribers-with-directory-addresses)kullanarak abonesine aboneliğin sağlandığını bildirin.

### <a name="updating-an-existing-subscriber"></a>Mevcut bir aboneyi güncelleştirme
Mevcut bir aboneyi bir dizin hesabıyla güncelleştirmek için lütfen aşağıdaki adımları izleyin.

1. [Toplu Lisanslama hizmeti Merkezi 'ni](https://www.microsoft.com/Licensing/servicecenter/default.aspx) (VLSC) ziyaret edin ve oturum açın.
2. VLSC yönetici sayfalarından **abonelikler** ' e ve ardından **Visual Studio abonelikleri**' ne tıklayın.
3. Visual Studio aboneliğiyle ilişkili **sözleşme numarasına** tıklayın.
4. Arama çubuğundaki **aşağı oka** tıklayın.
5. "E-posta adresi" alanını kullanarak aboneyi arayın.
6. Sonuçlar listesinden abonenin **son adına** tıklayın.
7.           **Düzenle**‘ye tıklayın.
8. E-posta adresi alanını istenen dizin adresiyle değiştirin ve **Kaydet**' e tıklayın.
9. Aşağıdaki e-posta şablonu kullanılarak abonelere aboneliğin sağlandığını bildirin.

### <a name="notifying-your-subscribers-with-directory-addresses"></a>Dizin adresleriyle abonelere bildirme
Hoş geldiniz e-postası aboneinizde başarılı bir şekilde ulaşmayacak, lütfen aşağıdaki iletiyi kopyalayıp bir e-postaya yapıştırın ve abonelere gönderin. % WORD% değerini her abone için uygun bilgilerle değiştirin.

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

## <a name="defining-a-work-or-school-account-as-a-personal-account"></a>Bir iş veya okul hesabını kişisel hesap olarak tanımlama
Yeni bir kullanıcı eklemek veya Toplu Lisanslama hizmeti Merkezi (VLSC) içindeki bir kullanıcının e-posta adresini güncelleştirmek için, [bir dizin hesabına abone atama](#assigning-subscribers-to-a-directory-account) bölümünde açıklanan yönergelerden yararlanın.  E-posta adresinin dizin tarafından tanınmaması durumunda, kullanıcının e-posta adresini kişisel hesap olarak tanımlamak için yeni bir hesap oluşturma işlemini adım adım yapması gerekir.  Kısa dönem için, Visual Studio abonelikleri ekibi aşağıda tanımlanan kimlik ilkesinden bir istisnayı güvenli hale getirdi, ancak bu ilkeyi kaldırmak için gereken yeteneklere yatırım yaptık.

> [!WARNING]
> Microsoft, "Iş veya okul" kimliklerinin "kişisel" kimliklerle birleştirilmesi önerilmez.  Bu eylem, kuruluşun hesabın sahipliğini ve denetimini kaybetmesine ve çalışanın şirketten ayrıldıktan sonra bile belirli ürün veya hizmetlere erişmesine devam edebilir.  

### <a name="defining-an-email-address-as-a-personal-account"></a>Kişisel hesap olarak bir e-posta adresi tanımlama
Aboneliğe bir abonelik atandıktan sonra, abonelik avantajlarından faydalanmak için ziyaret [https://my.visualstudio.com](https://my.visualstudio.com?wt.mc_id=o~msft~docs) etmesini isteyen bir e-posta gönderilir.  Oturum açmaya çalışırken, Visual Studio aboneliği oturum açma işlemi, hesabın tanınmadığını belirten bir hata vererek başarısız olur.  [https://my.visualstudio.com](https://my.visualstudio.com?wt.mc_id=o~msft~docs) Deneyime oturum açmadan önce, abonesinden bu yönergeleri izlemesini isteyin.  Gerekirse, bir aboneliği atadıktan sonra bu [şablonu](#notifying-your-subscribers-using-personal-accounts) kullanarak abone 'nize bildirim gönderebilirsiniz.

1. Öğesine https://my.visualstudio.com gidin ve **Yeni Microsoft hesabı oluştur**' a tıklayın.

2. Alanları doldurun:
   - Someone@example.com Kutuya hoş geldiniz e-postasını alan e-posta adresini girin
   - Parolanızı oluşturma
   - Promosyon ayarlarınızı seçin
   -           **İleri**'ye tıklayın.

3. Doğrulama adımlarını tamamlayıp **İleri**' ye tıklayın.

4. Yeni kullanıcıların Visual Studio profilini tamamlaması gerekebilir.

5. Abonelik ve avantajlar artık görünür olmalıdır.

### <a name="notifying-your-subscribers-using-personal-accounts"></a>Kişisel hesapları kullanarak abonelere bildirme
Yukarıda özetlenen senaryoda, aboneizin bir "hoş geldiniz e-postası" alır, ancak diğer ad nedeniyle bu kişiler oturum açamıyor olabilir.  Yukarıdaki adımları abonelere bildirmek için aşağıdaki metni kullanabilir ve gerekirse destek seçeneklerini önerebilirsiniz.  % WORD% değerini her abone için uygun bilgilerle değiştirin.

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
