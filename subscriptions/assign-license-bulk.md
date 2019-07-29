---
title: Visual Studio abonelikleri için Kullanıcı gruplarına lisans atama | Microsoft Docs
author: evanwindom
ms.author: lank
manager: lank
ms.date: 07/24/2019
ms.topic: conceptual
description: Yöneticilerin birden çok aboneye nasıl lisans atayabileceği hakkında bilgi edinin
ms.openlocfilehash: 7d54dcf3cf3e7fea7845a4e9a0053de4ba734ae9
ms.sourcegitcommit: ce1ab8a25c66a83e60eab80ed8e1596fe66dd85c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/29/2019
ms.locfileid: "68611906"
---
# <a name="assign-subscriptions-to-multiple-users"></a>Birden çok kullanıcıya abonelik atama
Abonelikler yönetim portalı, kullanıcıları tek seferde veya büyük gruplar halinde eklemenize olanak tanır.  Bireysel kullanıcı eklemek için bkz. [tek kullanıcı ekleme](assign-license.md).

## <a name="use-bulk-add-to-assign-subscriptions"></a>Abonelik atamak için toplu ekleme kullanma
1. Üzerinde https://manage.visualstudio.com Visual Studio abonelikleri Yönetim Portalı ' nda oturum açın.
2. Tek seferde birden çok abone eklemek için, **aboneleri Yönet** sekmesine gidin. Üstteki şeritte **toplu Ekle**' ye tıklayın.
   > [!div class="mx-imgBorder"]
   > ![Birden çok abone ekleme](media/add-multiple-subscribers.png)

2. Toplu ekleme, abone bilgilerini karşıya yüklemek için bir Microsoft Excel şablonu kullanır. Birden çok aboneyi karşıya yükle iletişim kutusunda şablonu indirmek için **İndir** ' e tıklayın.
   > [!div class="mx-imgBorder"]
   > ![Birden çok aboneyi karşıya yüklemek için Excel şablonunu indirin](media/download-template-upload-subscribers.png)
   >
   > [!NOTE]
   > Bu şablonun en son sürümünü her zaman indirin. Daha eski bir sürüm kullanıyorsanız toplu karşıya yükleme işlemi başarısız olabilir.

3. Excel elektronik tablosunda, abonelik atamak istediğiniz kişilerin bilgilerini içeren alanları doldurun. (*Başvuru* isteğe bağlı bir alandır.) İşiniz bittiğinde dosyayı yerel olarak kaydedin.

   Düzgün bir karşıya yükleme sağlamaya yardımcı olmak için aşağıdaki en iyi yöntemleri inceleyin:

    - Form alanlarının hiçbirinin virgüller içermediğinden emin olun.
    - Form alanlarından önce ve sonra boşlukları kaldır.
    - Kullanıcının adlarının iki parçalı ad veya soyadı arasında fazladan boşluk olmadığından emin olun (örneğin, bir kişi "Mıknatılis Mayıs" gibi iki bölümden oluşan bir ada sahipse, sistem ek alanı kırpmadığından "Mıknatıgiemay" olarak yazılmalıdır.)

4. Visual Studio abonelikleri yönetim portalına dönün. **Birden çok aboneyi karşıya yükle** iletişim kutusunda, **görüntüle**' ye tıklayın.
   > [!div class="mx-imgBorder"]
   > ![Birden çok aboneyi karşıya yüklemek için kaydedilmiş şablonunuz 'na gidin](media/bulk-add-browse-saved-template.png)

5. Kaydettiğiniz Excel dosyasına gidin ve ardından **Tamam**' a tıklayın.
   > [!div class="mx-imgBorder"]
   > ![Birden çok aboneyi karşıya yüklemek için Excel şablonunu karşıya yükleyin](media/bulk-upload-subscribers.png)

    Karşıya yükleme ilerleme durumu iletişim kutusu görüntülenir.

    Şablonda hatalar varsa, karşıya yükleme başarısız olur ve şablonu düzeltebilmeniz ve toplu karşıya yüklemeyi yeniden denemeniz için hatalar gösterilir.
   > [!div class="mx-imgBorder"]
   > ![Birden çok aboneye yükleme başarısız olursa hata iletisi](media/bulk-add-template-failed.png)

    Karşıya yükleme başarılı olduğunda, aboneler listesini ve bir onay iletisi görürsünüz.
   > [!div class="mx-imgBorder"]
   > ![Birden çok abonelerin karşıya yüklenmesi başarılı olursa onay iletisi](media/bulk-add-template-success.png)

## <a name="next-steps"></a>Sonraki adımlar
- Eklemek için yalnızca bir veya iki abone mi var?  [Tek Kullanıcı Ekle](assign-license.md) 'ye göz atın
- Mevcut abonelikleri nasıl [düzenleyeceğinizi](edit-license.md) öğrenin
- Yardıma mı ihtiyacınız var? [Visual Studio yönetim ve abonelikler desteğiyle](https://visualstudio.microsoft.com/support/support-overview-vs)iletişim kurun.
