---
title: İşleme iliştirilemiyor. | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.debug.remote.unable2attach
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: affcff981ee516810f2ed9f6c2337c5145ebc572
ms.sourcegitcommit: 5a65ca6688a2ebb36564657d2d73c4b4f2d15c34
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "53819581"
---
# <a name="unable-to-attach-to-the-process"></a>İşleme İliştirilemiyor
İşleme iliştirilemiyor. Hata ayıklayıcı bileşeni sunucuda bu makineye bağlanırken erişim aldı.  
  
 Bu hataya neden iki yaygın senaryo vardır:  
  
 **Senaryo 1:** Makine Windows XP çalışıyor. Windows Server 2003 çalıştıran makine B. Makine B üzerinde kayıt defterini, aşağıdaki DWORD değerini içerir:  
  
 `HKLM\Software\Microsoft\MachineDebugManager\AllowLaunchAsOtherUser=1`  
  
 1 kullanıcı Terminal Server oturumunu (oturumu 1) makinede B ve yönetilen bir uygulama bu oturumdan başlayan.  
  
 Her iki makinede yönetici de olan, kullanıcı 2, makine A. kaydediliyor Burada, makine b 1 oturumda çalışan bir uygulamaya eklemek izinli çalışır  
  
 **Senaryo 2:** Bir kullanıcı her iki makinelerde aynı parola kullanarak makinelere iki, A ve B aynı çalışma kaydedilir. Hata ayıklayıcı bir makine üzerinde çalışan ve makine b makine A üzerinde çalışan yönetilen bir uygulamaya iliştirmeye **ağ erişimi: Yerel hesaplar için paylaşım ve güvenlik modeli** kümesine **Konuk**.  
  
### <a name="to-solve-scenario-1"></a>Senaryo 1 çözmek için  
  
-   Hata ayıklayıcı ve yönetilen uygulama aynı kullanıcı hesabı adı ve parola altında çalıştırın.  
  
### <a name="to-solve-scenario-2"></a>Senaryo 2 çözmek için  
  
1.  Gelen **Başlat** menüsünde seçin **Denetim Masası**.  
  
2.  Denetim Masası'ndaki çift **Yönetimsel Araçlar**.  
  
3.  Yönetimsel Araçlar penceresinde, **yerel güvenlik ilkesi**.  
  
4.  Yerel Güvenlik İlkesi penceresinde **yerel ilkeler**.  
  
5.  İçinde **ilkeleri** sütunu, çift **ağ erişimi: Yerel hesaplar için paylaşım ve güvenlik modeli**.  
  
6.  İçinde **ağ erişimi: Yerel hesaplar için paylaşım ve güvenlik modeli** iletişim kutusunda, yerel güvenlik ayarını **Klasik**, tıklatıp **Tamam**.  
  
    > [!CAUTION]
    >  Güvenlik modeli Klasik olarak değiştirilmesi beklenmeyen Access'te paylaşılan dosyaları ve DCOM bileşenleri için neden olabilir. Bu değişiklik yaparsanız, uzak bir kullanıcı, yerel kullanıcı hesabı yerine ile Konuk kimlik doğrulaması yapabilir. Uzak bir kullanıcı, kullanıcı adınızı ve parolanızı eşleşiyorsa, bu kullanıcı herhangi bir klasör veya DCOM nesne dışarı paylaştığı erişebilir olacaktır. Bu güvenlik modeli kullandığınız makinedeki tüm kullanıcı hesaplarını güçlü parolalar veya hata ayıklama için bir yalıtılmış ağ Adası ayarlama ve yetkisiz erişimi önlemek için makineleri hata ayıklaması emin olun.  
  
7.  Tüm pencereleri kapatın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklayıcısı Ayarları ve Hazırlığı](../debugger/debugger-settings-and-preparation.md)