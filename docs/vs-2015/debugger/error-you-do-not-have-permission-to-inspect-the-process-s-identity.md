---
title: 'Hata: İnceleme işlemi için izniniz yok&#39;s kimlik | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: 6233d060-85b8-42be-ae5f-bde7e1d0f241
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: d66eacb1b7f5205ea430d7154f67d05bdd047a74
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68157516"
---
# <a name="error-you-do-not-have-permission-to-inspect-the-process39s-identity"></a>Hata: İnceleme işlemi için izniniz yok&#39;s kimlik
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İşlem kimliğini İnceleme için izniniz yok. Bu, sisteminizin yapılandırması nedeniyle olabilir.  
  
 Hata ayıklayıcı, hata ayıklama için gereken bilgi işlem kimliğini İnceleme ulaşamadı. En olası nedeni, Terminal Hizmetleri devre dışı bırakılan ' dir. Terminal Hizmetleri varsayılan olarak etkindir. Yeniden etkinleştirmek için aşağıdaki adımları izleyin.  
  
### <a name="to-enable-terminal-services"></a>Terminal Hizmetleri'ni etkinleştirmek için  
  
1. Tıklayın **Başlat** seçip **Denetim Masası**.  
  
2. Denetim Masası'ndaki seçin **Klasik görünümüne geç**, gerekirse ve çift tıklatarak **Yönetimsel Araçlar**.  
  
3. İçinde **Yönetimsel Araçlar** penceresinde çift **Bilgisayar Yönetimi**.  
  
4. Bilgisayar Yönetimi penceresinde **hizmetler ve uygulamalar** düğümü.  
  
5. Altında **hizmetler ve uygulamalar**, tıklayın **Hizmetleri**.  
  
     Hizmetler listesini sağ bölmede görünür.  
  
6. İçinde **Hizmetleri** listesinde, sağ **Terminal Hizmetleri** seçip **özellikleri**.  
  
7. İçinde **Terminal Hizmetleri özellikleri** penceresinde, Git **genel** ayarlayın ve sekme **başlangıç türü** için **el ile**.  
  
8. **Tamam**'ı tıklatın.  
  
9. Bilgisayarı yeniden başlatın.  
  
     Bu yordam, Uzak Masaüstü otomatik olarak etkinleştirmemektedir. Uzak Masaüstü bilgisayarınızda etkinleştirmek istiyorsanız, aşağıdaki ek yordamı gerçekleştirin.  
  
### <a name="to-enable-remote-desktop"></a>Uzak Masaüstü'nü etkinleştirmek için  
  
1. Tıklayın **Başlat** ve ardından sağ tıklayarak **Bilgisayarım**.  
  
2. Seçin **özellikleri**.  
  
     **Sistem Özellikleri** penceresi görüntülenir.  
  
3. Tıklayın **uzak**.  
  
4. Altında **Uzak Masaüstü**seçin **bu bilgisayara uzaktan bağlanmak kullanıcıların**.  
  
5. **Tamam**'ı tıklatın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan Hata Ayıklama Hataları ve Sorun Giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)
