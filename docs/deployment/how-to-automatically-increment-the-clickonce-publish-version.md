---
title: 'Nasıl yapılır: Artırma ClickOnce yayım sürümünü otomatik olarak | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- deploying applications [ClickOnce], incrementing publish version automatically
- Publish Version property, incrementing
- ClickOnce deployment, incrementing publish version automatically
- publishing, ClickOnce
ms.assetid: 686ab88a-6305-4914-a05b-fe269cc0ae1e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cce9dfe48e34d642b115c8391de73c0350ce515b
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60081846"
---
# <a name="how-to-automatically-increment-the-clickonce-publish-version"></a>Nasıl yapılır: Otomatik olarak artırma ClickOnce yayım sürümü

Yayımlama sırasında bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama, değiştirme `Publish Version` özelliği, bir güncelleştirme olarak yayımlanacak uygulama neden olur. Varsayılan olarak, Visual Studio otomatik olarak artırır `Revision` sayısı `Publish Version` her zaman uygulama yayımlayın.

Bu davranışı devre dışı bırakabilirsiniz **Yayımla** sayfasının **Proje Tasarımcısı**.

> [!NOTE]
> Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [ayarlarına](../ide/environment-settings.md#reset-settings).

## <a name="to-disable-automatically-incrementing-the-publish-version"></a>Yayınlama sürümünü otomatik olarak artırma devre dışı bırakmak için

1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.

2. Tıklayın **Yayımla** sekmesi.

3. İçinde **yayımlama sürümü** bölümünde, NET **her yayında düzeltmeyi otomatik artış** onay kutusu.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Kümesi ClickOnce yayım sürümü](../deployment/how-to-set-the-clickonce-publish-version.md)
- [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)
- [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)