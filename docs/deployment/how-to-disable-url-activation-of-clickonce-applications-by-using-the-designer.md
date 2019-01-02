---
title: 'Nasıl Yapılır: Tasarımcıyı kullanarak ClickOnce uygulamalarında URL etkinleştirmeyi devre dışı bırakma | Microsoft Docs'
ms.date: 11/04/2016
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
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 1f1fddb68737ca316fa3fc580f050cf4bfa04fba
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53891459"
---
# <a name="how-to-disable-url-activation-of-clickonce-applications-by-using-the-designer"></a>Nasıl Yapılır: Tasarımcıyı kullanarak ClickOnce uygulamalarında URL etkinleştirmeyi devre dışı bırak
Genellikle, bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama bir Web sunucusundan yükledikten hemen sonra otomatik olarak başlayacak. Güvenlik nedeniyle, bu davranışı devre dışı bırakmak ve uygulamayı başlatmak için kullanıcılar karar verebilir **Başlat** menü yerine. Aşağıdaki yordam, URL etkinleştirmeyi devre dışı bırakmak açıklar.  
  
 Bu teknik yalnızca kullanılabilir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] kullanıcının bilgisayarında bir Web sunucusundan yüklenen uygulamalar. Yalnızca kendi URL'yi kullanarak başlatılabilir, yalnızca çevrimiçi uygulamalar için kullanılamaz. Yalnızca çevrimiçi ve yüklü uygulamaları arasındaki fark hakkında daha fazla bilgi için bkz: [ClickOnce dağıtım stratejisini seçme](../deployment/choosing-a-clickonce-deployment-strategy.md).  
  
 Bu yordamı kullanır [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Bu görevi kullanarak da gerçekleştirebilirsiniz [!INCLUDE[winsdklong](../deployment/includes/winsdklong_md.md)]. Daha fazla bilgi için [nasıl yapılır: ClickOnce uygulamalarında URL etkinleştirmeyi devre dışı](../deployment/how-to-disable-url-activation-of-clickonce-applications.md).  
  
## <a name="procedure"></a>Yordam  
  
#### <a name="to-disable-url-activation-for-your-application"></a>Uygulamanız için URL etkinleştirmeyi devre dışı bırakmak için  
  
1.  İçinde proje adınıza sağ **Çözüm Gezgini**, tıklatıp **özellikleri**.  
  
2.  Üzerinde **özellikleri** sayfasında **Yayımla** sekmesi.  
  
3.  Tıklayın **seçenekleri**.  
  
4.  Tıklayın **bildirimlerini**.  
  
5.  Etiketli onay kutusunu seçin **engelleyecek bir URL ile etkinleştirilmekte olan uygulamanın**.  
  
6.  Uygulamanızı dağıtın.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)