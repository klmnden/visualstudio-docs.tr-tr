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
ms.openlocfilehash: 02805bc9951c682c654b47ae49c15c7682bd60ee
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54764624"
---
# <a name="the-connection-string-contains-credentials-with-a-clear-text-password-and-is-not-using-integrated-security"></a>Bağlantı dizesi şifresiz parola içeren kimlik bilgileri içeriyor ve tümleşik güvenliği kullanmıyor
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Bağlantı dizesini geçerli DBML dosyasının ve uygulama yapılandırma dosyaları ile bu hassas bilgileri kaydetmek istiyor musunuz?  Bağlantı dizesini hassas bilgiler olmadan kaydetmek için Hayır'a tıklayın.  
  
 Hassas bilgileri (bağlantı dizesine dahil parolalar) dahil veri bağlantıları ile çalışırken, bir projenin DBML dosyasının ve uygulama yapılandırma dosyası ile veya olmadan bağlantı dizesini kaydetme seçeneği sunulur. hassas bilgileri.  
  
> [!WARNING]
>  Açık olarak ayarlama **bağlantı** özellikleri **uygulama ayarları** özelliğini **False** DBML dosyasına parola ekleyeceksiniz.  
  
### <a name="to-save-the-connection-string-with-the-sensitive-information-in-the-projects-application-settings"></a>Hassas bilgileri projenin uygulama ayarlarında bağlantı dizesini kaydetmek için  
  
-   **Evet**'i tıklayın.  
  
     Bağlantı dizesi, bir uygulama ayarı olarak depolanır. Bağlantı dizesi düz metin olarak hassas bilgiler içerir. DBML dosyasının, hassas bilgileri içermiyor.  
  
### <a name="to-save-the-connection-string-without-the-sensitive-information-in-the-projects-application-settings"></a>Projenin uygulama ayarlarında bağlantı dizesini hassas bilgiler olmadan kaydetmek için  
  
-   **Hayır**'a tıklayın.  
  
     Bağlantı dizesi, bir uygulama ayarı olarak depolanır, ancak parola dahil değildir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio'daki LINQ to SQL Araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
