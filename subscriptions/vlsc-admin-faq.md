---
title: VLSC yönetici geçişi hakkında SSS | Microsoft Docs
author: evanwindom
ms.author: jaunger
manager: evelynp
ms.date: 03/13/2018
ms.topic: conceptual
description: Toplu Lisanslama hizmet Merkezi'nden yönetici geçişi hakkında SSS
ms.openlocfilehash: 34c5d2d287507699ebc47bdd7e4716838c408d07
ms.sourcegitcommit: 208395bc122f8d3dae3f5e5960c42981cc368310
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/10/2019
ms.locfileid: "67784745"
---
# <a name="visual-studio-subscriptions-administration-migration"></a>Visual Studio abonelikleri yönetim geçişi

Önümüzdeki birkaç ay içinde Visual Studio abonelikleri (önceki adıyla MSDN Abonelikleri) yönetimi için değişiklikler yapılacaktır. Bugün, Visual Studio aboneliklerini Toplu Lisanslama yoluyla ve abonelikler Toplu Lisans Hizmet Merkezi (VLSC) portalında yönetilir satın alabilirsiniz. Yeni bir Yönetim Portalı oluşturulur ve bu yeni portalda Visual Studio abonelikleri gelecekte yönetilmez. VLSC tarafından sağlanan mevcut işlemlere ek olarak, izleme ve abonelikleri ve Azure erişimi yönetmek için Active Directory'yi (Azure AD) kullanma olanağı filtreleme sınırsız toplu atama yeni portalı izin verir. Yeni Visual Studio Yönetim Portalı şu adreste yer alacaktır: [ https://manage.visualstudio.com ](https://manage.visualstudio.com).

> [!Note]
> Bu geçiş, MPSA müşterilerine etkilemez.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="why-is-it-changing"></a>Neden değişiyor?
Yeni portal, Visual Studio abonelikleri Yönetimi deneyimini iyileştirmek ve nasıl satın alınan bağımsız olarak Visual Studio Abonelikleri, yönetme, tek bir deneyim oluşturun. Yeni portal, Azure AD tarafından doğrulanmasını sağlar ve bize geleceği konumlandırır yeni bir platformu vardır. Ayrıca, bu gidin ve kullanmak, daha kolay bir güncelleştirilmiş kullanıcı arabirimi bulunacaktır yönetici verimliliği artacaktır.

### <a name="who-will-be-impacted"></a>Kimler etkilenecek?
Değişiklik, etkin Toplu Lisanslama sözleşmeleri olan ve Toplu Lisanslama aracılığıyla Visual Studio abonelikleri satın almış olan tüm müşterileri etkileyecek.

### <a name="when-is-it-changing"></a>Ne zaman değişiyor?
Bu büyük bir geçiş ve Visual Studio abonelikleri için etkin Toplu Lisanslama sözleşmeleri olan tüm müşterileri üzerinden yeni yönetim portalına geçirilene kadar aşamalardaki tamamlandı. Geçiş sırasında 2017'in ilk çeyreği başladı. Toplu Lisanslama müşterilerimizin zamanlanan geçiş haftasından önce bilgilendireceğiz.

### <a name="does-my-organization-need-to-sign-up-for-azure-active-directory-azure-ad"></a>Kuruluşumun Azure Active Directory (Azure AD) açmanız gerekiyor mu?
Kuruluşunuz için Azure AD'ye Kaydol gerekmez, ancak herhangi bir zamanda bunu yapabilirsiniz. Azure AD eklenmeyi tercih ederseniz, hiçbir ücret ödemeden ücretsiz katmanı için Azure AD'yi kullanarak bunu yapabilirsiniz. Azure Active Directory ile kuruluşunuz Artırılmış güvenlik, Denetim ve uzun süreli güvenilirlik koruyacağınızı. Azure AD için hazır değilseniz bugün olduğu gibi Microsoft Accounts (MSA) kullanmaya devam etmek mümkün olacaktır.

### <a name="how-do-i-know-when-my-organization-will-be-migrated"></a>Kuruluşumun ne zaman geçirilir mi olduğunu nasıl öğrenebilirim?
Birincil/bildirim ilgili kişileri kuruluşunuz geçirilmeden önce bir hafta ekleme işlemini tamamlamaya davet eden bizden e-posta alırsınız. Abonelik yöneticileri de biz birincil/bildirimler ilgili kişileri iletişim kurulacak ve ayrıntılar hakkında başarılı olmasına yardımcı olmak sağlanan olduğunu bildiren bir e-posta alırsınız. Bilgi edinmek için nasıl [kuruluşunuzun birincil/bildirim ilgili kişileri bulun](#how-do-i-find-out-who-my-primary-or-notices-contact-is).

### <a name="is-onboarding-different-from-migration"></a>Onboarding geçişten farklı mıdır?
Evet.  Bu işlemde iki aşama vardır. Ayarlama (veya ekleme), kuruluşunuzun geçiş öncesinde, bir yönetici olarak işinizde kesinti olmasını sağlar. Biz, kuruluşunuzun bilgileri geçirildikten sonra yeni portalda Visual Studio Aboneliklerini yönetmek mümkün olacaktır. Birincil/bildirimler ilgili kişileri geçirilmeden önce yerleşik Aksi takdirde, abonelik yöneticileri engellenir ve ekleme işlemi tamamlanana kadar abonelikleri yönetmek mümkün olmayacaktır.

### <a name="what-is-the-onboarding-process"></a>Onboarding işlemi nedir?
E-posta, ekleme işlemini tamamlamak için birincil ve bildirimler ilgili kişileri davet eden gönderilir.
İşlemi hakkında yönergeler için aşağıya bakın.
1. **PCN'nizi edinme ve oturum açma:**

    a. E-postada birincil ve bildirimler ilgili kişileri benzersiz bir bağlantı ve bunların genel müşteri numarasını (PCN), son üç basamak ile sağlanır. *

    b. Tüm PCN almak için birincil ilgili kişi VLSC için oturum açmanız gerekir (PCN bulmak için yönergeler için aşağıda).

    c. PCN aldıktan sonra kullanıcıdan oturum açmasını ister kendi benzersiz bağlantı seçmeniz gerekir. Bunlar, kuruluşunuz Azure AD üzerinde değilse, bir iş/Okul hesabı (Kuruluşunuz Azure AD'de ise) ya da bir Microsoft hesabı (MSA) kullanarak oturum açmanız mümkün olacaktır.

    d. Ardından, bunlar PCN'yi girmeniz istenir.

2. **Yöneticilerinize ayarlayın:**

    PCN girdikten sonra bunlar sayfasına Süper Yöneticiler ve yöneticiler (daha önce abonelik yöneticileri olarak da bilinir) ekleyebilir nerede alınır. İdeal olarak bu aboneliklerinizin yönetiminde herhangi kesintiyle karşılaşmamanız kuruluşunuzun geçiş tarihinden önce tamamlanmalıdır.

3. **Yeni abonelik yönetimi portalına erişme:** Kuruluşunuz geçirildikten sonra yeni portala erişmek ve abonelikleri yönetmeye başlamak için yöneticileri ve Süper Yöneticiler e-postalar gönderilir.

> [!NOTE]
> Birincil veya bildirimler ilgili kişileri birden fazla e-posta almanız durumunda, bu, birden çok PCN'ye sahip oldukları anlamına gelir. Her e-postasında PCN için benzersiz bağlantıyı kullanarak işlemi tamamlamak gerekir.

### <a name="what-is-the-difference-between-a-super-admin-and-an-administrator"></a>Süper yönetici ile yönetici arasındaki fark nedir?
Birincil/bildirimler ilgili ilk kez oturum açtığında, bunlar otomatik olarak bir süper Yöneticisi olarak ayarlanır Süper Yöneticiler ekleme/başka Süper Yöneticiler veya Yöneticiler silerek abonelikleri yönetici erişimi yönetebilir ve abonelikleri de yönetebilirsiniz. Süper yönetici, diğer Süper yöneticilerin kendilerini ek olarak atamak seçebilirsiniz.

(Daha önce abonelik yöneticileri olarak da bilinir) yöneticileri yalnızca abonelikleri yönetebilir, ancak Aboneliklerini Yönetme erişimi olanların denetleyemezsiniz.

### <a name="how-will-i-as-an-administrator-onboard-to-the-new-portal"></a>Nasıl olacak ı, bir yönetici olarak yeni portala ekleme?
Kuruluşunuzun birincil ilgili kişiler ve bildirimler ilgili kişileri bunları ya da iş kullanarak oturum açın ya da Okul hesapları, Azure Active Directory (Azure AD) veya kişisel MSA tarafından desteklenen sağlayacak bir sayfasına yönlendirilirsiniz benzersiz bir bağlantı içeren bir e-posta alırsınız. Oturum açtıktan sonra kuruluşunuzun genel müşteri numarasını (PCN) veya yetkilendirme numaranızı sözleşmeyi doğrulamak için girmeniz gerekir. Bunlar ardından, gibi başka Yöneticiler eklemek için bir süper yönetici olarak Visual Studio Aboneliklerini yönetmek için ayarlanır.

### <a name="where-do-i-manage-subscriptions-if-my-organization-has-been-onboarded-but-hasnt-been-migrated"></a>Kuruluşum eklendi, ancak geçirilen taşınmadığından abonelikleri nereden yönetebilirim?
Kuruluşunuz geçirildikten sonra artık ve yeni portalda yönetilmeye hazırdır Visual Studio abonelikleri e-posta almak kadar abonelikleri VLSC'de aracılığıyla yönetmeye devam eder.

### <a name="where-can-i-locate-my-organizations-public-customer-number-pcn-or-authorization-number"></a>Kuruluşumun genel müşteri numarasını (PCN) veya yetkilendirme numarasını nereden bulabilirim?
Oturum [VLSC](https://www.microsoft.com/Licensing/servicecenter/default.aspx) ve aşağıdaki yola gidin: **Abonelikleri** > **Visual Studio abonelikleri**. PCN aşağıda bulunan **sözleşmesi/genel müşteri numarası sonuçları**. Bu PCN'nizi edinme konusunda adım adım yönergeler almak [Yardım makalesi](find-pcn.md).

### <a name="how-do-i-find-out-who-my-primary-or-notices-contact-is"></a>Birincil veya bildirimler ilgili kim olduğunu nasıl bulabilirim?
Oturum [VLSC](https://www.microsoft.com/Licensing/servicecenter/default.aspx) ve aşağıdaki yola gidin: **Lisanslar > ilişki özeti** seçin, **lisans kimliği > kişiler**. Birincil veya bildirimler ilgili Kişim bu bulma, adım adım rehberlik alın [Yardım makalesi](find-primary-contact.md).

### <a name="what-if-my-primary-or-notices-contact-is-gone-no-longer-with-the-company-or-not-available-to-complete-onboarding"></a>Ne birincil veya bildirimler ilgili Kişim, artık şirketten veya tam ekleme kullanılamaz gitti?
Şunları yapmanız gerekir [desteğe](https://visualstudio.microsoft.com/subscriptions/support/#talktous) ve VLSC'de abonelikleri yönetmek için kullanılan e-posta sağlayın. Yapıldıktan sonra destek ekleme işlemi konusunda size yardımcı olmak üzere mümkün olacaktır.

### <a name="what-will-happen-with-renewing-customers"></a>Müşteriler yenileme ile ne?
Müşterileri yenilemek için yenileme aboneliklerini zamanki devam edebilmeli, yenileme işlemleri geçişten etkilenmez.

### <a name="should-my-organization-wait-to-set-up-a-new-agreement-in-the-new-system-rather-than-renew-an-existing-agreement"></a>Kuruluşum mevcut bir sözleşmeyi yenilemek yerine yeni sistemde yeni bir anlaşma ayarlamak için beklemeli midir?
Hayır.  Geçiş oluşturma veya yenileme sözleşmelerinin etkilemez.

### <a name="what-if-my-organizations-agreement-is-in-the-grace-period-during-the-transition-will-they-also-be-migrated"></a>Ne kuruluşumun sözleşmesi yetkisiz kullanım süresi içinde geçiş sırasında mı? Bunlar da geçirilir mi?
Evet, kuruluşunuz sözleşme hala etkinse geçirilir.

### <a name="what-if-my-organization-has-over-claimed-in-the-current-system-will-we-still-be-migrated-to-the-new-system"></a>Ne Kuruluşum geçerli sistemde üzerinde istenen? Biz yine de yeni sisteme geçirilir mi?
Evet, kuruluşunuz yine de yeni sisteme geçirilir. (Bunun sözleşmesi türleri için) talep aşımı olanağı yeni sistemde de sunulacaktır.

### <a name="what-if-my-organization-has-more-than-one-subscription-assigned-to-a-single-useremail-address"></a>Ne Kuruluşum için bir tek kullanıcı/e-posta adresi atanmış birden fazla aboneliğiniz var?
Kuruluşunuz yine de geçirilecektir.  Ancak, aynı düzeye ek tüm abonelikleri atamak mümkün olmayacaktır (IE: Enterprise, Professional, vs.) Bu kullanıcı/e-posta adresi. Geçiş yapıldıktan sonra aynı e-posta adresine sahip aynı düzeydeki tüm abonelikleri görünmeye devam edecektir, ancak yöneticiler e-posta adreslerini bunlar benzersiz olacak şekilde değiştirmeniz gerekir. Birden çok abonelik aynı düzeydeki bir tek kullanıcı/e-posta adresi yeni portalda atamak mümkün olmayacaktır.

### <a name="where-can-i-find-the-most-up-to-date-information-about-the-migration"></a>Geçiş hakkında en güncel bilgileri nerede bulabilirim?
Bu geçiş ile ilgili tarih bilgisi kadar çoğu için ziyaret edin, Visual Studio abonelikleri Yöneticisi [Web sayfası](https://aka.ms/vs-admin). Desteğe ihtiyacınız varsa, Visual Studio abonelikleri denetleyin [destek sayfasını](http://visualstudio.microsoft.com/subscriptions/support/#!collections/962-subscriptions), kendi kendine yardım içeren bilgi ve Destek iletişim bilgileri. Önümüzdeki birkaç ay içinde size yönetici Web sayfamızı ve bu geçişin kolaylıkla ortaya yardımcı olmak için e-posta aracılığıyla güncelleştirmeleri sağlamaya devam edecek.

## <a name="resources-and-support-information"></a>Kaynaklar ve destek bilgileri
- [Yönetici Web sayfamızı](https://visualstudio.microsoft.com/subscriptions-administration/)

- Visual Studio abonelikleri ve Yönetim [desteği](https://visualstudio.microsoft.com/subscriptions/support/)

- [My PCN bulma](find-pcn.md)

- [Birincil veya bildirimler ilgili Kişim bulma](find-primary-contact.md)

- [Video](https://www.youtube.com/watch?v=ZmnywYGSFMg&list=PLReL099Y5nRfDyvvwzNDBaZe7qTxmuM2T&index=1&t=0s) yetiştirme yöneten yöneticiler ve kuruluş
