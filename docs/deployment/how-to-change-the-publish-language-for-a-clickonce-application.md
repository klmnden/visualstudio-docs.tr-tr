---
title: Yayımlama dili ClickOnce uygulaması için değiştirme
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- Publish language property
- ClickOnce deployment, changing publish language
- publishing, ClickOnce
ms.assetid: ef5024c4-cda1-4970-bc75-32a2a10c92c3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e80a65b65d75d925decdf60b633a7d51ea9bafce
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66263171"
---
# <a name="how-to-change-the-publish-language-for-a-clickonce-application"></a>Nasıl yapılır: ClickOnce uygulaması için yayımlama dilini değiştirme

Yayımlama sırasında bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama, dil ve geliştirme bilgisayarınıza kültürünü Yükleme varsayılanlarını sırasında görüntülenen kullanıcı arabirimi. Yerelleştirilmiş bir uygulama yayımlıyorsanız, bir dil ve kültür yerelleştirilmiş sürümüyle eşleşecek şekilde belirtmeniz gerekir. Bu belirlenir `Publish language` projeniz için özellik.

`Publish language` Özellik ayarlanabilir **yayımlama seçeneği** iletişim kutusu, erişilebilir **Yayımla** sayfasının **Proje Tasarımcısı**.

> [!NOTE]
> Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [ayarlarına](../ide/environment-settings.md#reset-settings).

## <a name="to-change-the-publish-language"></a>Yayımlama dili değiştirmek için

1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.

2. Tıklayın **Yayımla** sekmesi.

3. Tıklayın **seçenekleri** açmak için düğmeyi **yayımlama seçeneği** iletişim kutusu.

4. Tıklayın **açıklama**.

5. İçinde **yayımlama seçeneği** iletişim kutusunda, bir dil seçin ve gelen kültür **yayımlama dilini** aşağı açılan liste ve ardından **Tamam**.

## <a name="see-also"></a>Ayrıca bkz.

- [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)
- [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)