---
title: VLSC 'de görünen kişisel e-postalar
author: evanwindom
ms.author: lank
manager: lank
ms.date: 07/24/2019
ms.topic: conceptual
description: Visual Studio abonelikleri – My aboneleri için hotmail veya Gmail adreslerini görüyorum mi?
ms.openlocfilehash: 8418a177e793f0b4fe9a5019d2cf62fa724312ff
ms.sourcegitcommit: ce1ab8a25c66a83e60eab80ed8e1596fe66dd85c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/29/2019
ms.locfileid: "68605759"
---
# <a name="visual-studio-subscriptions--why-am-i-seeing-hotmail-or-gmail-addresses-for-my-subscribers"></a>Visual Studio abonelikleri – My aboneleri için hotmail veya Gmail adreslerini görüyorum mi?
Toplu Lisanslama hizmeti Merkezi 'nden (VLSC) yeni Visual Studio [abonelikleri yönetim portalına](https://manage.visualstudio.com)geçiş yaptıktan sonra Yöneticiler, bazı aboneler Için "oturum açma e-posta adresinin" bir üçüncü taraf e-postası gösterdiğini bulmamaktadır. Hotmail, Gmail veya Yahoo gibi adresler.  Daha fazla bilgi için [Bu videoya](https://www.youtube.com/watch?v=J61EYaVN-dQ&list=PLReL099Y5nReJhZ6o8CQFPSBgzGCHX99_&index=6)göz atın.

## <a name="cause"></a>Sebep
Bu senaryo, eski MSDN abone deneyimiyle ilişkili oturum açma işlemlerinden dolayı oluşur. Kullanıcılar toplu lisans hizmeti Merkezi 'nden (VLSC), değişiklikler olmadan Visual Studio abonelikleri yönetim portalına geçirildi. Yöneticiler, kullanıcıların abonelik avantajlarına erişmek için kişisel hesapları kullandığını fark edemeyebilir. 2016 ' de tamamlanan Visual Studio abonesi geçişleri öncesinde, Visual Studio aboneliğini başarıyla kullanmak için iki eylem gerekiyordu:
1. "Atanan" Yönetici, iş veya okul e-posta adreslerini kullanarak tek bir abone için aboneliği "atandı".
2. Abone "etkinleştirildi".

Abone etkinleştirme işlemi sırasında: Oturum açmak için bir Microsoft hesabı (MSA) gerekiyordu. Abone, iş veya okul hesabını (ör. tasha@contoso.combir MSA) yapmayı denemediyse, yeni bir MSA oluşturabilir veya var olan bir bu kişinin faydalanabilir. Bunun sonucunda "oturum açma e-posta adresi", "e-posta adresi atandı" olarak farklılık Açamıştı.

> [!NOTE]
> Üzerinde [https://my.visualstudio.com](https://my.visualstudio.com?wt.mc_id=o~msft~docs) yeni abone deneyimi hem iş/okul hem de Microsoft hesabı (MAA) kimlik türlerini destekler.

Son olarak, yönetici geçişi yeni abone yönetimi deneyimini doldurmak için abonenin "oturum açma e-posta adresi" ile ilgili VLSC 'den veri gönderdiğinden, yakın zamanda geçirilmiş Yöneticiler bu önceden fark edilmemiş kişisel hesapları görmüş olabilir Kullanıcı arabirimindeki değişiklikler nedeniyle, bu bilgileri daha görünür hale geçirir.

## <a name="solution"></a>Çözüm
Sorunu gidermek için, oturum açma e-posta adreslerini güncelleştirmek üzere abone bilgilerini düzenlemeniz gerekir.  Ayrı aboneler veya toplu olarak düzenlemeler yapılabilir. Tüm bilgiler için lütfen [abonelikleri Düzenle](edit-license.md)' yi ziyaret edin.

##  <a name="next-steps"></a>Sonraki adımlar
- Abone (ler) e-posta adreslerini güncelleştirdiyseniz, oturum açma bilgilerinin değiştiğini bildirmek isteyebilirsiniz.  Ayrıca, güncelleştirilmiş bilgileri içeren bir e-posta alırlar.
- Değişiklik yapması gerekebilecek herhangi bir oturum açma e-posta adresini aramak için kuruluşunuzdaki [abone listesini filtrelemek](search-license.md) yararlı olabilir.  

