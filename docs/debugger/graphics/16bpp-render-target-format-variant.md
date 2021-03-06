---
title: 16bpp işleme hedef biçim çeşidi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 24b22ad9-5ad0-4161-809a-9b518eb924bf
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 94775b717a3095d54d3fa52e3d2a5325dc3d21c5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62896429"
---
# <a name="16-bpp-render-target-format-variant"></a>16 bpp hedef biçimi değişken işleme
Piksel biçimlendirmek için DXGI_FORMAT_B5G6R5_UNORM tüm ayarlar, işleme hedefleri ve arabellek yedekleyin.

## <a name="interpretation"></a>Yorumu
 İşleme hedefi veya geri arabelleği genellikle B8G8R8A8_UNORM gibi bir 32 bpp (32 bit / piksel) biçimi kullanır. 32-bpp biçimleri büyük miktarda bellek bant genişliği tüketebilir. B5G6R5_UNORM biçimi 32 bpp biçimlerinin boyutunda bir 16 bpp biçimde olduğundan, bunu kullanan baskısı bellek bant genişliği, ancak daha az renk uygunluk, hafifletmek.

 Bu değişken, bir büyük bir performans kazancı gösteriyorsa, bu büyük olasılıkla uygulamanızı çok fazla bellek bant genişliği tüketir gösterir. Özellikle, profili oluşturulan çerçeve overdraw veya alfa karıştırma önemli miktarda varken önemli bir performans geliştirmesi elde edebilirsiniz.

Uygulamanız aşağıdaki koşullara sahip olduğunda 16 bpp işleme hedef biçim bellek bant kullanımına sahip azaltabilirsiniz:
- Yüksek kaliteli renk çoğaltılması gerekmez.
- Alfa kanalını gerektirmez.
- (Bu daha az renk uygunluk altında Şerit yapılara açıktır) kesintisiz gradyanlar ofent sahip değil.

Bellek bant genişliğini azaltmak üzere diğer stratejiler şunlardır:
- Overdraw veya alfa karıştırma miktarını azaltın.
- Çerçeve arabelleği boyutunu azaltın.
- Doku kaynakları boyutunu azaltın.
- Doku kaynakları sıkıştırmaları azaltın.

Her zamanki şekilde resmi kalite herhangi birini bu iyileştirmeler ile gelen dengelemeler düşünmek zorunda.

Takas zinciri bir parçası olan uygulamaları 16 bpp desteklemeyen bir arka arabellek biçimi (DXGI_FORMAT_B5G6R5_UNORM) sahiptir. Bu takas zincirleri kullanılarak oluşturulan `D3D11CreateDeviceAndSwapChain` veya `IDXGIFactory::CreateSwapChain`. Bu sınırlara yakın çalışmak için aşağıdaki adımları uygulayın:
1. Kullanarak B5G6R5_UNORM biçimi işleme hedefi oluşturma `CreateTexture2D` ve o hedefinde işleyin.
2. Takas zinciri arka arabelleği üzerine işleme hedefi bir tam ekran dört işleme hedefi olarak, kaynak doku ile çizerek kopyalayın.
3. Yoksa, takas zinciri üzerinde çağırın.

   Ardından bu strateji işleme hedefi için takas zinciri arka arabelleği kopyalayarak tüketilen daha fazla bant genişliği kaydederse, işleme performansı geliştirildi.

   Döşenmiş işleme tekniklerini GPU mimarileri, 16 bpp çerçeve arabellek biçimini kullanarak önemli performans avantajlarını görebiliyorum. Bu geliştirme, çerçeve arabelleği daha büyük bir kısmını her kutucuğun yerel çerçeve arabelleği önbellekte sığabilen olmasıdır. Döşenmiş işleme mimarisi, bazen ahizeleri mobil ve tablet bilgisayarlar Gpu'lar bulunur; Bu özel dışında nadiren görünürler.

## <a name="remarks"></a>Açıklamalar
 İşleme hedef biçim üzerinde yapılan her çağrı için DXGI_FORMAT_B5G6R5_UNORM sıfırlanır `ID3D11Device::CreateTexture2D` işleme hedefi oluşturur. Özellikle, pDesc içinde geçirilen D3D11_TEXTURE2D_DESC nesnesi bir işleme hedefi açıkladığında biçimi geçersiz; Yani:

- BindFlags üyesi, ayarlayın D3D11_BIND_REDNER_TARGET bayrağı vardır.

- BindFlags üye temizlenmiş D3D11_BIND_DEPTH_STENCIL bayrağı vardır.

- Kullanım üye D3D11_USAGE_DEFAULT için ayarlanır.

## <a name="restrictions-and-limitations"></a>Kısıtlamalar ve sınırlamalar
 Alfa kanalını B5G6R5 biçim olmadığından, alfa içerik bu değişken tarafından korunmaz. Uygulamanızın işleme, işleme hedefi bir alfa kanalına gerektiriyorsa, yalnızca B5G6R5 biçimine geçiş yapamazsınız.

## <a name="example"></a>Örnek
 **16 bpp işleme hedef biçim** değişken çoğaltılamaz kullanılarak oluşturulan işleme hedefleri için `CreateTexture2D` aşağıdakine benzer bir kod kullanarak:

```cpp
D3D11_TEXTURE2D_DESC target_description;

target_description.BindFlags = D3D11_BIND_RENDER_TARGET;
target_description.Format = DXGI_FORMAT_B5G6R5_UNORM;
d3d_device->CreateTexture2D(&target_description, nullptr, &render_target);
```
