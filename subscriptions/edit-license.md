---
title: Yönetim portalında abonelikleri düzenleyin | Microsoft Docs
author: evanwindom
ms.author: lank
manager: lank
ms.date: 07/28/2019
ms.topic: conceptual
description: Yöneticilerin abonelik atamalarını nasıl düzenleyebileceğinizi öğrenin.
ms.openlocfilehash: e55cee74f861973e3cc29e3f19dc9b31a107f437
ms.sourcegitcommit: ce1ab8a25c66a83e60eab80ed8e1596fe66dd85c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/29/2019
ms.locfileid: "68605671"
---
# <a name="edit-visual-studio-subscription-assignments"></a>Visual Studio abonelik atamalarını Düzenle
Bir abonelik Yöneticisi olarak, kuruluşunuzdaki kişilere atanan aboneliklerde değişiklikler yapabilirsiniz.  Bu makale, yapabileceğiniz değişiklik türlerini açıklar ve gerekli adımları sağlar.

## <a name="change-subscriber-information"></a>Abone bilgilerini değiştirme
Hataları düzeltmek veya bilgileri güncelleştirmek için bir abonenin bilgilerini düzenleyebilirsiniz.

Bir aboneyi düzenlemek için, farenizi onun üzerine getirdiğinizde abonenin e-posta adresinin yanında görünen üç nokta (...) simgesini seçin. Bir açılan menü görüntülenir.  Abonenin ayrıntılarını değiştirmek için **Düzenle** ' yi seçin. Ayrıca düzenleme penceresini açmak için, kılavuzdaki abone satırına çift tıklayabilirsiniz.
> [!div class="mx-imgBorder"]
> ![Düzenlemek için abone seçin](_img/edit-license/select-subscriber.png)

Abonenin adı, soyadı, ülke, dil ve İndirmeleri güncelleştirebilirsiniz. Abonenin bilgilerini düzenleyin ve **Kaydet**' e tıklayın.

   > [!NOTE]
   > Abone için abonelik düzeyini değiştirmeniz gerekiyorsa, kullanıcıyı portaldan silip yeniden eklemeniz gerekir. Abonelik düzeyleri düzenlenemez.

## <a name="edit-multiple-subscribers-using-bulk-edit"></a>Toplu düzenleme kullanarak birden çok aboneyi düzenleme
Toplu düzenleme işlemini kullanarak, aynı anda birden çok aboneyi düzenleyebilirsiniz. Bu özellik öncelikle Kurumsal e-posta adresi değişikliklerinden veya bir kuruluşun indirmelere erişimi kısıtlamaya karar verdiği kuruluşlarda kullanılır.

   > [!IMPORTANT]
   > Abonelik düzeyleri (örneğin, Enterprise, Professional, vs.) ve abonelik GUID 'Leri değiştirilemez.  Bu öğelerle değiştirilen bir karşıya yüklemeyi denerseniz karşıya yükleme başarısız olur.

1. Birden çok aboneyi aynı anda düzenlemek için, aboneler sekmesine gidin. Üstteki şeritte **toplu düzenleme**' ye tıklayın.

2. Toplu düzenleme, abone bilgilerinde düzenlemeler yapmak için bir Excel şablonu kullanır. Toplu düzenleme kutusunda, tüm bilgileri de dahil olmak üzere geçerli aboneler listesini indirmek için **Bu Excel 'ı dışarı aktar** ' a tıklayın.
   > [!div class="mx-imgBorder"]
   > ![Bir lisansı düzenleme-toplu düzenlemeler listesini dışarı aktarma](_img/edit-license/edit-license-bulk-edit-export.png)

3. Daha sonra, dosyayı kolayca bulabilmek ve karşıya yüklemeden önce gerekli değişiklikleri yapabilmek için dosyayı yerel olarak kaydedin. Başarılı bir karşıya yükleme sağlamak için **abonelik düzeyini veya ABONELIK GUID** 'sini düzenlemediğinizden, yüklemenin başarısız olmasına neden olur.

4. Visual Studio abonelikleri yönetim portalına dönün ve toplu düzenleme iletişim kutusunda, **Araştır**' a tıklayın. Kaydettiğiniz Excel dosyasını seçin ve **Tamam**' a tıklayın. Karşıya yükleme ilerlemesini ekranda görürsünüz.
   > [!div class="mx-imgBorder"]
   > ![Lisans-toplu düzenleme dosya yükleme](_img/edit-license/edit-license-bulk-file-upload1.png)

5. Dosyayı karşıya yükledikten sonra, başarılı olduğunu bildiren bir bildirim görürsünüz. Bu noktada, düzenlemeleriniz abone bilgilerine yansıtılır.

## <a name="next-steps"></a>Sonraki adımlar
- Belirli bir aboneliği bulma konusunda yardım için [bir abonelik aramaya](search-license.md)göz atın.
- Aboneliklerinizin bir listesini oluşturmanız mı gerekiyor?  [Dışarı aktarma abonelikleri](exporting-subscriptions.md)göz atın.