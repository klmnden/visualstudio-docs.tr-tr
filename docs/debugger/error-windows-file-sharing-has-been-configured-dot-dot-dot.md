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
ms.openlocfilehash: 257d7a0ce597cc8cbbadca975ee3db60d4e3adcc
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54951852"
---
# <a name="error-windows-file-sharing-has-been-configured"></a>Hata: Windows dosya paylaşımı yapılandırıldı...
Böylece farklı bir kullanıcı adı kullanarak uzak bilgisayara bağlanacak Windows dosya paylaşımı yapılandırıldı. Bu uzaktan hata ayıklama ile uyumlu değil  
  
 Geçerli dosya yapılandırma paylaşımı farklı bir kullanıcı adı kullanarak uzak bilgisayara bağlanmak için ayarlanır. Uzaktan hata ayıklama, bu senaryoda mümkün değildir.  
  
 Bu hatayı düzeltmek için bir hesap adı kullanarak bilgisayarda oturum açın veya altında hata ayıklama hesap adı kullanacak şekilde dosya paylaşımı değiştirin.  
  
 Bu kullanıcı adıyla uzak bilgisayara bağlanmak isterseniz, uzak bilgisayardan bağlantısını kesmeniz gerekir.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1.  Bir hesap adı kullanarak, ayıkladığınız makine gibi yerel, makinede oturum açın.  
  
     —veya—  
  
     biçimindeki telefon numarasıdır. Uzak bilgisayar bağlantısını kesebilmeniz ve diğer makine hesap adınızı kullanarak bağlanmak için dosya paylaşımını yeniden yapılandırın:  
  
    1.  Üzerinde **Başlat** menüsünde **Donatılar**ve ardından **komut istemi**.  
  
    2.  Windows komut isteminde aşağıdakini yazın:  
  
         `net use /delete computer_name`  
  
    3.  Windows Yardım'da belirtildiği yöntemlerden birini kullanarak dosya paylaşım ayarlarınızı değiştirin.