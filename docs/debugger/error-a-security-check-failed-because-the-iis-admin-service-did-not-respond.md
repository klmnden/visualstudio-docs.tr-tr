---
title: 'Hata: IIS Yönetici Hizmeti yanıt vermediğinden güvenlik denetimi başarısız oldu | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.iis_not_responding
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8ae97ae0594b06e9b35ac3bdd61eacf852968889
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62851027"
---
# <a name="error-a-security-check-failed-because-the-iis-admin-service-did-not-respond"></a>Hata: IIS Yönetici Hizmeti yanıt vermediğinden güvenlik denetimi başarısız oldu.
IIS Yönetici Hizmeti yanıt vermiyor, bu hata oluşur. Bu, genellikle IIS yükleme ile ilgili bir sorun olduğunu gösterir. İlk olarak kullanarak hizmetinin çalıştığını doğrulayın. **Hizmetleri** gelen aracı **Yönetimsel Araçlar**.

### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

- IIS kullanarak yeniden **Program Ekle veya Kaldır** Denetim Masası.

- -veya-

- Program Ekle veya Kaldır Denetim Masası'nı kullanarak makinenizden IIS kaldırın. IIS kaldırmış ve hala sorunlarla, kayıt defterini denetleyin ve bu anahtar artık mevcut olduğundan emin olun:

    `HKEY_CLASSES_ROOT\CLSID\{A9E69610-B80D-11D0-B9B9-00A0C922E750}`

     -veya-

- Yönetimsel Araçlar Denetim Masası'nı kullanarak IIS Yönetici Hizmeti devre dışı bırakın. Bu IIS makinenizde devre dışı bırakır.

     Bu üç adımlardan herhangi biri gerçekleştirildikten sonra bilgisayarınızı yeniden başlatın.

     Ek bilgi için IIS belgelerine bakın.

## <a name="see-also"></a>Ayrıca Bkz.
- [Web Uygulamalarında Hata Ayıklama: Hatalar ve Sorun Giderme](../debugger/debugging-web-applications-errors-and-troubleshooting.md)