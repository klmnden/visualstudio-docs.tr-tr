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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0f44c429dad42a0a46fe2c00f9b6a82dfcdb92b8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62929774"
---
# <a name="security-warning-attaching-to-a-process-owned-by-an-untrusted-user-can-be-dangerous-if-the-following-information-looks-suspicious-or-you-are-unsure-do-not-attach-to-this-process"></a>Güvenlik Uyarısı: Güvenilmeyen bir kullanıcının sahip olduğu işleme ekleme tehlikeli olabilir. Aşağıdaki bilgiler kuşkulu görünüyorsa ya da emin değilseniz, bu işleme eklemeyin
Kısmen güvenilen kodu içerir veya hemen bağlama gerçekleşmeden önce güvenilmeyen bir kullanıcının sahip olduğu bir işleme eklediğinizde, bu uyarı iletişim kutusu görüntülenir. Kötü amaçlı kod içeren bir güvenilmeyen işlemi hata ayıklamada bilgisayar zarar verme olasılığı vardır. İşlem güvenmeyecekleri nedeniniz sonra tıklatmanız gerekir **iptal** hata ayıklama önlemek için.

 Yasal bir senaryo hata ayıklama sırasında bu uyarının gösterilmemesi için Visual Studio'yu kapatın ve bu kayıt defteri anahtarı değerini 1 olarak ayarlayın: `HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\<version>\Debugger\DisableAttachSecurityWarning`ve sonra Visual Studio'yu yeniden başlatın. Hata ayıklama senaryoyu tamamladıktan sonra değerini 0 olarak ayarlamak ve Visual Studio'yu yeniden başlatın.

 "Kullanıcıların güvenilen" dahil kendiniz artı genellikle .NET Framework gibi yüklü olan bilgisayarlarda tanımlanan standart kullanıcı kümesini `aspnet`, `localsystem`, `networkservice`, ve `localservice`.

## <a name="uielement-list"></a>UIElement Listesi
 Hata ayıklamak için istenen derleme adı

 Geçerli kullanıcı

 Ekleyerek hatalarını ayıklamaya devam etmek için ENTER tuşuna ekleme

 Ekleme yapmak işleme yoksa değil mi

## <a name="see-also"></a>Ayrıca Bkz.
- [Çalıştırma İşlemine İliştirme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md)
- [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)