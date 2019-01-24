---
title: ClickOnce dağıtım stratejisini seçme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, strategies
- deploying applications, ClickOnce
ms.assetid: 98bcab65-ab8b-4ed1-9adc-fdacf92b8106
caps.latest.revision: 21
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 619d70b79d75cc45add0d541cd081d9ac0f258d5
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54774042"
---
# <a name="choosing-a-clickonce-deployment-strategy"></a>ClickOnce Dağıtım Stratejisini Seçme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Dağıtmak için üç farklı strateji vardır bir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] öncelikle dağıtmakta olduğunuz uygulama türüne bağlıdır seçtiğiniz strateji; uygulama. Üç dağıtım stratejisi aşağıdaki gibidir:  
  
-   Web'den veya bir Ağ Paylaşımı'ndan yükle  
  
-   CD'den yükle  
  
-   Uygulamayı Web'den veya Ağ Paylaşımı'ndan başlat  
  
    > [!NOTE]
    >  Dağıtım stratejisi seçmenin yanı sıra, uygulama güncelleştirmeleri sağlamak için de bir strateji seçmek isteyeceksiniz. Daha fazla bilgi için [ClickOnce güncelleştirme stratejisini seçme](../deployment/choosing-a-clickonce-update-strategy.md).  
  
## <a name="install-from-the-web-or-a-network-share"></a>Web'den veya bir Ağ Paylaşımı'ndan yükle  
 Bu stratejiyi kullandığınızda, uygulamanız bir Web sunucusuna veya ağ dosyası paylaşımına dağıtılır. Son kullanıcı uygulamayı yüklemek istediğinde, Web sayfası üzerinde bir simgeye tıklar veya dosya paylaşımındaki simgeye çift tıklar. Sonra son kullanıcının bilgisayarında uygulama indirilir, kurulur ve başlatılır. Öğeleri eklenir **Başlat** menü ve **Program Ekle veya Kaldır** içinde **Denetim Masası**.  
  
 Bu strateji ağ bağlantısına bağlı olduğundan, yerel ağ veya yüksek hızlı Internet bağlantısı erişimi olan kullanıcılar çok iyi çalışır.  
  
 Uygulamayı Web'den dağıtırsanız, URL kullanımı etkinleştirildiğinde bağımsız değişkenleri uygulamaya geçirebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Bir çevrimiçi bir ClickOnce uygulamasında sorgu dize bilgilerini alma](../deployment/how-to-retrieve-query-string-information-in-an-online-clickonce-application.md). Bu belgede açıklanan diğer yöntemleri kullanarak etkinleştirilen bir uygulamaya bağımsız değişkenler geçirilemez.  
  
 İçinde bu dağıtım stratejisini etkinleştirmek için [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], tıklayın **Web'den** veya **UNC yolu veya dosya paylaşımı** üzerinde **nasıl yükleneceğini** Yayımla Sihirbazı'nın sayfa.  
  
 Bu, varsayılan dağıtım stratejisidir.  
  
## <a name="install-from-a-cd"></a>CD'den yükle  
 Bu stratejiyi kullandığınızda, uygulamanız CD-ROM veya DVD gibi çıkarılabilir ortamla dağıtılır. Kullanıcı uygulamayı yüklemeyi seçtiğinde, yüklü ve başlatılmış ve öğeleri eklenir önceki seçeneği ile **Başlat** menü ve **Program Ekle veya Kaldır** içinde **denetimi Paneli**.  
  
 Bu strateji en iyi, devamlı ağ bağlantısı olmayan veya bant genişliği düşük bağlantısı olan kullanıcılara dağıtılacak uygulamalar için çalışır. Uygulama çıkarılabilir ortamdan yüklendiğinden yükleme için ağ bağlantısı gerekmez, ancak ağ bağlantısını yine de uygulama güncelleştirmeleri için gereklidir.  
  
 İçinde bu dağıtım stratejisini etkinleştirmek için [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], tıklayın **CD-ROM veya DVD-ROM** üzerinde **nasıl yükleneceğini** Yayımla Sihirbazı'nın sayfa.  
  
 Bu dağıtım stratejisini el ile etkinleştirmek için değiştirin **deploymentProvider** dağıtım bildirimi içinde etiketi. (Visual Studio'da bu özellik olarak kullanıma sunulan **yükleme URL'si** üzerinde **Yayımla** sayfası Proje Tasarımcısı. İçinde Mage.exe **Başlat konumu**.)  
  
## <a name="start-the-application-from-the-web-or-a-network-share"></a>Uygulamayı Web'den veya Ağ Paylaşımı'ndan başlat  
 Uygulamanın bir Web uygulaması gibi davranması dışında, bu strateji birinci stratejiye benzer. Kullanıcı Web sayfası üzerinde bir bağlantıyı tıkladığında (veya dosya paylaşımında bir simgeye çift tıklarsa) uygulama başlatılır. Kullanıcı uygulamayı kapatırsa, artık yerel bilgisayarlarında kullanılamıyor; hiçbir şey eklenir **Başlat** menüsü veya **Program Ekle veya Kaldır** içinde **Denetim Masası**.  
  
> [!NOTE]
>  Teknik olarak uygulama, Web uygulamalarının Web önbelleğine indirilmesi gibi yerel bilgisayar üzerinde uygulama önbelleğine indirilir ve kurulur. Web önbelleği gibi, dosyalar son olarak uygulama önbelleğinden atılır. Ancak, kullanıcı uygulamanın Web'den veya dosya paylaşımından çalıştığını zanneder.  
  
 Bu strateji en iyi seyrek kullanılan uygulamalar için çalışır. Örneğin, genellikle her yıl yalnızca bir kez çalıştırılan bir çalışan-yarar aracı.  
  
 İçinde bu dağıtım stratejisini etkinleştirmek için [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], tıklayın **uygulama yüklemeyen** üzerinde **yükleme veya Web'den çalıştırın** Yayımla Sihirbazı'nın sayfa.  
  
 Bu dağıtım stratejisini el ile etkinleştirmek için değiştirin **yükleme** dağıtım bildirimi içinde etiketi. (Bunun değeri olabilir **true** veya **false**. Mage.exe içinde kullanım **yalnızca çevrimiçi** seçeneğini **uygulama türü** listesi.)  
  
## <a name="web-browser-support"></a>Web Tarayıcısı Desteği  
 .NET Framework 3.5 kullanan uygulamalar herhangi bir tarayıcı kullanarak yüklenebilir.  
  
 .NET Framework 2.0 kullanan uygulamalar Internet Explorer gerektirir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce güvenliği ve dağıtımı](../deployment/clickonce-security-and-deployment.md)   
 [ClickOnce güncelleştirme stratejisini seçme](../deployment/choosing-a-clickonce-update-strategy.md)   
 [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)   
 [ClickOnce Uygulamalarının Güvenliğini Sağlama](../deployment/securing-clickonce-applications.md)
