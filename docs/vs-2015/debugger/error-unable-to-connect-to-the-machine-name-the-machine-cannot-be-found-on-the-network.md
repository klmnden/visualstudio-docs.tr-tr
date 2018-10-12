---
title: 'Hata: Makineye bağlanılamıyor &lt;adı&gt;. Makine ağ üzerinde bulunamadı. | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.remote.dcom_disabled
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- DCOM, unable to connect error
ms.assetid: b584b5db-ef52-45ed-8561-1314da3cc5b8
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d4e2c60723827466942ea02b8881f234e38fa438
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49223087"
---
# <a name="error-unable-to-connect-to-the-machine-ltnamegt-the-machine-cannot-be-found-on-the-network"></a>Hata: Makineye bağlanılamıyor &lt;adı&gt;. Makine ağ üzerinde bulunamadı.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

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
 [Cihazda uzak araçları ayarlama](http://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c)   
 [Hata Ayıklayıcısı Ayarları ve Hazırlığı](../debugger/debugger-settings-and-preparation.md)



