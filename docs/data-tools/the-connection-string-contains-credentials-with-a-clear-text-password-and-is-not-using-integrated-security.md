---
title: Bağlantı dizesi şifresiz parola içeren kimlik bilgileri içeriyor ve tümleşik güvenliği kullanmıyor
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 501d85af-92e0-4471-b280-8a59c0688575
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 2f7d9c945d3e8897114f165464c0823cce3ceeae
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53854769"
---
# <a name="the-connection-string-contains-credentials-with-a-clear-text-password-and-is-not-using-integrated-security"></a>Bağlantı dizesi şifresiz parola içeren kimlik bilgileri içeriyor ve tümleşik güvenliği kullanmıyor

Bağlantı dizesini geçerli DBML dosyasının ve uygulama yapılandırma dosyaları ile bu hassas bilgileri kaydetmek istiyor musunuz?  Tıklayın **Hayır** bağlantı dizesini hassas bilgiler olmadan kaydetmek için.

Hassas bilgileri (bağlantı dizesine dahil parolalar) dahil veri bağlantıları ile çalışırken, bir projenin DBML dosyasının ve uygulama yapılandırma dosyası ile veya olmadan bağlantı dizesini kaydetme seçeneği sunulur. hassas bilgileri.

> [!WARNING]
> Açık olarak ayarlama **bağlantı** özellikleri **uygulama ayarları** özelliğini **False** DBML dosyasına parola ekleyeceksiniz.

## <a name="to-save-the-connection-string-with-the-sensitive-information-in-the-projects-application-settings"></a>Hassas bilgileri projenin uygulama ayarlarında bağlantı dizesini kaydetmek için

- **Evet**'i tıklayın.

   Bağlantı dizesi, bir uygulama ayarı olarak depolanır. Bağlantı dizesi düz metin olarak hassas bilgiler içerir. DBML dosyasının, hassas bilgileri içermiyor.

## <a name="to-save-the-connection-string-without-the-sensitive-information-in-the-projects-application-settings"></a>Projenin uygulama ayarlarında bağlantı dizesini hassas bilgiler olmadan kaydetmek için

- **Hayır**'a tıklayın.

   Bağlantı dizesi, bir uygulama ayarı olarak depolanır, ancak parola dahil değildir.

## <a name="see-also"></a>Ayrıca bkz.

- [O/R Tasarımcısı iletileri](../data-tools/o-r-designer-messages.md)
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)