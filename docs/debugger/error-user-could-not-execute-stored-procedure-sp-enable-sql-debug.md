---
title: 'Hata: Kullanıcı verebilir saklı yordamını sp_enable_sql_debug | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.sqlde_accessdenied
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 795dcb07459318326085d5e1fe99554d9c8d1311
ms.sourcegitcommit: bc43970c000f07c9cc2051f1264a9742943a9755
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/09/2018
ms.locfileid: "51349510"
---
# <a name="error-user-could-not-execute-stored-procedure-spenablesqldebug"></a>Hata: Kullanıcı sp_enable_sql_debug Saklı Yordamını Yürütemedi
Sp_enable_sql_debug saklı yordamını yürütemedi sunucu üzerinde yürütülemedi. Bu neden olabilir:  
  
- Bir bağlantı sorunu. Kararlı bir sunucu bağlantısı olması gerekir.  
  
- Sunucuda gerekli izinleri yetersiz. SQL Server 2005'te hata ayıklamak için Visual Studio çalıştıran hesabı hem de SQL Server'a bağlanmak için kullanılan hesap sysadmin rolünün üyesi olması gerekir. (SQL kimlik doğrulaması kullanıyorsanız) SQL Server'a bağlanmak için kullanılan hesap veya (Windows kimlik doğrulaması kullanıyorsanız), Windows kullanıcı hesabı, hem de kullanıcı kimliği ve parolası olan bir hesap değil.  
  
  Daha fazla bilgi için [nasıl yapılır: hata ayıklama için SQL Server izinleri ayarlayın](https://msdn.microsoft.com/84e088d0-0409-41d4-841b-f5d4b0fda414).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: hata ayıklama için SQL Server izinleri ayarla](https://msdn.microsoft.com/84e088d0-0409-41d4-841b-f5d4b0fda414)   
 [SQL hata ayıklamayı kurma](/previous-versions/visualstudio/visual-studio-2010/s4sszxst\(v\=vs.100\))