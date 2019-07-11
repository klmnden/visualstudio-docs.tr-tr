---
title: Visual Studio abonesi veri anonimleştirme | Microsoft Docs
author: evanwindom
ms.author: lank
manager: lank
ms.date: 10/31/2018
ms.topic: conceptual
description: Aboneliklere erişimi kesildiğinde nasıl abone veriler anonimleştirilmiştir öğrenin.
ms.openlocfilehash: 1d4e4c5f2e1946a75a70ab4ddb49f000c951cd97
ms.sourcegitcommit: 208395bc122f8d3dae3f5e5960c42981cc368310
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/10/2019
ms.locfileid: "67783664"
---
# <a name="anonymization-of-visual-studio-subscriber-information"></a>Visual Studio abonesi bilgilerin anonimleştirme

Bir abonenin aboneliği süre sonu veya bir abonenin oturum açma hesabı silme gibi bir abonelik kullanımını engelleyen bir olay oluştuğunda kullanıcının adını ve oturum açma hesabı gibi kişisel bilgileri temelde karıştırılmış işlemek için bunları kullanılamaz.  Bu, abonenin kişisel bilgileri korumak için gerçekleştirilir.

[!INCLUDE [GDPR-related guidance](includes/gdpr-intro-sentence.md)]

## <a name="when-does-anonymization-occur"></a>Anonimleştirme ne zaman gerçekleşiyor?

Bir abonenin aboneliği kullanılamaz hale gelmesine neden olayların anonimleştirme tetikler.  Anonimleştirme nasıl hızlı bir şekilde gerçekleşir, abonelik ve olay türüne göre değişir. Daha fazla bilgi için aşağıdaki tabloya bakın.

| Abonelik türü                                                                                                                       | Anonimleştirme tetikleyen olayı                                                                                                     | Anonimleştirme gerçekleştiğinde |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------|
| Visual Studio Dev Essentials                                                                                                            | Abone programdan kabul eder ya da kullanım koşullarını kabul etmiyorum                                    | 30 gün               |
| Visual Studio abonelikleri Microsoft Store (Perakende) satın                                                                      | Abonelik süresi dolana veya sözleşme etkinleştirilmemiş                                                                   | 360 gün                  |
| Toplu Lisans, Visual Studio Marketi (bulut abonelikleri) veya MPN gibi programları aracılığıyla edinilen visual Studio abonelikleri | Abonelik süresi dolana veya bir kullanıcıya atanmadı                                                          | 180 gün                  |
| Tüm abonelikler                                                                                                                       | Bir Azure Active Directory hesabı veya Microsoft hesabı (MSA) aboneliğe imzalamak için kullanılan kapalı | Hemen               |
| Tüm abonelikler                                                                                                                       | Azure Active Directory hesabı ile ilişkili Kiracı abone kaldırılır                                | Hemen               |

## <a name="faq"></a>SSS

### <a name="q--does-the-anonymization-of-the-subscribers-personal-information-cause-them-to-lose-access-to-the-subscription"></a>S:  Abonenin kişisel bilgilerin anonimleştirme bunları aboneliğe erişimi kaybetmenize neden?
Y:  Hayır.  Anonimleştirme aboneliğe erişim kaybına neden olur, ancak erişim eksiği neden olmayan bir olaya yanıt olarak kullanılıyor.

### <a name="q--im-an-administrator-for-my-organizations-subscriptions--if-one-of-my-subscribers-information-is-anonymized-can-that-subscription-be-reassigned-to-another-user"></a>S:  Kuruluşumun abonelikler için bir yönetici ortağıyım.  My abonenin bilgi birini anonim hale getirilen, bu abonelik başka bir kullanıcıya atanabilir?
Y:  Evet – abonelik süresi geçmemiş sürece, başka bir aboneye atanabilir.

## <a name="next-steps"></a>Sonraki adımlar

Anonimleştirme tarafından önlemek öğrenin [MSA ve AAD kimlikleri bağlama](/azure/active-directory/b2b/add-users-administrator).
