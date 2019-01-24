---
title: 'Nasıl yapılır: ClickOnce uygulaması için güncelleştirmeleri yönetme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
f1_keywords:
- Microsoft.VisualStudio.Publish.ClickOnceProvider.Dialog.Update
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, managing applications
- ClickOnce deployment, updates
- updating data, ClickOnce
- application updates
ms.assetid: a3f23f05-e7f1-4620-b23c-2d68f9643684
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 9781745af5d65d497652002c9afcd8132058ffb6
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54790686"
---
# <a name="how-to-manage-updates-for-a-clickonce-application"></a>Nasıl yapılır: ClickOnce Uygulaması için Güncelleştirmeleri Yönetme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] Uygulama güncelleştirmeleri otomatik olarak veya programlama yoluyla denetleyebilirsiniz. Bir geliştirici olarak ne zaman ve nasıl güncelleme kontrolleri gerçekleştirilir, güncelleştirmeleri zorunlu olan ve burada uygulama güncelleştirmeleri denetlemeli belirtme esneklik kullanabileceğiniz birçok seçenek mevcuttur.  
  
 Uygulama güncelleştirmeleri otomatik olarak uygulama başlamadan önce ya da belirlenen aralıklarda uygulama başladıktan sonra denetlemek için yapılandırabilirsiniz. Buna ek olarak, gerekli en düşük sürüm belirtebilirsiniz; diğer bir deyişle, kullanıcının sürüm gereken sürümden düşükse bir güncelleştirmenin yüklü olduğu.  
  
 Program aracılığıyla bir kullanıcı isteği gibi bir olay tabanlı güncelleştirmeleri denetlemek için uygulamanın yapılandırabilirsiniz. "Güncelleştirmeleri programlı olarak denetlemek için" yordamında bu konuda kullanan kodu nasıl yazacağınızı gösterir <xref:System.Deployment.Application.ApplicationDeployment> güncelleştirmeleri denetlemek için sınıf tabanlı bir olayı.  
  
 Ayrıca, uygulamanızı bir konumdan dağıtabilir ve başka bir yerden güncelleştirebilirsiniz. "Farklı bir güncelleştirme konumu belirtin." yordamına bakın.  
  
 Daha fazla bilgi için [ClickOnce güncelleştirme stratejisini seçme](../deployment/choosing-a-clickonce-update-strategy.md).  
  
 Güncelleştirme davranışını yönetilir **uygulama güncelleştirmeleri** iletişim kutusu, kullanılabilir **Yayımla** sayfasının **Proje Tasarımcısı.**  
  
### <a name="to-check-for-updates-before-the-application-starts"></a>Uygulama başlamadan önce güncelleştirmeleri denetlemek için  
  
1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2.  Tıklayın **Yayımla** sekmesi.  
  
3.  Tıklayın **güncelleştirmeleri** açmak için düğmeyi **uygulama güncelleştirmeleri** iletişim kutusu.  
  
4.  İçinde **uygulama güncelleştirmeleri** iletişim kutusunda, emin olun **uygulama güncelleştirmeleri denetlesin** onay kutusu seçilidir.  
  
5.  İçinde **uygulamanın güncelleştirmeleri denetleyeceği zamanı seçin** bölümünden **Uygulama başlatılmadan önce**. Bu, kullanıcıların ağa her zaman bağlı uygulama yapılan son güncelleştirmelerle birlikte çalışmasını sağlar.  
  
### <a name="to-check-for-updates-in-the-background-after-the-application-starts"></a>Uygulama başlatıldıktan sonra arka planda güncelleştirmeleri denetlemek için  
  
1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2.  Tıklayın **Yayımla** sekmesi.  
  
3.  Tıklayın **güncelleştirmeleri** açmak için düğmeyi **uygulama güncelleştirmeleri** iletişim kutusu.  
  
4.  İçinde **uygulama güncelleştirmeleri** iletişim kutusunda, emin onay kutusunu **uygulama güncelleştirmeleri denetlesin** seçilir.  
  
5.  İçinde **uygulama için güncelleştirmeleri bölümüne denetleyeceği zamanı seçin**seçin **uygulama başladıktan sonra**. Uygulama, böylece daha hızlı başlatılır ve ardından, arka planda güncelleştirmeleri denetler ve bir güncelleştirme kullanılabilir olduğunda yalnızca kullanıcıya bildir. Uygulama yeniden başlatılana kadar yüklendikten sonra güncelleştirmeleri etkili olmaz.  
  
6.  İçinde **uygulamanın güncelleştirmeleri ne sıklıkla denetleyeceğini belirtin** bölümünde, ya da seçin **uygulama her çalıştırıldığında denetle** (varsayılan) veya **denetleyin her** ve bir sayı ve zaman aralığı girin.  
  
### <a name="to-specify-a-minimum-required-version-for-the-application"></a>Uygulama için gerekli en düşük sürüm olarak belirtmek için  
  
1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2.  Tıklayın **Yayımla** sekmesi.  
  
3.  Tıklayın **güncelleştirmeleri** açmak için düğmeyi **uygulama güncelleştirmeleri** iletişim kutusu.  
  
4.  İçinde **uygulama güncelleştirmeleri** iletişim kutusunda, emin olun **uygulama güncelleştirmeleri denetlesin** onay kutusu seçilidir.  
  
5.  Seçin **bu uygulama için gerekli en düşük sürüm belirtin** onay kutusunu işaretleyin ve ardından girin **ana**, **küçük**, **derleme**ve  **Düzeltme** uygulama için sayı.  
  
### <a name="to-specify-a-different-update-location"></a>Farklı güncelleştirme konumunu belirtmek için  
  
1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2.  Tıklayın **Yayımla** sekmesi.  
  
3.  Tıklayın **güncelleştirmeleri** açmak için düğmeyi **uygulama güncelleştirmeleri** iletişim kutusu.  
  
4.  İçinde **uygulama güncelleştirmeleri** iletişim kutusunda, emin olun **uygulama güncelleştirmeleri denetlesin** onay kutusu seçilidir.  
  
5.  İçinde **güncelleştirme konumu** biçimini kullanarak tam bir URL ile güncelleştirme konumu girin http://Hostname/ApplicationName, ya da UNC yolu biçiminde \\\Server\ApplicationName veya tıklatın **Gözat** güncelleştirme konumu için Gözat düğmesini.  
  
### <a name="to-check-for-updates-programmatically"></a>Güncelleştirmeleri programlı olarak denetlemek için  
  
1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2.  Tıklayın **Yayımla** sekmesi.  
  
3.  Tıklayın **güncelleştirmeleri** açmak için düğmeyi **uygulama güncelleştirmeleri** iletişim kutusu.  
  
4.  İçinde **uygulama güncelleştirmeleri** iletişim kutusunda, emin **uygulama güncelleştirmeleri denetlesin** onay kutusu işaretli değilse. (İsteğe bağlı olarak, güncelleştirmeleri programlama yoluyla ve aynı zamanda güncelleştirmeleri otomatik olarak denetle ClickOnce çalışma zamanı denetlemesine izin vermek için bu onay kutusunu seçebilirsiniz.)  
  
5.  İçinde **güncelleştirme konumu** biçimini kullanarak tam bir URL ile güncelleştirme konumu girin http://Hostname/ApplicationName, ya da UNC yolu biçiminde \\\Server\ApplicationName veya tıklatın **Gözat** güncelleştirme konumu için Gözat düğmesini. Uygulamanın güncelleştirilmiş bir sürümünü kendisi için nerede görüneceğini güncelleştirme konumdur.  
  
6.  Güncelleştirmeleri denetlemek için kullanıcıları seçip bir Windows formunda bir düğme, menü öğesi veya diğer kullanıcı arabirimi öğesi oluşturun. Bu öğenin olay işleyicisinden denetlemek ve güncelleştirmeleri yüklemek için bir yöntemini çağırın. Visual Basic ve Visual örneği bulabilirsiniz C# benzer bir yöntem için kod [nasıl yapılır: ClickOnce dağıtım API'sini kullanarak program aracılığıyla uygulama güncelleştirmelerini denetleme](../deployment/how-to-check-for-application-updates-programmatically-using-the-clickonce-deployment-api.md).  
  
7.  Uygulamanızı oluşturun.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Deployment.Application.ApplicationDeployment>   
 [Uygulama güncelleştirmeleri iletişim kutusu](http://msdn.microsoft.com/8eca8743-8e68-4d04-bfd5-4dc0a9b2934f)   
 [ClickOnce güncelleştirme stratejisini seçme](../deployment/choosing-a-clickonce-update-strategy.md)   
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)   
 [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)   
 [Nasıl yapılır: ClickOnce Dağıtım API'sini Kullanarak Program Aracılığıyla Uygulama Güncelleştirmelerini Denetleme](../deployment/how-to-check-for-application-updates-programmatically-using-the-clickonce-deployment-api.md)
