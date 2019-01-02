---
title: 'Hata: Kullanıcı verebilir saklı yordamını sp_enable_sql_debug | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
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
ms.openlocfilehash: 9c80a4055b899f155b4be8e7832df9f3aa22db20
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53903584"
---
# <a name="error-user-could-not-execute-stored-procedure-spenablesqldebug"></a>Hata: Kullanıcı olabilir değil yürütme sp_enable_sql_debug saklı yordamını yürütemedi

Sp_enable_sql_debug saklı yordamını yürütemedi sunucu üzerinde yürütülemedi. Bu neden olabilir:

- Bir bağlantı sorunu. Kararlı bir sunucu bağlantısı olması gerekir.

- Sunucuda gerekli izinleri yetersiz. SQL Server 2005'te hata ayıklamak için Visual Studio çalıştıran hesabı hem de SQL Server'a bağlanmak için kullanılan hesap sysadmin rolünün üyesi olması gerekir. (SQL kimlik doğrulaması kullanıyorsanız) SQL Server'a bağlanmak için kullanılan hesap veya (Windows kimlik doğrulaması kullanıyorsanız), Windows kullanıcı hesabı, hem de kullanıcı kimliği ve parolası olan bir hesap değil.

Daha fazla bilgi için [nasıl yapılır: Hata ayıklama için SQL Server izinleri ayarla](https://msdn.microsoft.com/84e088d0-0409-41d4-841b-f5d4b0fda414).

## <a name="see-also"></a>Ayrıca Bkz.

- [Nasıl yapılır: Hata ayıklama için SQL Server izinleri ayarlayın](https://msdn.microsoft.com/84e088d0-0409-41d4-841b-f5d4b0fda414)
- [SQL hata ayıklamayı kurma](/previous-versions/visualstudio/visual-studio-2010/s4sszxst\(v\=vs.100\))