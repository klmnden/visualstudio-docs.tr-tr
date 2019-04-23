---
title: 'Hata: İnceleme işlemi için izniniz yok&#39;s kimlik | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 437693b289723c44986f61cc65d644742cd8e77c
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60102139"
---
# <a name="error-you-do-not-have-permission-to-inspect-the-process39s-identity"></a>Hata: İnceleme işlemi için izniniz yok&#39;s kimlik
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
- [Uzaktan Hata Ayıklama Hataları ve Sorun Giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)