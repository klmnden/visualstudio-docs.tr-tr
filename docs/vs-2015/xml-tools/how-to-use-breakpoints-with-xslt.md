---
title: 'Nasıl yapılır: XSLT ile kesme noktaları kullanma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: bf7bbc2c-71dc-4cac-a6fc-add6b27d92ed
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 5590d9f33d2c34b7d3d86aaf00307419685ca8da
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54773274"
---
# <a name="how-to-use-breakpoints-with-xslt"></a>Nasıl yapılır: XSLT ile Kesme Noktaları Kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir XSLT stil sayfası veya XML kaynak belgesinde kesme noktaları ayarlayabilirsiniz. Ayarlarsanız kaynak satır bilgisi olan sonraki deyimi yürütme bir kesme noktası başlatıldığında bir etiketi, bir kesme noktasına taşınır.  
  
 Daha fazla bilgi için [hata ayıklama temelleri: Kesme noktaları](http://msdn.microsoft.com/752a02c2-0ac7-4c8b-aa1b-4b2b3b21152e).  
  
## <a name="set-a-breakpoint-in-a-style-sheet"></a>Bir stil sayfası içinde bir kesme noktası ayarlayın  
 Başlangıç etiketleri, bitiş etiketleri ve metin düğümleri bir XSLT stil sayfası üzerinde kesme noktaları ayarlanabilir. Kesme noktaları, aynı zamanda bir betik bloğu içindeki kod üzerinde ayarlanabilir.  
  
#### <a name="to-set-a-breakpoint-in-a-style-sheet"></a>Bir stil sayfası içinde bir kesme noktası ayarlamak için  
  
1.  Bir stil sayfası XML düzenleyicisinde açın.  
  
2.  Kesme noktası konumunda imleci getirin, sağ tıklayın, fareyle **kesme noktası**, tıklatıp **kesme noktası Ekle**.  
  
3.  Göz at düğmesine Gözat'a tıklayın (**...** ) üzerinde **giriş** belge penceresinin alan.  
  
4.  XML kaynak belge bulun ve tıklatın **açık**.  
  
     Bu XSLT dönüşümü için kullanılan kaynak dosyanın ayarlar.  
  
5.  Tıklayın **hata ayıklama XSL** XML Düzenleyicisi araç çubuğu düğmesi.  
  
## <a name="set-a-breakpoint-in-an-xml-source-document"></a>Bir XML kaynak belgesinde bir kesme noktası ayarlayın  
 Kesme noktaları, öğeleri, öznitelikleri, ad alanı düğümü, açıklamalar, işlem yönergesi ve metin düğümleri bir XML kaynak belgesi üzerinde ayarlanabilir. Üst öğeden devralınan bir ad alanı düğümü veya belge düğümü üzerinde bir kesme noktası ayarlanamıyor.  
  
#### <a name="to-set-a-breakpoint-in-an-xml-source-document"></a>Bir XML kaynak belgesinde bir kesme noktası ayarlamak için  
  
1.  XML belgesi bir XML düzenleyicisinde açın.  
  
2.  Kesme noktası konumunda imleci getirin, sağ tıklayın, fareyle **kesme noktası**, tıklatıp **kesme noktası Ekle**.  
  
3.  Göz at düğmesine Gözat'a tıklayın (**...** ) üzerinde **stil sayfası** belge penceresinin alan.  
  
4.  XML kaynak belge bulun ve tıklatın **açık**.  
  
     Bu XSLT dönüşümü için kullanılan kaynak dosyanın ayarlar.  
  
5.  Tıklayın **hata ayıklama XSL** XML Düzenleyicisi araç çubuğu düğmesi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İzlenecek yol: Bir XSLT stil sayfasında hata ayıklama](../xml-tools/walkthrough-debug-an-xslt-style-sheet.md)
