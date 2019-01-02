---
title: XSLT Varsayılan Şablonları
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 773dd34e-67d3-4997-8df9-b71e7f880d88
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 2eb71cf0a94f02e5de8af9e61bdc947694920929
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53908390"
---
# <a name="xslt-default-templates"></a>XSLT varsayılan şablonları

Varsayılan bir şablon XSLT stil sayfasında eşleşen hiçbir açık şablon kuralı olduğunda işleme sırasında kullanılır. Yerleşik bir şablon kuralı olarak da adlandırılan varsayılan şablonu W3C XSLT 1.0 önerisi 5.8 bölümünde tanımlanır. Eşleşecek hiçbir açık şablon kuralı olsa bile varsayılan şablonun bir düğüm işlemek için XSLT işlemci sağlar. Ancak, yerleşik bir şablon kural stil sayfası içinde açıkça tanımlanmayan çünkü bu beklenmeyen veya karmaşık XSLT dönüştürme sonuçlara neden olabilir.

XSLT hata ayıklayıcısı artık XSLT varsayılan şablonları kodunu görüntüler. Varsayılan bir şablon kullanılıyorsa bir XSLT dönüşümü adımladığınızda hata ayıklayıcısı varsayılan şablonu bir pencerede açar. Bu, varsayılan şablonunun kod içinde gezinebilmek ve kesme noktaları ayarlayın, yönergeler sağlar.

## <a name="see-also"></a>Ayrıca bkz.

- [XSLT Hatalarını Ayıklama](../xml-tools/debugging-xslt.md)