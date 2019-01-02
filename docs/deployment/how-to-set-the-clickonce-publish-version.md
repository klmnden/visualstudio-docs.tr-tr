---
title: 'Nasıl Yapılır: Kümesi ClickOnce yayım sürümü | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, setting publish version
- publishing, ClickOnce
- Publish Version property
ms.assetid: 06f15504-6385-40a6-b01d-cd90ca36dc73
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: bd0f38fda93d1a91e72c547bdfe230354988da9d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53869118"
---
# <a name="how-to-set-the-clickonce-publish-version"></a>Nasıl Yapılır: Kümesi ClickOnce yayım sürümü
[!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] `Publish Version` Özelliği yayımlamakta olduğunuz uygulamayı güncelleştirme olarak kabul edilip edilmeyeceğini belirler. Her zaman sürümü artırılır, uygulama bir güncelleştirme olarak yayımlanır.  
  
 `Publish Version` Özelliği, üzerinde ayarlanabilir **Yayımla** sayfasının **Proje Tasarımcısı**.  
  
> [!NOTE]
>  Otomatik artış bir proje seçeneği `Publish Version` özelliği her zaman uygulama yayımlanır; bu seçenek varsayılan olarak etkindir. Daha fazla bilgi için [nasıl yapılır: Artırma ClickOnce yayım sürümünü otomatik olarak](../deployment/how-to-automatically-increment-the-clickonce-publish-version.md).  
  
### <a name="to-change-the-publish-version"></a>Yayınlama sürümünü değiştirmek için  
  
1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünü tıklatın **özellikleri**.  
  
2.  Tıklayın **Yayımla** sekmesi.  
  
3.  İçinde **yayımlama sürümü** artış, alan **ana**, **küçük**, **derleme**, veya **düzeltme** sürümü sayı.  
  
    > [!NOTE]
    >  Hiçbir zaman bir sürüm numarası azaltmayın. Bunun yapılması, bu nedenle öngörülemeyen güncelleştirme davranışlara neden olabilir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [ClickOnce güncelleştirme stratejisini seçin](../deployment/choosing-a-clickonce-update-strategy.md)   
 [Nasıl yapılır: Otomatik olarak artırma ClickOnce yayım sürümü](../deployment/how-to-automatically-increment-the-clickonce-publish-version.md)   
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)   
 [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)