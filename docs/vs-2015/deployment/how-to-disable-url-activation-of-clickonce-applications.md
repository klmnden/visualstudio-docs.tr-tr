---
title: 'Nasıl yapılır: ClickOnce uygulamalarında URL etkinleştirmeyi devre dışı bırakma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- disallowUrlActivation
- URL activation, ClickOnce applications
- ClickOnce deployment, URL activation
ms.assetid: db31a16b-960f-4264-91d7-c7c40f876068
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 75a98706858323693ec01ec3c3420a6d2d25ffef
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65697220"
---
# <a name="how-to-disable-url-activation-of-clickonce-applications"></a>Nasıl yapılır: ClickOnce Uygulamalarında URL Etkinleştirmeyi Devre Dışı Bırakma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Genellikle, bir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] uygulama bir Web sunucusundan yükledikten hemen sonra otomatik olarak başlatılır. Güvenlik nedeniyle, bu davranışı devre dışı bırakmak ve kullanıcıların uygulamayı başlatacağı karar verebilir **Başlat** menü yerine. Aşağıdaki yordam, URL etkinleştirmeyi devre dışı bırakmak açıklar.  
  
 Bu teknik yalnızca kullanılabilir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] kullanıcının bilgisayarında bir Web sunucusundan yüklenen uygulamalar. Yalnızca kendi URL'yi kullanarak başlatılabilir, yalnızca çevrimiçi uygulamalar için kullanılamaz. Yalnızca çevrimiçi ve yüklü uygulamaları arasındaki fark hakkında daha fazla bilgi için bkz. [ClickOnce dağıtım stratejisini seçme](../deployment/choosing-a-clickonce-deployment-strategy.md).  
  
 Bu yordamı kullanır [!INCLUDE[winsdklong](../includes/winsdklong-md.md)] MageUI.exe aracı. Bu araç hakkında daha fazla bilgi için bkz. [MageUI.exe (bildirim üretme ve düzenleme aracı, grafik istemci)](https://msdn.microsoft.com/library/f9e130a6-8117-49c4-839c-c988f641dc14). Bu yordamı kullanarak da gerçekleştirebilirsiniz [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
## <a name="procedure"></a>Yordam  
  
#### <a name="to-disable-url-activation-for-your-application"></a>Uygulamanız için URL etkinleştirmeyi devre dışı bırakmak için  
  
1. Dağıtım bildiriminin MageUI.exe açın. Henüz bir oluşturmadıysanız, adımları [izlenecek yol: Bir ClickOnce uygulamasını el ile dağıtma](../deployment/walkthrough-manually-deploying-a-clickonce-application.md).  
  
2. Seçin **dağıtım seçenekleri** sekmesi.  
  
3. NET **otomatik olarak yükledikten sonra uygulamayı çalıştırmak** onay kutusu.  
  
4. Kaydet ve bildirim oturum açın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce Uygulamalarını Yayımlama](../deployment/publishing-clickonce-applications.md)
