---
title: 'Test Alanı 2: Kaynak denetiminden almak | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, getting items from source control
- source control [Visual Studio SDK], getting items from
ms.assetid: cbd345c5-ca43-4630-b7a4-85564f4e2090
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0d7942aa658208143aea3c3ae3a09eb677568f17
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60067189"
---
# <a name="test-area-2-get-from-source-control"></a>Test Alanı 2: Kaynak Denetiminden Alma
Bu test alanı Get komutu aracılığıyla sürüm deposundan öğeleri almak için test çalışmaları kapsar. Bu test çalışmaları, yerel ve Web projeleri için uygulanabilir.

## <a name="command-menu-access"></a>Komut menü erişimi
 Aşağıdaki [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı menüsü yolları test durumlarında kullanılır.

##### <a name="get-latest-version"></a>En son sürümü Al:

- **Dosya**, **kaynak denetimi**, **en son sürümü Al**.

- **Dosya**, **en son sürümü Al**.

- Kısayol menüsünde, **en son sürümü Al**.

- Al: **Dosya**, **kaynak denetimi**, **alma**.

## <a name="expected-behavior"></a>Beklenen davranış

##### <a name="get-latest-version"></a>En son sürümü Al:
 Bir öğenin en son sürümünü (kullanıcı Arabirimi) Sessiz alınmasını sürüm Mağazası'ndan gerçekleştirir.

##### <a name="get"></a>Al:
 Görüntüler **alma** iletişim kutusu ve kullanıcının değişiklik alınır yanı sıra dosyaların nasıl alınır etkileyen seçenekleri değiştirmek, dosya kümesine izin verir.

## <a name="test-cases"></a>Test çalışmaları

|Eylem|Test adımları|Beklenen sonuçları doğrulamak için|
|------------|----------------|--------------------------------|
|Yerel olarak mevcut olmayan bir dosyanın en son sürümü Al|1.  Bir proje oluşturun.<br />2.  Projeye bir öğe ekleyin.<br />3.  Projenin kaynak denetimi altına yerleştirin.<br />4.  Öğenin yerel kopyasını silin.<br />5.  Öğenin en son sürümü Al (kısayol menüsünde, **en son sürümü Al**).|Öğesi dosyasını yerel olarak alınır.|
|Yerel olarak mevcut olmayan bir dosya alın|1.  Bir proje oluşturun.<br />2.  Projeye bir öğe ekleyin.<br />3.  Projenin kaynak denetimi altına yerleştirin.<br />4.  Öğenin yerel kopyasını silin.<br />5.  Öğe alma (**dosya**, **kaynak denetimi**, **alma** \<öğesi >).|Öğesi dosyasını yerel olarak alınır.|
|Özel olarak kullanıma ve yerel olarak değiştiren bir dosya alın|1.  Bir proje oluşturun.<br />2.  Projeye bir öğe ekleyin.<br />3.  Projenin kaynak denetimi altına yerleştirin.<br />4.  Proje öğesi özel kontrol edin.<br />5.  Yerel kopya değiştirin.<br />6.  Öğenin en son sürümü Al (**dosya**, **en son sürümü Al** \<öğesi >). Bu adım başarılı olursa, sonraki adıma geçin.<br />7.  Tıklayın **değiştirin** uyarı iletişim kutusunda düğmesi.|**6. adımdan reResult** `:`<br /><br /> Uyarı iletişim kutusunda, bu dosya kullanıma gösterir.<br /><br /> **7. adımdan reResult:**<br /><br /> Değiştirilen yerel dosya sürümü Mağazası'ndan özgün sürümle değiştirilir.<br /><br /> Okuma/yazma dosyasıdır.|
|Alma ve kullanıma, paylaşılan ve yerel olarak değiştirilen dosya değiştirin|1.  Yeni bir proje oluşturun.<br />2.  Projeye bir öğe ekleyin.<br />3.  Projenin kaynak denetimi altına yerleştirin.<br />4.  Proje öğesi paylaşılan olarak göz atın.<br />5.  Yerel kopya değiştirin.<br />6.  Öğenin en son sürümü Al (**dosya**, **en son sürümü Al** \<öğesi >). Bu adım başarılı olursa, sonraki adıma geçin.<br />7.  Tıklayın **değiştirin** uyarı iletişim kutusunda.|**6. adımdan sonuç:**<br /><br /> Uyarı iletişim kutusunda, bu dosya kullanıma gösterir.<br /><br /> **7. adımdan sonuç:**<br /><br /> Değiştirilen yerel dosya sürümü Mağazası'ndan özgün sürümle değiştirilir.<br /><br /> Okuma/yazma dosyasıdır.|
|Yerel olarak mevcut bir dosyayı aynı sürüm deposuna en son sürümü Al|1.  Yeni bir proje oluşturun.<br />2.  Projeye bir öğe ekleyin.<br />3.  Projenin kaynak denetimi altına yerleştirin.<br />4.  Öğe alma (**dosya**, **kaynak denetimi**, **alma** \<öğesi >).|Yerel dosya değiştirilmez.|
|Bir proje içeren bir çözümünü edinme|1.  Bir çözümü ile bir proje oluşturun.<br />2.  Çözüm kaynak denetimi altına yerleştirin.<br />3.  Tüm proje dosyaları yerel olarak sil.<br />4.  Çözümünü edinme (**dosya**, **kaynak denetimi**, **alma**).|Tüm silinen dosyaları yerel olarak geri yüklenir.|

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentileri için Test Kılavuzu](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)