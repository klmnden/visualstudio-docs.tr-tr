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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 038b448c0ecd0b19afd7671a381eb68c9ba8cbbe
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53854119"
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
    regsrv32 ssdebugps.dll
    ```
