---
title: SharePoint nesne modellerini çağırma | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, client object model
- SharePoint development in Visual Studio, server object model
- SharePoint commands [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, extensibility features
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: df55347ea08bfcb243f37aaee111066106da49ff
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53914533"
---
# <a name="call-into-the-sharepoint-object-models"></a>SharePoint nesne modellerini çağırma
  Visual Studio'da SharePoint araçları için uzantıları oluşturduğunuzda, bazı görevleri gerçekleştirmek için SharePoint API'leri çağırmak zorunda kalabilirsiniz. Örneğin, SharePoint projeleri için bir özel dağıtım adımı oluşturmak, SharePoint çözümlerini dağıtmak için görevlerden bazılarını gerçekleştirmek için API'leri çağırmak olabilir.  
  
 [!INCLUDE[wss_14_long](../sharepoint/includes/wss-14-long-md.md)] ve [!INCLUDE[moss_14_long](../sharepoint/includes/moss-14-long-md.md)] SharePoint araçları uzantıları için kullanabileceğiniz iki farklı nesne modeli sağlar: sunucu nesne modeli ve bir istemci nesne modeli. Her nesne modeli, SharePoint araç uzantıları bağlamında avantajları ve dezavantajları vardır.  
  
 SharePoint nesne modellerini genel bakış için bkz. [SharePoint programlama modeline genel bakış araçları uzantıları](../sharepoint/overview-of-the-programming-model-of-sharepoint-tools-extensions.md).  
  
## <a name="use-the-client-object-model-in-extension-projects"></a>Uzantısı projelerinde istemci nesne modelini kullanma
 SharePoint araçları için bir uzantı geliştirdiğinizde, projenizdeki herhangi bir yönetilen API'ler kümesi gibi istemci nesne modelini kullanabilirsiniz. İstemci nesne modelini derlemelere başvuruları projenize ekleyebilirsiniz ve doğrudan kodunuzdan istemci nesne modelini API'leri çağırabilirsiniz.  
  
 Ancak, istemci nesne modelini SharePoint araç uzantıları bağlamında iki engelleri vardır:  
  
- İstemci nesne modelini yalnızca bir kısmı sunucu nesne modeli sağlar. İstemci nesne modelinde gösterilmeyen SharePoint işlevselliği kullanmak varsa, sunucu nesne modeli kullanmanız gerekir.  
  
- SharePoint araçları uzantıları için istemci nesne modelini kullanarak, çoğu durumda çalışması gerekir, ancak burada çağrılar için istemci nesne modelini beklendiği gibi çalışmıyor bazı senaryolar karşılaşabilirsiniz. İstemci nesne modelini istemci uygulamalarında SharePoint sitelerine bir uzak sunucuda veya grubunda çağırmak için kullanılmak üzere tasarlanmıştır. Visual Studio'da SharePoint araçları yalnızca yerel bir SharePoint yükleme geliştirme bilgisayarında çalışır. Bu nedenle, bir SharePoint araçları uzantısı'nda istemci nesne modelini kullandığınızda, bir SharePoint sitesine nasıl istemci nesne modelini kullanılmak üzere tasarlanmamıştır olduğu yerel bilgisayarda çağırın.  
  
  Visual Studio'da SharePoint araçları uzantısı istemci nesne modelini kullanma izlenecek yol için bkz: [izlenecek yol: Sunucu Gezgini uzantısında SharePoint istemcisi nesne modelini çağırma](../sharepoint/walkthrough-calling-into-the-sharepoint-client-object-model-in-a-server-explorer-extension.md).  
  
## <a name="use-the-server-object-model-in-extension-projects"></a>Sunucu nesne modeli uzantısı projelerinde kullanma
 Sunucu nesne modeli istemci nesne modelini bir üst kümesidir. Sunucu nesne modeli kullandığınız zaman, tüm özelliklerini kullanabilir, [!INCLUDE[wss_14_long](../sharepoint/includes/wss-14-long-md.md)] ve [!INCLUDE[moss_14_long](../sharepoint/includes/moss-14-long-md.md)] programlı olarak kullanıma sunar.  

 SharePoint araç uzantıları sunucusu nesne modelinde API'leri kullanabilirsiniz, ancak API'leri doğrudan çağrılamaz. Sunucu nesne modeli hedefleyen .NET Framework 3.5 yalnızca 64 bit işlemden çağrılabilir. SharePoint araç uzantıları ancak gerekli [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] ve bunlar 32-bit Visual Studio işleminde çalıştırın. Bu, SharePoint araç uzantıları SharePoint sunucusu nesne modelinde derlemeleri doğrudan başvuruda engeller.  
  
 Sunucu nesne modeli SharePoint Araçlar uzantısından kullanmak istiyorsanız, özel bir oluşturmalısınız *SharePoint komutu* API'sini çağırmak için. Sunucu nesne modeline doğrudan çağırabilir miyim ikincil bir derlemede SharePoint komutunun tanımlarsınız. Uzantı projenizde SharePoint komutunun dolaylı olarak ExecuteCommand yöntemini kullanarak çağırırsınız bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointConnection> nesne.  
  
 Oluşturma ve SharePoint komutlarını kullanma hakkında daha fazla bilgi için bkz. [nasıl yapılır: Bir SharePoint komutu oluşturma](../sharepoint/how-to-create-a-sharepoint-command.md) ve [nasıl yapılır: Bir SharePoint komutu yürütme](../sharepoint/how-to-execute-a-sharepoint-command.md). SharePoint komutları dağıtma hakkında daha fazla bilgi için bkz: [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).  
  
 Oluşturma ve kullanma SharePoint komutlarını nasıl gösteren izlenecek yollar için bkz. [izlenecek yol: SharePoint projeleri için bir özel dağıtım adımı oluşturmak](../sharepoint/walkthrough-creating-a-custom-deployment-step-for-sharepoint-projects.md) ve [izlenecek yol: Sunucu Gezgini, web bölümlerini görüntülemek üzere genişletme](../sharepoint/walkthrough-extending-server-explorer-to-display-web-parts.md).  
  
### <a name="understand-how-sharepoint-commands-are-executed"></a>SharePoint komutlarını nasıl yürütülür anlama
 SharePoint komutları tanımlayan derlemeleri adlı bir 64-bit ana bilgisayar işlemi içinde yüklenen *vssphost4.exe*. SharePoint Araçlar uzantısından SharePoint komutu çağırdıktan sonra komutu tarafından yürütülür *vssphost4.exe* 32-bit Visual Studio işlemini yerine (*devenv.exe*). Kayıt defterinde değerleri ayarlayarak SharePoint komutlarını nasıl yürütülür bazı yönlerini denetleyebilirsiniz. Daha fazla bilgi için [uzantıları Visual Studio'da SharePoint araçları için hata ayıklama](../sharepoint/debugging-extensions-for-the-sharepoint-tools-in-visual-studio.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Nasıl yapılır: Bir SharePoint komutu oluşturma](../sharepoint/how-to-create-a-sharepoint-command.md)   
 [Nasıl yapılır: Bir SharePoint komutu yürütme](../sharepoint/how-to-execute-a-sharepoint-command.md)   
 [Araç uzantılarının programlama modeline SharePoint genel bakış](../sharepoint/overview-of-the-programming-model-of-sharepoint-tools-extensions.md)  
