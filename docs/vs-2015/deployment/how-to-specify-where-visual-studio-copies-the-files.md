---
title: 'Nasıl yapılır: Burada Visual Studio 2015 kopyaları dosyaları belirtin. | Microsoft Docs'
titleSuffix: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- publishing, specifying location
- Publish Location property
ms.assetid: 6c552700-dda3-49fe-af98-4717344fda07
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 6b9f44f3d4f1a9d1b110501d0178e0e2e8dc4e47
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54798562"
---
# <a name="how-to-specify-where-visual-studio-copies-the-files"></a>Nasıl yapılır: Visual Studio'nun Dosyaları Nereye Kopyalayacağını Belirtme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

ClickOnce kullanarak bir uygulamayı yayımladığınızda `Publish Location` özelliği burada bildirimini ve uygulama dosyalarını isimlerine konumunu belirtir. Bu, bir dosya yolu veya bir FTP sunucusuna bir yolu olabilir.

 Belirtebileceğiniz `Publish Location` özelliği **Yayımla** sayfasının **Proje Tasarımcısı**, veya Yayımlama Sihirbazı'nı kullanarak. Daha fazla bilgi için [nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md).

> [!NOTE]
>  ClickOnce kullanarak bir uygulamanın birden fazla sürüm yüklediğinizde, yükleme uygulamanın önceki sürümlerini belirttiğiniz yayımlama konum arşivinde adlı bir klasöre taşır. Yükleme dizini temizler önceki sürümünden önceki sürümleri bu şekilde korur arşivleme.

### <a name="to-specify-a-publishing-location"></a>Bir yayımlama konumu belirtmek için

1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.

2. Tıklayın **Yayımla** sekmesi.

3. İçinde **yayımlama konumu** aşağıdaki biçimlerden birini kullanarak Yayınlama konumu girin:

   - Bir dosya paylaşımını veya disk yolu yayımlamak için bir UNC yolu kullanılarak yolunu girin (\\\Server\ApplicationName) veya bir dosya yolu (C:\Deploy\ApplicationName).

   - FTP sunucusuna yayımlamak için ftp://ftp.microsoft.com/ApplicationName biçimini kullanarak yolunu girin.

     Metin mevcut olması gerektiğini unutmayın **yayımlama konumu** Gözat sırayla kutusuna (**...** ) çalışmaya düğmesi.

## <a name="see-also"></a>Ayrıca Bkz.
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md) [nasıl yapılır: Yayımlama Sihirbazını Kullanarak ClickOnce Uygulaması Yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)
