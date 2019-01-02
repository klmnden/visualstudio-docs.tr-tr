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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ab842ce4f66684bf167d3cf627ce8cde82c5ea7c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53830381"
---
# <a name="how-to-specify-where-visual-studio-copies-the-files"></a>Nasıl Yapılır: Visual Studio'nun dosyaları nereye kopyalayacağını belirtme
ClickOnce kullanarak bir uygulamayı yayımladığınızda `Publish Location` özelliği burada bildirimini ve uygulama dosyalarını isimlerine konumunu belirtir. Bu, bir dosya yolu veya bir FTP sunucusuna bir yolu olabilir.  
  
 Belirtebileceğiniz `Publish Location` özelliği **Yayımla** sayfasının **Proje Tasarımcısı**, veya Yayımlama Sihirbazı'nı kullanarak. Daha fazla bilgi için [nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md).  
  
> [!NOTE]
>  ClickOnce kullanarak bir uygulamanın birden fazla sürüm yüklediğinizde, yükleme uygulamanın önceki sürümlerini belirttiğiniz yayımlama konum arşivinde adlı bir klasöre taşır. Yükleme dizini temizler önceki sürümünden önceki sürümleri bu şekilde korur arşivleme.  
  
### <a name="to-specify-a-publishing-location"></a>Bir yayımlama konumu belirtmek için  
  
1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2. Tıklayın **Yayımla** sekmesi.  
  
3. İçinde **yayımlama konumu** aşağıdaki biçimlerden birini kullanarak Yayınlama konumu girin:  
  
   - Bir dosya paylaşımını veya disk yolu yayımlamak için bir UNC yolu kullanılarak yolunu girin (*\\\Server\ApplicationName*) veya bir dosya yolu (*C:\Deploy\ApplicationName*).  
  
   - FTP sunucusuna yayımlamak için yol biçimi kullanarak girin <em>ftp://ftp.microsoft.com/\<ApplicationName ></em>.  
  
     Metin mevcut olması gerektiğini unutmayın **yayımlama konumu** Gözat sırayla kutusuna (**...** ) çalışmaya düğmesi.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)   
 [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)