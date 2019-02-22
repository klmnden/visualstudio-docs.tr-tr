---
title: 'Nasıl yapılır: Son kullanıcıların yükleme yapacakları konumu belirtme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- deploying applications [ClickOnce], specifying an installation URL
- URLs, specifying an installation URL
- installation, specifying installation an URL
- Installation URL property
ms.assetid: 04a804bf-ed55-4a7a-a1e6-f63ed99c0276
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2470c6ff8603bc100ee515b046efcf2436cb0b4e
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56629137"
---
# <a name="how-to-specify-the-location-where-end-users-will-install-from"></a>Nasıl yapılır: Burada son kullanıcıların yükleme yapacakları konumu belirtme
Yayımlama sırasında bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama, kullanıcıların gittikleri uygulamasını indirme ve yükleme için konum değildir nerede başlangıçta yayımladığınız uygulamanın konumu. Örneğin, bazı kuruluşlarda bir geliştirici bir uygulama için bir hazırlık sunucusu yayınlayabilir ve uygulamayı bir Web sunucusuna yönetici ardından taşıyabilir.

 Bu durumda, kullanabileceğiniz `Installation URL` kullanıcıları nereye uygulamayı indirmek için Web sunucusunu belirtmek için özellik. Bu, uygulama bildirimini güncelleştirmeleri aranacağı bilebilmesi gereklidir.

 `Installation URL` Özelliği, üzerinde ayarlanabilir **Yayımla** sayfasının **Proje Tasarımcısı**.

 **Not** `Installation URL` özelliği de ayarlanabilir kullanarak **PublishWizard**. Daha fazla bilgi için [nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md).

### <a name="to-specify-an-installation-url"></a>Bir yükleme URL'si belirtmek için

1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.

2.  Tıklayın **Yayımla** sekmesi.

3.  Yükleme URL'si biçimi kullanarak tam bir URL kullanarak yükleme konumu alanına *http://www.microsoft.com/ApplicationName*, ya da UNC yolu biçiminde  *\\\Server\ApplicationName*.

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Visual Studio'nun dosyaları nereye kopyalayacağını belirtme](../deployment/how-to-specify-where-visual-studio-copies-the-files.md)
- [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)
- [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)