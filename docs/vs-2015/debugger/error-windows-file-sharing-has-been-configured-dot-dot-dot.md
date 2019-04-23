---
title: 'Hata: Windows dosya paylaşımı yapılandırıldı... | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.error.remote_credentials_prohibited
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: c45a1b74-61ec-4c64-9e2c-13051a4f50a5
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 96d65ae615522bcee43ddf5e8181e96eecc0d958
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60040863"
---
# <a name="error-windows-file-sharing-has-been-configured"></a>Hata: Windows dosya paylaşımı yapılandırıldı...
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

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
