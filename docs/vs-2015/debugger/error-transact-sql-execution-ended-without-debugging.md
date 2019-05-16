---
title: 'Hata: Transact-SQL yürütmesi hata ayıklama olmadan bitti | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.error.sqlde_sql_executed_but_not_debugged
dev_langs:
- FSharp
- VB
- CSharp
- C++
- SQL
ms.assetid: 7a4d4999-3973-4339-ba6a-f0d19bcb1d4a
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: cdfcaa42c55f87711b0889c6a67d1a4799b84fed
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65681072"
---
# <a name="error-transact-sql-execution-ended-without-debugging"></a>Hata: Transact-SQL yürütmesi hata ayıklaması yapılmadan sonlandı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Hata ayıklayıcı hata ayıklama iletisi, SQL Server'dan almaz ve Transact-SQL veya SQLCLR yordam hata ayıklamaya çalıştığınız bu hata oluşur.  
  
 Bu ağ sorunları nedeniyle veya SQL Server üzerinde sorunları olabilir, ancak en olası nedeni izinlerle ilgili bir sorun.  
  
 Kullanılan iki hesap vardır:  
  
- Kullanıcı hesabı uygulama hesabıdır [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] olarak çalışıyor.  
  
- Bağlantı hesabı SQL Server'a bağlantı kurmak için kullanılan kimliktir. Bu mutlaka bağlantı SQL kimlik doğrulaması kullanıyorsanız gibi Visual Studio çalıştıran kimliğin ile aynı değildir.  
  
  SQL hata ayıklama, uygulama hesabı bağlantı hesapla eşleşmesi gerekir veya sysadmin olmanız gerekir.  
  
  Uygulama hesabı sa gibi bir SQL oturum açma kullanıyorsanız, kurulum SQL Server'da sysadmin olarak olması gerekir. Varsayılan olarak, yöneticiler makine SQL server üzerinde çalıştığı SQL Server Sistem bulunur.  
  
  Bu hatayı düzeltmek için ihtiyacınız olabilecek:  
  
- İzinleri ayarlarınızı doğrulayın. Daha fazla bilgi için [nasıl yapılır: Hata ayıklama için SQL Server izinleri ayarla](https://msdn.microsoft.com/84e088d0-0409-41d4-841b-f5d4b0fda414).  
  
- SQL hata ayıklamayı'ı doğru bir şekilde ayarlandığından emin olun.  
  
- Ağ veya veritabanı yöneticinize başvurun.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [SQL hata ayıklamayı kurma](https://msdn.microsoft.com/3db09e68-edcc-42de-9c22-4e97cfd55ab3)   
 [Nasıl yapılır: Hata ayıklama için SQL Server izinleri ayarlayın](https://msdn.microsoft.com/84e088d0-0409-41d4-841b-f5d4b0fda414)   
 [Hata ayıklayıcı ayarları ve hazırlığı](../debugger/debugger-settings-and-preparation.md)   
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)
