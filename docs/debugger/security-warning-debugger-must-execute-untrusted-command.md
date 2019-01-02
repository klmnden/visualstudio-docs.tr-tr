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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 3e421521bd40ff4369433b0a0c3c323579e36125
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53855622"
---
# <a name="security-warning-debugger-must-execute-untrusted-command"></a>Güvenlik Uyarısı: Hata ayıklayıcı güvenilmeyen komut yürütmeli
Kaynak Sunucusu'nu kullanırken, bu uyarı iletişim kutusu görüntülenir. Bu, hata ayıklayıcı kaynak kodunu edinmek için yürütmek için gereken komut kaynak sunucu srcsvr.ini dosyasının içerdiği için güvenilir komutları listesinde olmadığını gösterir. Bu geçerli bir komutsa, srcsvr.ini dosyasına bunu ekleyebilirsiniz. Aksi takdirde, bunu çalıştırmamanız gerekir. Daha fazla bilgi için [belirtin sembol (.pdb) ve kaynak dosyaları](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md).  
  
## <a name="message-text"></a>İleti metni  
 **Hata ayıklayıcı kaynak kodunu kaynak sunucudan almak için aşağıdaki güvenilmeyen komutu yürütmelidir.**  
  
 **Hata ayıklama sembol dosyası varsa (\*.pdb) olduğunu değil bir bilinen ve güvenilir bir kaynaktan, bu komut geçersiz veya çalıştırılması tehlikeli olabilir.**  
  
 **Bu komutu çalıştırmak istiyor musunuz?**  
  
## <a name="uielement-list"></a>UIElement Listesi  
 Metin kutusu  
 Çalıştırılacak .pdb dosyasından komut.  
  
 Çalıştır  
 Çalıştırmak için komuta izin verin.  
  
 Çalıştırma  
 Komutun yürütülmesini ve kaynak sunucudan dosya indirme durdurun.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sembol (.pdb) belirtin ve kaynak dosyaları](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)   
 [Hata ayıklayıcısı güvenliği](../debugger/debugger-security.md)   
 [Kaynak sunucu](/windows/desktop/Debug/source-server-and-source-indexing)