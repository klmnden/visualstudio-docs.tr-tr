---
title: Windows Information Protection dışında tut
ms.date: 06/01/2018
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 714d85ea41674563922903f5bf38db04ffc2fbce
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62978129"
---
# <a name="configure-visual-studio-as-a-wip-exempt-app"></a>Bir WIP muaf uygulaması olarak Visual Studio'yu yapılandırma

[Windows Information Protection](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip) (WIP) Kurumsal verileri e-posta, sosyal medya ve genel bulut, kuruluşun denetimi dışında kalan gibi uygulamalar aracılığıyla sızmasını önlemeye yardımcı olur. WIP ortamınız veya diğer uygulamalarda değişiklik yapmaya gerek kalmadan kuruluşa ait cihazlardaki ve kişisel cihazlarda yanlışlıkla veri sızıntılarına karşı korunmasına yardımcı olur.

*Kullanan* için WIP uygulama Kurumsal verileri korumasız ağ konumlarına gitmesini önlemek ve kişisel veri şifreleme önlemek için bekleniyor. Visual Studio, muaf sürece WIP etkin ortamlarda çalışmıyor bu nedenle bir uygulamaya değil. Visual Studio, WIP özellikli bir makinede işlevi sağlamak için bu makaledeki adımları izleyin.

## <a name="configure-vs-as-a-wip-exempt-app"></a>Bir WIP muaf uygulaması olarak VS yapılandırın

Visual Studio WIP kısıtlamalarından muaf ancak yine de kurumsal verileri kullanmasını sağlar. WIP muaf uygulamalar, Kurumsal bulut kaynakları için bir IP adresi veya ana bilgisayar adı kullanarak bağlanabilirsiniz. Şifreleme uygulanır ve uygulama yerel dosyalara erişebilirsiniz.

Visual Studio'dan WIP muaf tutmak için izleyin [dışarıda bir masaüstü uygulaması için adımları](/windows/security/information-protection/windows-information-protection/create-wip-policy-using-intune-azure#exempt-apps-from-a-wip-policy).

## <a name="create-a-wip-exempt-applocker-policy-file"></a>Bir WIP muaf AppLocker ilke dosyası oluşturma

Birden çok ikili dosyaları, Visual Studio içerdiği için [bir WIP muaf AppLocker ilke dosyası oluşturma](/windows/security/threat-protection/windows-defender-application-control/applocker/run-the-automatically-generate-rules-wizard). AppLocker kuralları bir klasördeki tüm dosyalar için otomatik olarak oluşturmanızı sağlar.

## <a name="add-appcompat-to-the-enterprise-cloud-resource-policy"></a>Kurumsal bulut kaynağı ilkeye AppCompat ekleyin

Visual Studio ağınızdaki Kurumsal verilere erişebileceğiniz belirtmek için aşağıdaki adımları [korumalı uygulamalarınızı nerede bulabilir ve kurumsal veri gönderme tanımlamak için adımları](/windows/security/information-protection/windows-information-protection/create-wip-policy-using-intune-azure#choose-where-apps-can-access-enterprise-data). Windows aracılığıyla bir IP adresi kaynaklarına bağlantılar paylaşacağından durdurmak için eklediğinizden emin olun /\*AppCompat\*/ dizesi ayarı.

## <a name="see-also"></a>Ayrıca bkz.

- [WIP ile uygulama davranışı](/windows/security/information-protection/windows-information-protection/app-behavior-with-wip)