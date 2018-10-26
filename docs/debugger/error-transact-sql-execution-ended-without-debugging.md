---
title: 'Hata: Transact-SQL yürütmesi hata ayıklama olmadan bitti | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.sqlde_sql_executed_but_not_debugged
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
ms.openlocfilehash: 1bc4de5e9ef0830f69b60d773a59411c4b691454
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49894761"
---
# <a name="error-transact-sql-execution-ended-without-debugging"></a>Hata: Transact-SQL yürütmesi hata ayıklaması yapılmadan sonlandı
Hata ayıklayıcı hata ayıklama iletisi, SQL Server'dan almaz ve Transact-SQL veya SQLCLR yordam hata ayıklamaya çalıştığınız bu hata oluşur.  
  
 Bu ağ sorunları nedeniyle veya SQL Server üzerinde sorunları olabilir, ancak en olası nedeni izinlerle ilgili bir sorun.  
  
 Kullanılan iki hesap vardır:  
  
- Kullanıcı hesabı uygulama hesabıdır [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] olarak çalışıyor.  
  
- Bağlantı hesabı SQL Server'a bağlantı kurmak için kullanılan kimliktir. Bu mutlaka bağlantı SQL kimlik doğrulaması kullanıyorsanız gibi Visual Studio çalıştıran kimliğin ile aynı değildir.  
  
  SQL hata ayıklama, uygulama hesabı bağlantı hesapla eşleşmesi gerekir veya sysadmin olmanız gerekir.  
  
  Uygulama hesabı sa gibi bir SQL oturum açma kullanıyorsanız, kurulum SQL Server'da sysadmin olarak olması gerekir. Varsayılan olarak, yöneticiler makine SQL server üzerinde çalıştığı SQL Server Sistem bulunur.  
  
  Bu hatayı düzeltmek için ihtiyacınız olabilecek:  
  
- İzinleri ayarlarınızı doğrulayın. Daha fazla bilgi için [nasıl yapılır: hata ayıklama için SQL Server izinleri ayarlayın](http://msdn.microsoft.com/en-us/84e088d0-0409-41d4-841b-f5d4b0fda414).  
  
- SQL hata ayıklamayı'ı doğru bir şekilde ayarlandığından emin olun.  
  
- Ağ veya veritabanı yöneticinize başvurun.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [SQL hata ayıklamayı kurma](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/s4sszxst(v=vs.100))   
 [Nasıl yapılır: hata ayıklama için SQL Server izinleri ayarla](http://msdn.microsoft.com/en-us/84e088d0-0409-41d4-841b-f5d4b0fda414)   
 [Hata ayıklayıcı ayarları ve hazırlığı](../debugger/debugger-settings-and-preparation.md)   
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)