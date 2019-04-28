---
title: 'Nasıl yapılır: Grafik tanılama kayıttan yürütme makinesini değiştirme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 1b9aa3ea-29a0-4e21-bc57-936f33537b5c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cd1f893874a9b0cfe1c7cd36f8e0bb1c38beaca1
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63388560"
---
# <a name="how-to-change-the-graphics-diagnostics-playback-machine"></a>Nasıl yapılır: Grafik Tanılama Kayıttan Yürütme Makinesini Değiştirme
Yerel makinenizi kullanarak veya bir uzak makine ya da aygıt kullanarak grafik bilgilerini kayıttan yürütme.

## <a name="choosing-a-playback-machine"></a>Kayıttan yürütme makinesi seçme
 Kayıttan yürütme makinesi, bir makine ya da bir grafik günlüğünden grafik olaylarını kayıttan yürütmek için kullanılan cihaz ' dir. Genellikle yerel makine en kullanışlı seçenektir, ancak oluşturma sorununun nerede yakalanan farklı donanım veya sürücü sürümlerine makine sahip bir makinede oluşturma değil; Bu durumda, sorunu daha iyi yakalandığı bir uzak kayıttan yürütme makinesi seçebilir ve tanılamak için geliştirme makinenizi kullanmaya devam edebilirsiniz.

#### <a name="to-use-the-local-machine-to-play-back-graphics-information"></a>Grafik bilgilerini kayıttan çalıştırmak üzere yerel makine kullanmak için

1. Grafik günlüğü belge penceresinde seçin **kayıttan yürütme makinesi** bağlantı. **Uzaktan hata ayıklayıcı bağlantıları** iletişim kutusu görüntülenir.

2. Altında **el ile yapılandırma**, **adresi** özelliği girin `localhost`.

3. Ayarlama **kimlik doğrulama modu** özelliğini **hiçbiri**.

4. Seçin **seçin** düğmesi.

#### <a name="to-use-a-remote-machine-to-play-back-graphics-information"></a>Grafik bilgilerini kayıttan çalıştırmak üzere uzak bir makineyi kullanmak için

1. Grafik günlüğü belge penceresinde seçin **kayıttan yürütme makinesi** bağlantı. **Uzaktan hata ayıklayıcı bağlantıları** iletişim kutusu görüntülenir.

2. Altında **el ile yapılandırma**, **adresi** özelliği, Windows etki alanı adı veya makine ya da grafik bilgilerini kayıttan çalıştırmak üzere kullanmak istediğiniz cihazın IP adresini girin.

3. Yürütme makinesine bağlantıyı güvenli hale getirmek için kullanmak istediğiniz yetkilendirme türünü belirtin.

    - Windows kimlik doğrulaması için ayarlanmış **kimlik doğrulama modu** özelliğini **Windows**.

    - Kimlik doğrulaması için ayarlanmış **kimlik doğrulama modu** özelliğini **hiçbiri**.

4. Seçin **seçin** düğmesi.

> [!NOTE]
> **Uzaktan hata ayıklayıcı bağlantıları** iletişim kutusu, geliştirme makinenize doğrudan bağlı olan veya aynı alt ağda olan uzaktan hata ayıklama hedefleri de görüntüleyebilir. Bu uzaktan hata ayıklama hedeflerinden birini grafik tanılama kayıttan yürütme makinesi el ile yapılandırma olmadan kullanabilirsiniz. İçinde **uzaktan hata ayıklayıcı bağlantıları** iletişim kutusunda, istediğiniz ve ardından hedef seçin **seçin** düğmesi.

## <a name="see-also"></a>Ayrıca Bkz.
- [Grafik Günlük Belgesi](graphics-log-document.md)