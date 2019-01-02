---
title: 'Güvenlik Uyarısı: Güvenilmeyen bir kullanıcının sahip olduğu işleme ekleme tehlikeli olabilir. Aşağıdaki bilgiler kuşkulu görünüyorsa ya da emin değilseniz, bu işleme eklemeyin. | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.attachsecuritywarning
dev_langs:
- CSharp
- VB
- FSharp
- C++
ms.assetid: 52246c1e-a371-40a0-b756-a435cc51876f
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 22f7ecafbbf9c3d43c49d253bba482e0f2ff0941
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53821428"
---
# <a name="security-warning-attaching-to-a-process-owned-by-an-untrusted-user-can-be-dangerous-if-the-following-information-looks-suspicious-or-you-are-unsure-do-not-attach-to-this-process"></a>Güvenlik Uyarısı: Güvenilmeyen bir kullanıcının sahip olduğu işleme ekleme tehlikeli olabilir. Aşağıdaki bilgiler kuşkulu görünüyorsa ya da emin değilseniz, bu işleme eklemeyin
Kısmen güvenilen kodu içerir veya hemen bağlama gerçekleşmeden önce güvenilmeyen bir kullanıcının sahip olduğu bir işleme eklediğinizde, bu uyarı iletişim kutusu görüntülenir. Kötü amaçlı kod içeren bir güvenilmeyen işlemi hata ayıklamada bilgisayar zarar verme olasılığı vardır. İşlem güvenmeyecekleri nedeniniz sonra tıklatmanız gerekir **iptal** hata ayıklama önlemek için.  
  
 Yasal bir senaryo hata ayıklama sırasında bu uyarının gösterilmemesi için Visual Studio'yu kapatın ve bu kayıt defteri anahtarı değerini 1 olarak ayarlayın: `HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\<version>\Debugger\DisableAttachSecurityWarning`ve sonra Visual Studio'yu yeniden başlatın. Hata ayıklama senaryoyu tamamladıktan sonra değerini 0 olarak ayarlamak ve Visual Studio'yu yeniden başlatın.  
  
 "Kullanıcıların güvenilen" dahil kendiniz artı genellikle .NET Framework gibi yüklü olan bilgisayarlarda tanımlanan standart kullanıcı kümesini `aspnet`, `localsystem`, `networkservice`, ve `localservice`.  
  
## <a name="uielement-list"></a>UIElement Listesi  
 Ad  
 Hata ayıklamak için istenen derlemenin adı  
  
 Kullanıcı  
 Geçerli kullanıcı  
  
 İliştir  
 Ekleyerek hatalarını ayıklamaya devam etmek için basın  
  
 İliştirme  
 İşleme eklemeyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çalıştırma işlemleri iliştirme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md)   
 [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)