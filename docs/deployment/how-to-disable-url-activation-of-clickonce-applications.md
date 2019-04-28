---
title: 'Nasıl yapılır: ClickOnce uygulamalarında URL etkinleştirmeyi devre dışı bırakma | Microsoft Docs'
ms.date: 11/04/2016
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
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6841b8a91cec24f467f6e3f684cbb27e25c9fa63
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62899355"
---
# <a name="how-to-disable-url-activation-of-clickonce-applications"></a>Nasıl yapılır: ClickOnce uygulamalarında URL etkinleştirmeyi devre dışı bırak

Genellikle, bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama bir Web sunucusundan yükledikten hemen sonra otomatik olarak başlatılır. Güvenlik nedeniyle, bu davranışı devre dışı bırakmak ve kullanıcıların uygulamayı başlatacağı karar verebilir **Başlat** menü yerine. Aşağıdaki yordam, URL etkinleştirmeyi devre dışı bırakmak açıklar.

Bu teknik yalnızca kullanılabilir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] kullanıcının bilgisayarında bir Web sunucusundan yüklenen uygulamalar. Yalnızca kendi URL'yi kullanarak başlatılabilir, yalnızca çevrimiçi uygulamalar için kullanılamaz. Yalnızca çevrimiçi ve yüklü uygulamaları arasındaki fark hakkında daha fazla bilgi için bkz. [ClickOnce dağıtım stratejisini seçme](../deployment/choosing-a-clickonce-deployment-strategy.md).

Bu yordam, Windows Yazılım Geliştirme Seti (SDK) aracı MageUI.exe kullanır. Bu araç hakkında daha fazla bilgi için bkz. [MageUI.exe (bildirim üretme ve düzenleme aracı, grafik istemci)](/dotnet/framework/tools/mageui-exe-manifest-generation-and-editing-tool-graphical-client). Ayrıca, bu yordamı Visual Studio kullanarak da gerçekleştirebilirsiniz.

## <a name="procedure"></a>Yordam

### <a name="to-disable-url-activation-for-your-application"></a>Uygulamanız için URL etkinleştirmeyi devre dışı bırakmak için

1. Dağıtım bildiriminin MageUI.exe açın. Henüz bir oluşturmadıysanız, adımları [izlenecek yol: Bir ClickOnce uygulamasını el ile dağıtmak](../deployment/walkthrough-manually-deploying-a-clickonce-application.md).

2. Seçin **dağıtım seçenekleri** sekmesi.

3. NET **otomatik olarak yükledikten sonra uygulamayı çalıştırmak** onay kutusu.

4. Kaydet ve bildirim oturum açın.

## <a name="see-also"></a>Ayrıca bkz.

- [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)