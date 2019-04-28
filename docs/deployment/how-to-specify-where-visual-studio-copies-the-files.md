---
title: Dosyaları kopyalamak istediğiniz yeri belirtin | Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- publishing, specifying location
- Publish Location property
ms.assetid: 6c552700-dda3-49fe-af98-4717344fda07
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ec54a2d3150b0e8e11b19d2ca739324d7388f1f0
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63407649"
---
# <a name="how-to-specify-where-visual-studio-copies-the-files"></a>Nasıl yapılır: Visual Studio'nun dosyaları nereye kopyalayacağını belirtme
ClickOnce kullanarak bir uygulamayı yayımladığınızda `Publish Location` özelliği burada bildirimini ve uygulama dosyalarını isimlerine konumunu belirtir. Bu, bir dosya yolu veya bir FTP sunucusuna bir yolu olabilir.

 Belirtebileceğiniz `Publish Location` özelliği **Yayımla** sayfasının **Proje Tasarımcısı**, veya Yayımlama Sihirbazı'nı kullanarak. Daha fazla bilgi için [nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md).

> [!NOTE]
> ClickOnce kullanarak bir uygulamanın birden fazla sürüm yüklediğinizde, yükleme uygulamanın önceki sürümlerini belirttiğiniz yayımlama konum arşivinde adlı bir klasöre taşır. Yükleme dizini temizler önceki sürümünden önceki sürümleri bu şekilde korur arşivleme.

### <a name="to-specify-a-publishing-location"></a>Bir yayımlama konumu belirtmek için

1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.

2. Tıklayın **Yayımla** sekmesi.

3. İçinde **yayımlama konumu** aşağıdaki biçimlerden birini kullanarak Yayınlama konumu girin:

   - Bir dosya paylaşımını veya disk yolu yayımlamak için bir UNC yolu kullanılarak yolunu girin (*\\\Server\ApplicationName*) veya bir dosya yolu (*C:\Deploy\ApplicationName*).

   - FTP sunucusuna yayımlamak için yol biçimi kullanarak girin <em>ftp://ftp.microsoft.com/\<ApplicationName ></em>.

     Metin mevcut olması gerektiğini unutmayın **yayımlama konumu** Gözat sırayla kutusuna (**...** ) çalışmaya düğmesi.

## <a name="see-also"></a>Ayrıca bkz.
- [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)
- [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)