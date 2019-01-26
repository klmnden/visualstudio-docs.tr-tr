---
title: 'Nasıl yapılır: XSLT ile Kesme Noktaları Kullanma'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7a569e3bc9d467b1cfce16d3836fdd1bb2a86e1c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55013697"
---
# <a name="how-to-use-breakpoints-with-xslt"></a>Nasıl yapılır: XSLT ile kesme noktaları kullanma

Bir XSLT stil sayfası veya XML kaynak belgesinde kesme noktaları ayarlayabilirsiniz. Ayarlarsanız kaynak satır bilgisi olan sonraki deyimi yürütme bir kesme noktası başlatıldığında bir etiketi, bir kesme noktasına taşınır.

Daha fazla bilgi için [hata ayıklama temelleri: Kesme noktaları](../debugger/using-breakpoints.md).

## <a name="set-a-breakpoint-in-a-style-sheet"></a>Bir stil sayfası içinde bir kesme noktası ayarlayın

Başlangıç etiketleri, bitiş etiketleri ve metin düğümleri bir XSLT stil sayfası üzerinde kesme noktaları ayarlanabilir. Kesme noktaları, aynı zamanda bir betik bloğu içindeki kod üzerinde ayarlanabilir.

### <a name="to-set-a-breakpoint-in-a-style-sheet"></a>Bir stil sayfası içinde bir kesme noktası ayarlamak için

1.  Bir stil sayfası XML düzenleyicisinde açın.

2.  Kesme noktası konumunda imleci getirin, sağ tıklayın, fareyle **kesme noktası**, tıklatıp **kesme noktası Ekle**.

3.  Gözat düğmesine tıklayın (**...** ) üzerinde **giriş** belge penceresinin alan.

4.  XML kaynak belge bulun ve tıklatın **açık**.

     Bu XSLT dönüşümü için kullanılan kaynak dosyanın ayarlar.

5.  Tıklayın **hata ayıklama XSL** XML Düzenleyicisi araç çubuğu düğmesi.

## <a name="set-a-breakpoint-in-an-xml-source-document"></a>Bir XML kaynak belgesinde bir kesme noktası ayarlayın

Kesme noktaları, öğeleri, öznitelikleri, ad alanı düğümü, açıklamalar, işlem yönergesi ve metin düğümleri bir XML kaynak belgesi üzerinde ayarlanabilir. Üst öğeden devralınan bir ad alanı düğümü veya belge düğümü üzerinde bir kesme noktası ayarlanamıyor.

### <a name="to-set-a-breakpoint-in-an-xml-source-document"></a>Bir XML kaynak belgesinde bir kesme noktası ayarlamak için

1.  XML belgesi bir XML düzenleyicisinde açın.

2.  Kesme noktası konumunda imleci getirin, sağ tıklayın, fareyle **kesme noktası**, tıklatıp **kesme noktası Ekle**.

3.  Gözat düğmesine tıklayın (**...** ) üzerinde **stil sayfası** belge penceresinin alan.

4.  XML kaynak belge bulun ve tıklatın **açık**.

     Bu XSLT dönüşümü için kullanılan kaynak dosyanın ayarlar.

5.  Tıklayın **hata ayıklama XSL** XML Düzenleyicisi araç çubuğu düğmesi.

## <a name="see-also"></a>Ayrıca bkz.

- [İzlenecek yol: Bir XSLT stil sayfasında hata ayıklama](../xml-tools/walkthrough-debug-an-xslt-style-sheet.md)