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
ms.openlocfilehash: bd52c635d5ade1bef73176601d6957ba5859723b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54791163"
---
# <a name="dia2dump-sample"></a>Dia2dump Örneği
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Dia2dump örneği, Visual Studio ile yüklenir ve Dia2dump.cpp kaynak dosyası içerir. Derlenmiş yürütülebilir dosya, komut satırından çalıştırır ve tüm program veritabanı (.pdb) dosyasının içeriği görüntüler.  
  
### <a name="to-install-the-sample"></a>Örneği yüklemek için  
  
1.  Sisteminizin Visual Studio Kurulumu başlangıç sayfasında açıklanan tüm Kurulum gereksinimlerini karşıladığını doğrulayın.  
  
2.  Visual Studio yükleyin ve dahil edilen örnekleri tüm Kurulum ve yükleme yönergelerini izleyin.  
  
#### <a name="to-build-the-sample"></a>Örneği oluşturmak için  
  
1.  Dia2dump.sln dosyasını Visual Studio'da açın. (Gerekirse, Visual Studio ilk Dia2dump proje yükseltmenize yardımcı olur.)  
  
2.  Projenin özellik sayfalarındaki içinde **C/C++** &#124; **genel** &#124; **ek içerik dizinleri** özelliği belirtin `..\DIA SDK\include` dizin. Bu, derleyicinin dia2.h dosya bulabilirsiniz garanti eder.  
  
3.  Üzerinde **derleme** menüsünde tıklatın **çözümü yeniden derle**.  
  
4.  Visual Studio’yu kapatın.  
  
#### <a name="to-run-the-sample"></a>Örnek çalıştırmak için  
  
1.  Bir komut istemi açın ve aşağıdaki komutu yazın:  
  
    ```  
    dia2dump filename  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Dia2dump.cpp kaynak dosyası](../../debugger/debug-interface-access/dia2dump-cpp-source-file.md)   
 [Nasıl yapılır: Başarısız Visual Studio Proje yükseltmelerinde sorun giderme](../../porting/how-to-troubleshoot-unsuccessful-visual-studio-project-upgrades.md)
