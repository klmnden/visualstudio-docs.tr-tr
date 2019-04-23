---
title: Dia2dump örneği | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- sample applications [DIA SDK]
- Dia2dump sample [DIA SDK]
ms.assetid: 492c0893-7043-452f-a020-890a47230d20
caps.latest.revision: 15
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a817720c1ad73b666e0c9a586bb583120a2533c1
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60092025"
---
# <a name="dia2dump-sample"></a>Dia2dump Örneği
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Dia2dump örneği, Visual Studio ile yüklenir ve Dia2dump.cpp kaynak dosyası içerir. Derlenmiş yürütülebilir dosya, komut satırından çalıştırır ve tüm program veritabanı (.pdb) dosyasının içeriği görüntüler.  
  
### <a name="to-install-the-sample"></a>Örneği yüklemek için  
  
1. Sisteminizin Visual Studio Kurulumu başlangıç sayfasında açıklanan tüm Kurulum gereksinimlerini karşıladığını doğrulayın.  
  
2. Visual Studio yükleyin ve dahil edilen örnekleri tüm Kurulum ve yükleme yönergelerini izleyin.  
  
#### <a name="to-build-the-sample"></a>Örneği oluşturmak için  
  
1. Dia2dump.sln dosyasını Visual Studio'da açın. (Gerekirse, Visual Studio ilk Dia2dump proje yükseltmenize yardımcı olur.)  
  
2. Projenin özellik sayfalarındaki içinde **C/C++** &#124; **genel** &#124; **ek içerik dizinleri** özelliği belirtin `..\DIA SDK\include` dizin. Bu, derleyicinin dia2.h dosya bulabilirsiniz garanti eder.  
  
3. Üzerinde **derleme** menüsünde tıklatın **çözümü yeniden derle**.  
  
4. Visual Studio’yu kapatın.  
  
#### <a name="to-run-the-sample"></a>Örnek çalıştırmak için  
  
1. Bir komut istemi açın ve aşağıdaki komutu yazın:  
  
    ```  
    dia2dump filename  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Dia2dump.cpp kaynak dosyası](../../debugger/debug-interface-access/dia2dump-cpp-source-file.md)   
 [Nasıl yapılır: Başarısız Visual Studio Proje yükseltmelerinde sorun giderme](../../porting/how-to-troubleshoot-unsuccessful-visual-studio-project-upgrades.md)
