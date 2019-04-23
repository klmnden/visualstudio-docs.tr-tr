---
title: Bağlantı dizesi şifresiz parola içeren kimlik bilgileri içeriyor ve tümleşik güvenlik kullanmıyor | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
ms.assetid: 501d85af-92e0-4471-b280-8a59c0688575
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 0538620cde170ea9ae033a510c7fa01ff20c64d3
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60093156"
---
# <a name="the-connection-string-contains-credentials-with-a-clear-text-password-and-is-not-using-integrated-security"></a>Bağlantı dizesi şifresiz parola içeren kimlik bilgileri içeriyor ve tümleşik güvenliği kullanmıyor
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bağlantı dizesini geçerli DBML dosyasının ve uygulama yapılandırma dosyaları ile bu hassas bilgileri kaydetmek istiyor musunuz?  Bağlantı dizesini hassas bilgiler olmadan kaydetmek için Hayır'a tıklayın.  
  
 Hassas bilgileri (bağlantı dizesine dahil parolalar) dahil veri bağlantıları ile çalışırken, bir projenin DBML dosyasının ve uygulama yapılandırma dosyası ile veya olmadan bağlantı dizesini kaydetme seçeneği sunulur. hassas bilgileri.  
  
> [!WARNING]
>  Açık olarak ayarlama **bağlantı** özellikleri **uygulama ayarları** özelliğini **False** DBML dosyasına parola ekleyeceksiniz.  
  
### <a name="to-save-the-connection-string-with-the-sensitive-information-in-the-projects-application-settings"></a>Hassas bilgileri projenin uygulama ayarlarında bağlantı dizesini kaydetmek için  
  
- **Evet**'i tıklayın.  
  
     Bağlantı dizesi, bir uygulama ayarı olarak depolanır. Bağlantı dizesi düz metin olarak hassas bilgiler içerir. DBML dosyasının, hassas bilgileri içermiyor.  
  
### <a name="to-save-the-connection-string-without-the-sensitive-information-in-the-projects-application-settings"></a>Projenin uygulama ayarlarında bağlantı dizesini hassas bilgiler olmadan kaydetmek için  
  
- **Hayır**'a tıklayın.  
  
     Bağlantı dizesi, bir uygulama ayarı olarak depolanır, ancak parola dahil değildir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio'daki LINQ to SQL Araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
