---
title: 'Nasıl yapılır: Tasarımcıyı kullanarak ClickOnce uygulamalarında URL etkinleştirmeyi devre dışı bırakma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- disallowURLActivation
- URL activation, ClickOnce applications
- ClickOnce deployment, URL activation
ms.assetid: a337a582-e67c-409a-b52e-607cd1a8fc57
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 27690ab275d0c7ef2a090fa8ef2e42887ae9daeb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68153808"
---
# <a name="how-to-disable-url-activation-of-clickonce-applications-by-using-the-designer"></a>Nasıl yapılır: Tasarımcıyı Kullanarak ClickOnce Uygulamalarında URL Etkinleştirmeyi Devre Dışı Bırakma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Genellikle, bir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] uygulama bir Web sunucusundan yükledikten hemen sonra otomatik olarak başlayacak. Güvenlik nedeniyle, bu davranışı devre dışı bırakmak ve uygulamayı başlatmak için kullanıcılar karar verebilir **Başlat** menü yerine. Aşağıdaki yordam, URL etkinleştirmeyi devre dışı bırakmak açıklar.  
  
 Bu teknik yalnızca kullanılabilir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] kullanıcının bilgisayarında bir Web sunucusundan yüklenen uygulamalar. Yalnızca kendi URL'yi kullanarak başlatılabilir, yalnızca çevrimiçi uygulamalar için kullanılamaz. Yalnızca çevrimiçi ve yüklü uygulamaları arasındaki fark hakkında daha fazla bilgi için bkz: [ClickOnce dağıtım stratejisini seçme](../deployment/choosing-a-clickonce-deployment-strategy.md).  
  
 Bu yordamı kullanır [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Bu görevi kullanarak da gerçekleştirebilirsiniz [!INCLUDE[winsdklong](../includes/winsdklong-md.md)]. Daha fazla bilgi için [nasıl yapılır: ClickOnce uygulamalarında URL etkinleştirmeyi devre dışı](../deployment/how-to-disable-url-activation-of-clickonce-applications.md).  
  
## <a name="procedure"></a>Yordam  
  
#### <a name="to-disable-url-activation-for-your-application"></a>Uygulamanız için URL etkinleştirmeyi devre dışı bırakmak için  
  
1. İçinde proje adınıza sağ **Çözüm Gezgini**, tıklatıp **özellikleri**.  
  
2. Üzerinde **özellikleri** sayfasında **Yayımla** sekmesi.  
  
3. Tıklayın **seçenekleri**.  
  
4. Tıklayın **bildirimlerini**.  
  
5. Etiketli onay kutusunu seçin **engelleyecek bir URL ile etkinleştirilmekte olan uygulamanın**.  
  
6. Uygulamanızı dağıtın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce Uygulamalarını Yayımlama](../deployment/publishing-clickonce-applications.md)
