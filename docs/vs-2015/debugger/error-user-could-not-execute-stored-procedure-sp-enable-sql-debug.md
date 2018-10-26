---
title: 'Hata: Kullanıcı verebilir saklı yordamını sp_enable_sql_debug | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.error.sqlde_accessdenied
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: 11957495-c238-4cc5-8937-e4026f5e10e1
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 561bc9b96ff12309ae9bc9ba7ea58cef16074361
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49922243"
---
# <a name="error-user-could-not-execute-stored-procedure-spenablesqldebug"></a>Hata: Kullanıcı sp_enable_sql_debug Saklı Yordamını Yürütemedi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Sp_enable_sql_debug saklı yordamını yürütemedi sunucu üzerinde yürütülemedi. Bu neden olabilir:  
  
- Bir bağlantı sorunu. Kararlı bir sunucu bağlantısı olması gerekir.  
  
- Sunucuda gerekli izinleri yetersiz. SQL Server 2005'te hata ayıklamak için Visual Studio çalıştıran hesabı hem de SQL Server'a bağlanmak için kullanılan hesap sysadmin rolünün üyesi olması gerekir. (SQL kimlik doğrulaması kullanıyorsanız) SQL Server'a bağlanmak için kullanılan hesap veya (Windows kimlik doğrulaması kullanıyorsanız), Windows kullanıcı hesabı, hem de kullanıcı kimliği ve parolası olan bir hesap değil.  
  
  Daha fazla bilgi için [nasıl yapılır: hata ayıklama için SQL Server izinleri ayarlayın](http://msdn.microsoft.com/en-us/84e088d0-0409-41d4-841b-f5d4b0fda414).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: hata ayıklama için SQL Server izinleri ayarla](http://msdn.microsoft.com/en-us/84e088d0-0409-41d4-841b-f5d4b0fda414)   
 [SQL hata ayıklamayı kurma](http://msdn.microsoft.com/en-us/3db09e68-edcc-42de-9c22-4e97cfd55ab3)



