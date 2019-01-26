---
title: 'Hata: Makineye bağlanılamıyor &lt;adı&gt;. Makine ağ üzerinde bulunamadı. | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.remote.dcom_disabled
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- DCOM, unable to connect error
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9531151402b5070aaa3a680e09e0082b4e1237f0
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54972046"
---
# <a name="error-unable-to-connect-to-the-machine-ltnamegt-the-machine-cannot-be-found-on-the-network"></a>Hata: Makineye bağlanılamıyor &lt;adı&gt;. Makine ağ üzerinde bulunamadı.
Bu davranış, aşağıdaki koşullardan biri doğru ise oluşur:  
  
-   Uzak bilgisayarla bağlantınız kesildi.  
  
-   Kullanıcı hesabınızın uzak bilgisayarda devre dışıdır.  
  
-   Uzak bilgisayardaki parolanızın süresi doldu.  
  
### <a name="to-resolve-this-behavior"></a>Bu davranışı düzeltmek için  
  
-   Yerel bilgisayarda ve uzak bilgisayar aynı ağda olduğundan emin olun. Bunu yapmak için uzak bilgisayara erişmeye denemek için Microsoft Windows Explorer'ı (veya dosya Gezgini) kullanın.  
  
     — ve —  
  
-   Uzak bilgisayara bağlanmak için kullandığınız kullanıcı hesabının etkin olduğundan emin olun.  
  
     — ve —  
  
-   Uzak bilgisayara bağlanmak için kullandığınız parolayı geçerlidir ve süresi geçmemiş olduğundan emin olun.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan hata ayıklama](../debugger/remote-debugging.md)   
 [Hata Ayıklayıcısı Ayarları ve Hazırlığı](../debugger/debugger-settings-and-preparation.md)