---
title: "Hata: SQL için&#39;bulamıyorsanız SSDEBUGPS'yi | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.error.sqlde_cant_find_ssdebugps
dev_langs:
- FSharp
- VB
- CSharp
- C++
- SQL
ms.assetid: 596425c8-14c7-4c05-8823-e1c52f420f5e
caps.latest.revision: 9
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 25462a99bd3e773f03af3918a9e25d11ed006c1c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68185201"
---
# <a name="error-sql-can39t-find-ssdebugps"></a>Hata: SQL için&#39;SSDEBUGPS'yi bulamıyorum
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

SSDEBUGPS.dll SQL Server hata ayıklama konağı bileşendir.  
  
 Bu hata, hata ayıklamayı başlatmak çalışılırken oluşuyor ve belirtilen dosya mevcut olmadığını gösterir [!INCLUDE[sqprsqlong](../includes/sqprsqlong-md.md)] makine. Ya da uzaktan hata ayıklama Kurulumu hiçbir zaman çalıştırıldığı veya şekilde bu dosya silindi, bunun olası nedenler.  
  
 Bu hatayı çözmek için iki yolu vardır: Kur'u yeniden uzaktan hata ayıklama ve dosyanın üzerine kopyalayarak [!INCLUDE[sqprsqlong](../includes/sqprsqlong-md.md)] makine.  
  
 Uzaktan hata ayıklama kurulumu yeniden çalıştırmak için konumundaki yönergeleri [uzaktan hata ayıklama](../debugger/remote-debugging.md).  
  
 Bir kopyasını ssdebugps.dll bulabiliyorsa, üzerine kopyalayabilirsiniz [!INCLUDE[sqprsqlong](../includes/sqprsqlong-md.md)] makine. Varsa, dosyayı dizin Files\ içinde ortak Files\Microsoft Shared\SQL Debugging olacaktır. Bunu başka bulabilirsiniz [!INCLUDE[sqprsqlong](../includes/sqprsqlong-md.md)] makinede veya farklı olan bir makinede [!INCLUDE[vsprvslong](../includes/vsprvslong-md.md)] yüklü.  
  
### <a name="to-copy-ssdebugpsdll-onto-the-sql-server-2005-machine"></a>SQL Server 2005 makinede SSDEBUGPS.dll kopyalamak için  
  
1. Üzerinde aynı ad ve yolunu dizine dosya kopyalama [!INCLUDE[sqprsqlong](../includes/sqprsqlong-md.md)] makine.  
  
2. Açarak kaydetmek bir **komut istemi**ve aşağıdaki komutu çalıştırın:  
  
    ```  
    regsvr32 ssdebugps.dll  
    ```
