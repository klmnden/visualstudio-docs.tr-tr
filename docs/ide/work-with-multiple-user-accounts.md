---
title: Birden çok kullanıcı hesabıyla çalışma
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-acquisition
ms.topic: conceptual
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 33f88444d7bbdc0b0fe85bfa5efbdbbd794fa3e4
ms.sourcegitcommit: bc43970c000f07c9cc2051f1264a9742943a9755
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/09/2018
ms.locfileid: "51349401"
---
# <a name="work-with-multiple-user-accounts"></a>Birden çok kullanıcı hesabıyla çalışma

Birden çok Microsoft hesabına ve/veya iş veya Okul hesapları varsa, böylece herhangi bir hesabı kaynakları için ayrı ayrı oturum açmanız gerek kalmadan erişebilir bunları tüm Visual Studio için ekleyebilirsiniz. Şu anda Azure, Application Insights, Team Foundation Server ve Office 365 Hizmetleri kolaylaştırılmış oturum açma deneyimini destekler. Zaman geçtikçe ek hizmetler kullanılabilir duruma gelebilir.

Başka bir makinede Visual Studio'ya oturum açarsanız bir makine üzerinde birden çok hesap ekledikten sonra bu hesapları kümesi sizinle birlikte dolaşır. Hesap adlarını Dolaşımda olsa da, kimlik bilgileri sağlamadığı, dikkat edin önemlidir. Bu nedenle, ilk kez yeni makineye kaynaklarını kullanma girişimi diğer hesaplar için kimlik bilgilerini girin istenir.

Bu izlenecek yol, Visual Studio için birden fazla hesap ekleme işlemi açıklanır ve bu hesaplardan erişilebilir kaynakları yansıtılır nasıl yerleştirir gibi **bağlı hizmet Ekle** iletişim kutusunda **Sunucu Gezgini** , ve **Takım Gezgini**.

## <a name="sign-in-to-visual-studio"></a>Visual Studio’da oturum açma

- Visual Studio'ya bir Microsoft hesabı veya kuruluş hesabı ile oturum açın. Kullanıcı adınızı, şuna benzer şekilde penceresinin üst köşesinde görünür görmeniz gerekir:

     ![Kullanıcı oturum Currentlly](../ide/media/vs2015_username.png)

### <a name="access-your-azure-account-in-server-explorer"></a>Sunucu Gezgini'nde Azure hesabınıza erişin

Tuşuna **Ctrl**+**Alt**+**S** açmak için **Sunucu Gezgini**. Seçin **Azure** simgesi ve ne zaman, genişleyen Visual Studio'ya oturum açmak için kullanılan kimliği ile ilişkili Azure hesabındaki kullanılabilir kaynakları görmelisiniz. (Kendi kaynaklarını görürsünüz, hariç) aşağıdaki gibi görünmelidir.

![Sunucu Gezgini gösteren Azure Araçları düğümün genişletilmiş](../ide/media/vs2015_serverexplorer.png)

İlk kez belirli bir cihazda Visual Studio kullandığınızda iletişim kutusu yalnızca IDE ile oturum açtığı kimliği altında kayıtlı abonelikleri gösterir. Herhangi diğer hesaplarınız doğrudan kaynaklara erişebilir **Sunucu Gezgini** sağ tıklayarak **Azure** düğüm ve seçme **yönetin ve filtre abonelikleri**ve hesaplarınızı hesap seçici denetimi ekleme. Ardından, isterseniz aşağı oka tıklayıp hesapları listesinden seçim başka bir hesap seçebilirsiniz. Bir hesap seçtikten sonra görüntülemek istediğiniz söz konusu hesap altında abonelikleri seçebilirsiniz **Sunucu Gezgini**.

![Azure abonelikleri iletişim yönetme](../ide/media/vs2015_manage_subs.png)

Bir sonraki açışınızda **Sunucu Gezgini**, kaynaklar için aboneliklerinizi görüntülenir.

### <a name="access-your-azure-account-via-add-connected-service-dialog"></a>Bağlı hizmet Ekle iletişim kutusu aracılığıyla Azure hesabınıza erişin

1. C# dilinde bir UWP uygulaması projesi oluşturun.

1. İçinde proje düğümünü seçin **Çözüm Gezgini** seçip **Ekle** > **bağlı hizmet**. **Bağlı hizmet Ekle** Sihirbazı görünür ve hizmetlerin listesi, Visual Studio oturum açma kimliğiyle ilişkili Azure hesabındaki gösterir Azure için ayrı ayrı oturum açmanız gerekmez unutmayın. Ancak, diğer hesapları için belirli bir bilgisayardan kullanıcıların kaynaklara erişmeye ilk kez oturum açmanız gerekir.

    > [!WARNING]
    > Bu ilk kez kullanıyorsanız, belirli bir bilgisayarda Visual Studio'da bir UWP uygulaması oluşturuyorsanız, cihazınızın geliştirme modu için ekranına giderek etkinleştirirsiniz istenir **ayarları** > **güncelleştirmeler ve güvenlik**  >  **Geliştiriciler için** bilgisayarınızda. Daha fazla bilgi için [Cihazınızı geliştirme için etkinleştirme](/windows/uwp/get-started/enable-your-device-for-development).

### <a name="access_azure"></a> Web projesinde erişimi Azure Active Directory

Azure AD, son kullanıcı çoklu oturum açma ASP.NET MVC web uygulamaları veya web API hizmetlerindeki AD kimlik doğrulaması için destek sağlar. Etki alanı kimlik doğrulaması, kullanıcı hesabı kimlik doğrulamasını farklıdır; Active Directory etki alanınıza erişimi olan kullanıcılar, mevcut Azure AD hesaplarına web uygulamalarınıza bağlanmak için kullanabilirsiniz. Office 365 uygulamaları, etki alanı kimlik doğrulaması olarak da kullanabilirsiniz. Bu uygulamada görmek için bir web uygulaması oluşturma (**dosya** > **yeni proje** > **C#** > **bulut**  >  **ASP.NET Web uygulaması**). İçinde **yeni ASP.NET projesi** iletişim kutusunda seçin **kimlik doğrulamayı Değiştir**. Kimlik doğrulaması Sihirbazı görünür ve uygulamanızda kullanılacak kimlik doğrulaması türünü seçmenize olanak tanır.

![ASP.NET kimlik doğrulaması iletişim kutusu değişimi](../ide/media/vs2015_change_authentication.png)

ASP.NET kimlik doğrulaması farklı türleri hakkında daha fazla bilgi için bkz. [oluşturma ASP.NET web projeleri Visual Studio 2013'te](http://www.asp.net/visual-studio/overview/2013/creating-web-projects-in-visual-studio#orgauth) (kimlik doğrulaması hakkında bilgi hala geçerli Visual Studio sürümleri için geçerlidir).

### <a name="access-your-team-foundation-server-tfs-organization"></a>Team Foundation Server (TFS) kuruluşunuz erişimi

Ana menüden **takım** > **Team Foundation Server'a Bağlan** ortaya çıkarmak için **Takım Gezgini** penceresi. Tıklayarak **projeleri seçin**ve ardından liste kutusu altında **Team Foundation Server'ı seçin**, TFS kuruluşunuz için URL görmeniz gerekir. URL seçtiğinizde, kimlik bilgilerinizi yeniden girmek zorunda kalmadan oturumunuz açılır.

## <a name="add-a-second-user-account-to-visual-studio"></a>Visual Studio için ikinci bir kullanıcı hesabı Ekle

Visual Studio'nun üst köşedeki kullanıcı adınızın yanındaki aşağı oka tıklayın. Ardından **hesap ayarları** menü öğesi. **Hesap Yöneticisi** iletişim kutusu açılır ve oturum açmada görüntüler. Seçin **Hesap Ekle** yeni bir Microsoft hesabı veya yeni bir iş veya Okul hesabınızı eklemek için iletişim kutusunun köşesindeki bağlantı.

![Visual Studio hesabı Seçici](../ide/media/vs2015_acct_picker.png)

Yeni hesap kimlik bilgilerini girmek için istemleri izleyin. Aşağıdaki çizimde gösterildiği **Hesap Yöneticisi** bir kullanıcı parolasını ekledikten sonra *Contoso.com* iş hesabı.

![Hesap Yöneticisi](../ide/media/vs2015_accountmanager.gif)

## <a name="revisit-the-add-connected-services-wizard-and-server-explorer"></a>Sunucu Gezgini ve bağlı hizmetler Ekleme Sihirbazı'nı yeniden ziyaret

Artık Git **Sunucu Gezgini** tekrar sağ tıklayın **Azure** düğüm ve **yönetin ve filtre abonelikleri**. Açılan geçerli hesap yanındaki oka tıklayarak yeni bir hesap seçin ve ardından görüntülemek istediğiniz abonelikleri **Sunucu Gezgini**. Belirtilen aboneliği ile ilişkili tüm hizmetlerini görmelisiniz. Şu anda Visual Studio IDE ikinci hesabı ile oturum olsa bile, bu hesabın hizmetlerine ve kaynaklarına oturum açtınız. Aynı true **proje** > **bağlı hizmet Ekle** ve **takım** > **Team Foundation ServerBağlan**.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio’da oturum açma](signing-in-to-visual-studio.md)
- [Oturum açmak için Visual Studio Mac için](/visualstudio/mac/signing-in)
