---
title: 'Güvenlik Uyarısı: Hata ayıklayıcı güvenilmeyen komut yürütme gerekir | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.sourceserver.securityalert
dev_langs:
- CSharp
- VB
- FSharp
- C++
ms.assetid: e5c004b3-b364-4098-ac98-770076ca9981
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7c4ab45feeae409a1951e1a57e964eaaa5963896
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62902590"
---
# <a name="security-warning-debugger-must-execute-untrusted-command"></a>Güvenlik Uyarısı: Hata ayıklayıcı güvenilmeyen komut yürütmeli
Kaynak Sunucusu'nu kullanırken, bu uyarı iletişim kutusu görüntülenir. Bu, hata ayıklayıcı kaynak kodunu edinmek için yürütmek için gereken komut kaynak sunucu srcsvr.ini dosyasının içerdiği için güvenilir komutları listesinde olmadığını gösterir. Bu geçerli bir komutsa, srcsvr.ini dosyasına bunu ekleyebilirsiniz. Aksi takdirde, bunu çalıştırmamanız gerekir. Daha fazla bilgi için [belirtin sembol (.pdb) ve kaynak dosyaları](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md).

## <a name="message-text"></a>İleti metni
 **Hata ayıklayıcı kaynak kodunu kaynak sunucudan almak için aşağıdaki güvenilmeyen komutu yürütmelidir.**

 **Hata ayıklama sembol dosyası varsa (\*.pdb) olduğunu değil bir bilinen ve güvenilir bir kaynaktan, bu komut geçersiz veya çalıştırılması tehlikeli olabilir.**

 **Bu komutu çalıştırmak istiyor musunuz?**

## <a name="uielement-list"></a>UIElement Listesi
 Metin kutusunu çalıştırmak için komutu .pdb dosyasından.

 Çalıştırma çalıştırmak için komuta izin verin.

 Komutu Çalıştır Durdur yürütülmesini ve kaynak sunucudan dosya indirme yok.

## <a name="see-also"></a>Ayrıca Bkz.
- [Simge (.pdb) ve Kaynak Dosyaları Belirtme](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)
- [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)
- [Kaynak sunucu](/windows/desktop/Debug/source-server-and-source-indexing)