---
title: 'Hata: Windows dosya paylaşımı yapılandırıldı... | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.remote_credentials_prohibited
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
ms.openlocfilehash: 89224dc5394f248ea82d428731ef387cb705ff27
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62850054"
---
# <a name="error-windows-file-sharing-has-been-configured"></a>Hata: Windows dosya paylaşımı yapılandırıldı...
Böylece farklı bir kullanıcı adı kullanarak uzak bilgisayara bağlanacak Windows dosya paylaşımı yapılandırıldı. Bu uzaktan hata ayıklama ile uyumlu değil

 Geçerli dosya yapılandırma paylaşımı farklı bir kullanıcı adı kullanarak uzak bilgisayara bağlanmak için ayarlanır. Uzaktan hata ayıklama, bu senaryoda mümkün değildir.

 Bu hatayı düzeltmek için bir hesap adı kullanarak bilgisayarda oturum açın veya altında hata ayıklama hesap adı kullanacak şekilde dosya paylaşımı değiştirin.

 Bu kullanıcı adıyla uzak bilgisayara bağlanmak isterseniz, uzak bilgisayardan bağlantısını kesmeniz gerekir.

### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

1. Bir hesap adı kullanarak, ayıkladığınız makine gibi yerel, makinede oturum açın.

     —veya—

     biçimindeki telefon numarasıdır. Uzak bilgisayar bağlantısını kesebilmeniz ve diğer makine hesap adınızı kullanarak bağlanmak için dosya paylaşımını yeniden yapılandırın:

    1. Üzerinde **Başlat** menüsünde **Donatılar**ve ardından **komut istemi**.

    2. Windows komut isteminde aşağıdakini yazın:

         `net use /delete computer_name`

    3. Windows Yardım'da belirtildiği yöntemlerden birini kullanarak dosya paylaşım ayarlarınızı değiştirin.