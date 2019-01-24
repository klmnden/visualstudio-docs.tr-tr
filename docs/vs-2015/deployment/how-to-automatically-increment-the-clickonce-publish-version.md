---
title: 'Nasıl yapılır: Artırma ClickOnce yayım sürümünü otomatik olarak | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
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
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 0d779e364f5cbe7bc4b90e0a77ab3fb825a7b6c2
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54788388"
---
# <a name="how-to-automatically-increment-the-clickonce-publish-version"></a>Nasıl yapılır: ClickOnce Yayım Sürümünü Otomatik Olarak Artırma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yayımlama sırasında bir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] uygulama, değiştirme `Publish Version` özelliği, bir güncelleştirme olarak yayımlanacak uygulama neden olur. Varsayılan olarak, Visual Studio otomatik olarak artırır `Revision` sayısı `Publish Version` her zaman uygulama yayımlayın.  
  
 Bu davranışı devre dışı bırakabilirsiniz **Yayımla** sayfasının **Proje Tasarımcısı**.  
  
> [!NOTE]
>  Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [Visual Studio'da geliştirme ayarlarını özelleştirme](http://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### <a name="to-disable-automatically-incrementing-the-publish-version"></a>Yayımla sürümünü otomatik olarak artırma devre dışı bırakmak için  
  
1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2.  Tıklayın **Yayımla** sekmesi.  
  
3.  İçinde **yayımlama sürümü** bölümünde, NET **her yayında düzeltmeyi otomatik artış** onay kutusu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Kümesi ClickOnce yayım sürümü](../deployment/how-to-set-the-clickonce-publish-version.md)   
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)   
 [Nasıl yapılır: Yayımlama Sihirbazını Kullanarak ClickOnce Uygulaması Yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)
