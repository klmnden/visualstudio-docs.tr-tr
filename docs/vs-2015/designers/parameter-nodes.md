---
title: Parametre düğümleri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
ms.assetid: da54db0b-3a3d-48dc-858c-7ac43aa04b13
caps.latest.revision: 12
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 110f380f7450d611de5786fb865bdee8e64195f6
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54764177"
---
# <a name="parameter-nodes"></a>Parametre Düğümleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Gölgelendirici Tasarımcısı'nda, çizim başına temelinde, uygulamanın denetiminde örnek olarak gölgelendirici, malzeme özelliklerine, tek yönlü ışık, kamera konumuna ve zaman girişleri parametre düğümleri temsil eder. Bu parametrelerin her bir çizim çağrısıyla değiştirebilirsiniz çünkü nesne farklı görünümlerini sağlamak için aynı gölgelendirici kullanabilirsiniz.  
  
## <a name="parameter-node-reference"></a>Parametre düğüm başvurusu  
  
|Düğüm|Ayrıntılar|Özellikler|  
|----------|-------------|----------------|  
|**Kamera dünya konumu**|Dünya alanındaki kameranın konumu.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float4`<br /> Kamera konumu.|Hiçbiri|  
|**Işık Yönü**|Işığın, dünya alanındaki bir ışık kaynağından saçıldığı yönü tanımlayan vektör.<br /><br /> Bunu, dünya alanındaki aydınlatma ve Yansımalı Katkıları hesaplamak için kullanabilirsiniz.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float3`<br /> Geçerli pikselin öğesinden bir ışık kaynağına.|Hiçbiri|  
|**Malzeme ortam**|Dolaylı Aydınlatmanın öznitelikli geçerli pikselin yayınık renk katkısı.<br /><br /> Bir pikselin yayınık rengi aydınlatma kaba yüzeyleri ile nasıl etkileştiğini benzetimini yapar. Malzeme ortam parametresi, dolaylı Aydınlatmanın gerçek dünyadaki bir nesnenin görünümüne nasıl katkıda bulunduğunu tahmin etmek için kullanabilirsiniz.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float4`<br /> Dolaylı nedeniyle olan geçerli pikselin yayınık rengi — diğer bir deyişle, ortam — aydınlatma.|**Erişim**<br /> **Genel** Model Düzenleyicisi'nden Ayarla; tersi durumda, özelliğini etkinleştirmek üzere **özel**.<br /><br /> **Değer**<br /> Dolaylı nedeniyle olan geçerli pikselin yayınık rengi — diğer bir deyişle, ortam — aydınlatma.|  
|**Malzeme Yayınık**|Geçerli pikselin doğrudan aydınlatmayı nasıl pürüzlü açıklayan bir renk.<br /><br /> Bir pikselin yayınık rengi aydınlatma kaba yüzeyleri ile nasıl etkileştiğini benzetimini yapar. Malzeme Yayınık parametresi, geçerli pikselin doğrudan aydınlatmayı nasıl pürüzlü değiştirmek için kullanabilirsiniz — diğer bir deyişle, doğrusal, nokta ve spot ışıklar.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float4`<br /> Geçerli pikselin doğrudan aydınlatmayı nasıl pürüzlü açıklayan bir renk.|**Erişim**<br /> **Genel** Model Düzenleyicisi'nden Ayarla; tersi durumda, özelliğini etkinleştirmek üzere **özel**.<br /><br /> **Değer**<br /> Geçerli pikselin doğrudan aydınlatmayı nasıl pürüzlü açıklayan bir renk.|  
|**Malzeme Yayımlatıcı**|Renk katkısı geçerli pikselin kendisine sağlayan aydınlatma uymama nedeniyle gerçekleşir.<br /><br /> Bu, Parlayan benzetimini yapmak için kullanabilirsiniz; yani kendi ışığını sağlayan bir nesne. Bu ışığın diğer nesneleri etkilememesine.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float4`<br /> Renk katkısı geçerli pikselin son tarihi için kendi kendine aydınlatmaya.|**Erişim**<br /> **Genel** Model Düzenleyicisi'nden Ayarla; tersi durumda, özelliğini etkinleştirmek üzere **özel**.<br /><br /> **Değer**<br /> Renk katkısı geçerli pikselin son tarihi için kendi kendine aydınlatmaya.|  
|**Malzeme Yansımalı**|Geçerli pikselin doğrudan aydınlatmayı nasıl yansıttığını açıklayan bir renk.<br /><br /> Bir pikselin Yansımalı renk aydınlatma pürüzsüz, ayna benzeri yüzeyleri ile nasıl etkileştiğini benzetimini yapar. Malzeme Yansımalı parametresi, geçerli pikselin doğrudan aydınlatmayı nasıl yansıttığını değiştirmek için kullanabilirsiniz — diğer bir deyişle, doğrusal, nokta ve spot ışıklar.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float4`<br /> Geçerli pikselin doğrudan aydınlatmayı nasıl yansıttığını açıklayan bir renk.|**Erişim**<br /> **Genel** özelliğin Model Düzenleyicisi'nden Ayarla; tersi durumda, izin vermek için **özel**.<br /><br /> **Değer**<br /> Geçerli pikselin doğrudan aydınlatmayı nasıl yansıttığını açıklayan bir renk.|  
|**Malzeme Yansımalı güç**|Yansımalı parlak alanların yoğunluğunu açıklayan skaler bir değer vurgular.<br /><br /> Yansımalı vurguları haline büyük Yansımalı güç, daha güçlü ve yılı.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float`<br /> Yansımalı parlak alanların yoğunluğunu açıklayan bir üstel terim, geçerli pikselin vurgular.|**Erişim**<br /> **Genel** Model Düzenleyicisi'nden Ayarla; tersi durumda, özelliğini etkinleştirmek üzere **özel**.<br /><br /> **Değer**<br /> Geçerli pikselin Yansımalı vurgular yoğunluğunu tanımlayan üs.|  
|**Normalleştirilmiş zaman**|Saniye cinsinden süre aralığına normalleştirilmiş [0, 1], saat 1 değerine ulaştığında 0 değerine Sıfırlanan.<br /><br /> Bu gölgelendirici hesaplamalarında bir parametre olarak örneğin doku koordinatlarına, renk değerlerine veya diğer özniteliklere animasyon uygulamak için kullanabilirsiniz.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float`<br /> Saniye cinsinden normalleştirilmiş süresi.|Hiçbiri|  
|**saat**|Saniye cinsinden süre.<br /><br /> Bu gölgelendirici hesaplamalarında bir parametre olarak örneğin doku koordinatlarına, renk değerlerine veya diğer özniteliklere animasyon uygulamak için kullanabilirsiniz.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float`<br /> Saniye cinsinden süre.|Hiçbiri|
