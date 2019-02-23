---
title: "Hata: SQL için&#39;bulamıyorsanız SSDEBUGPS'yi | Microsoft Docs"
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.sqlde_cant_find_ssdebugps
dev_langs:
- CSharp
- VB
- FSharp
- C++
- SQL
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 854105ea5d94f6d3b09ce73a23ec45ccab9e797c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56694172"
---
# <a name="error-sql-can39t-find-ssdebugps"></a>Hata: SQL için&#39;SSDEBUGPS'yi bulamıyorum

SSDEBUGPS.dll SQL Server hata ayıklama konağı bileşendir.

Bu hata, hata ayıklamayı başlatmak çalışılırken oluşuyor ve belirtilen dosya mevcut olmadığını gösterir [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] makine. Ya da uzaktan hata ayıklama Kurulumu hiçbir zaman çalıştırıldığı veya şekilde bu dosya silindi, bunun olası nedenler.

Bu hatayı çözmek için iki yolu vardır: Kur'u yeniden uzaktan hata ayıklama ve dosyanın üzerine kopyalayarak [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] makine.

Uzaktan hata ayıklama kurulumu yeniden çalıştırmak için konumundaki yönergeleri [uzaktan hata ayıklama](../debugger/remote-debugging.md).

Bir kopyasını ssdebugps.dll bulabiliyorsa, üzerine kopyalayabilirsiniz [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] makine. Varsa, dosyayı dizin Files\ içinde ortak Files\Microsoft Shared\SQL Debugging olacaktır. Bunu başka bulabilirsiniz [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] makinede veya farklı bir makinede Visual Studio 2005 sahiptir.

SQL Server 2005 makinede SSDEBUGPS.dll kopyalamak için:

1. Üzerinde aynı ad ve yolunu dizine dosya kopyalama [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] makine.

2. Açarak kaydetmek bir **komut istemi**ve aşağıdaki komutu çalıştırın:

    ```cmd
    regsvr32 ssdebugps.dll
    ```
