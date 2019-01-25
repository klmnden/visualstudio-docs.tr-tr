---
title: 'Hata: Kullanıcı verebilir saklı yordamını sp_enable_sql_debug | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.error.sqlde_accessdenied
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: 11957495-c238-4cc5-8937-e4026f5e10e1
caps.latest.revision: 9
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 1f463aca03cd0e869f4028f8e086c623295fd2f6
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54799400"
---
# <a name="error-user-could-not-execute-stored-procedure-spenablesqldebug"></a>Hata: Kullanıcı olabilir değil yürütme sp_enable_sql_debug saklı yordamını yürütemedi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Sp_enable_sql_debug saklı yordamını yürütemedi sunucu üzerinde yürütülemedi. Bu neden olabilir:  
  
- Bir bağlantı sorunu. Kararlı bir sunucu bağlantısı olması gerekir.  
  
- Sunucuda gerekli izinleri yetersiz. SQL Server 2005'te hata ayıklamak için Visual Studio çalıştıran hesabı hem de SQL Server'a bağlanmak için kullanılan hesap sysadmin rolünün üyesi olması gerekir. (SQL kimlik doğrulaması kullanıyorsanız) SQL Server'a bağlanmak için kullanılan hesap veya (Windows kimlik doğrulaması kullanıyorsanız), Windows kullanıcı hesabı, hem de kullanıcı kimliği ve parolası olan bir hesap değil.  
  
  Daha fazla bilgi için [nasıl yapılır: Hata ayıklama için SQL Server izinleri ayarla](http://msdn.microsoft.com/84e088d0-0409-41d4-841b-f5d4b0fda414).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Hata ayıklama için SQL Server izinleri ayarlayın](http://msdn.microsoft.com/84e088d0-0409-41d4-841b-f5d4b0fda414)   
 [SQL hata ayıklamayı kurma](http://msdn.microsoft.com/3db09e68-edcc-42de-9c22-4e97cfd55ab3)
