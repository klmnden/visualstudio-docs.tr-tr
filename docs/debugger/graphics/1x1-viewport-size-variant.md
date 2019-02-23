---
title: 1 x 1 Görünüm penceresi boyut çeşidi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 3dbc3247-00f5-4644-8ff9-72e9febcf09a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a5b2c96b11c2075ce88b43cdebc34b905141c973
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56690428"
---
# <a name="1x1-viewport-size-variant"></a>1x1 Görünüm Penceresi Boyut Çeşidi
Tüm işleme hedeflerde Görünüm penceresi boyutları 1 x 1 piksel azaltır.

## <a name="interpretation"></a>Yorumu
 Daha küçük bir Görünüm penceresi, gölgelendirme için sahip olduğunuz piksel sayısını azaltır. Ancak, daha küçük bir Görünüm penceresi için sahip köşelerin sayısını azaltmaz işlem. Görünüm penceresi boyutları 1 x 1 piksel etkili bir şekilde ayarlanması piksel gölgelendirme uygulamanızdan ortadan kaldırır.

 Bu değişken, bir büyük bir performans kazancı gösteriyorsa, uygulamanızı doldurma oranı çok fazla tüketen gösterebilir. Ayrıca, uygulamanızı daha sonra üzerine önemli zaman gölgelendirme piksel harcayabilirsiniz veya çözünürlüğünüz hedef platform için çok yüksek olabilir, ayrıca olarak bilmeniz *overdraw*. Daha küçük bir çerçeve arabelleği veya overdraw miktarını azaltmayı uygulamanızın performansı iyileştirir.

## <a name="remarks"></a>Açıklamalar
 Görünüm penceresi boyutları 1 x 1 piksel yapılan her çağrı sonra sıfırlanır `ID3D11DeviceContext::OMSetRenderTargets` veya `ID3D11DeviceContext::RSSetViewports`.

## <a name="example"></a>Örnek
 Bu değişken, aşağıdaki kod ile yeniden oluşturulabilir:

```cpp
D3D11_VIEWPORT viewport;
viewport.TopLeftX = 0;
viewport.TopLeftY = 0;
viewport.Width = 1;
viewport.Height = 1;
d3d_context->RSSetViewports(1, &viewport);
```
