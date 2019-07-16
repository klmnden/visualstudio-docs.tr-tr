---
title: 1 x 1 Görünüm penceresi boyut çeşidi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 3dbc3247-00f5-4644-8ff9-72e9febcf09a
caps.latest.revision: 9
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 74e3bc706cb2df12aacddf9fbb77dec598bfc17a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68157561"
---
# <a name="1x1-viewport-size-variant"></a>1x1 Görünüm Penceresi Boyut Çeşidi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Tüm işleme hedeflerde Görünüm penceresi boyutları 1 x 1 piksel azaltır.  
  
## <a name="interpretation"></a>Yorumu  
 Daha küçük bir Görünüm penceresi gölgeli olmalı, ancak işlenmesi gereken köşelerin sayısını azaltmaz piksel sayısını azaltır. Görünüm penceresi boyutları 1 x 1 piksel etkili bir şekilde ayarlanması piksel gölgelendirme uygulamanızdan ortadan kaldırır.  
  
 Bu değişken, bir büyük bir performans kazancı gösteriyorsa, uygulamanızın çok fazla fillrate kullandığı gösterebilir. Bu seçtiğiniz çözüm için hedef platform çok yüksek olup olmadığını veya uygulamanızı daha sonra üzerine önemli zaman gölgelendirme piksel harcadığı gösterebilir (overdraw). Bu sonuç önerir, framebuffer boyutunu azaltma veya overdraw miktarını azaltmak için uygulamanızın performansı iyileştirir.  
  
## <a name="remarks"></a>Açıklamalar  
 Görünüm penceresi boyutları 1 x 1 piksel yapılan her çağrı sonra sıfırlanır `ID3D11DeviceContext::OMSetRenderTargets` veya `ID3D11DeviceContext::RSSetViewports`.  
  
## <a name="example"></a>Örnek  
 Bu değişken bu kodu kullanarak yeniden oluşturulabilir:  
  
```  
D3D11_VIEWPORT viewport;  
viewport.TopLeftX = 0;  
viewport.TopLeftY = 0;  
viewport.Width = 1;  
viewport.Height = 1;  
d3d_context->RSSetViewports(1, &viewport);  
```
