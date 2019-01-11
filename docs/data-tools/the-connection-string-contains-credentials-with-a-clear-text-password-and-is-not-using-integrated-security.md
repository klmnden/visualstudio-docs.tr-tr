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
ms.openlocfilehash: ef63abe36a5880305f522d75d9e1cb1d7f6995fa
ms.sourcegitcommit: 59c48e1e42b48ad25a4e198af670faa4d8dae370
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/10/2019
ms.locfileid: "54204209"
---
# <a name="the-connection-string-contains-credentials-with-a-clear-text-password-and-is-not-using-integrated-security"></a>Bağlantı dizesi şifresiz parola içeren kimlik bilgileri içeriyor ve tümleşik güvenliği kullanmıyor

Bağlantı dizesini geçerli DBML dosyasının ve uygulama yapılandırma dosyaları ile bu hassas bilgileri kaydetmek istiyor musunuz?  Tıklayın **Hayır** bağlantı dizesini hassas bilgiler olmadan kaydetmek için.

Hassas bilgileri (bağlantı dizesine dahil parolalar) dahil veri bağlantıları ile çalışırken, bir projenin DBML dosyasının ve uygulama yapılandırma dosyası ile veya olmadan bağlantı dizesini kaydetme seçeneği sunulur. hassas bilgileri.

> [!WARNING]
> Açık olarak ayarlama **bağlantı** özellikleri **uygulama ayarları** özelliğini **False** DBML dosyasına parola ekleyeceksiniz.

## <a name="save-options"></a>Kaydetme seçenekleri

- Bağlantı dizesini hassas bilgilerle birlikte kaydetmek için seçin **Evet**.

   Bağlantı dizesi, bir uygulama ayarı olarak depolanır. Bağlantı dizesi düz metin olarak hassas bilgiler içerir. DBML dosyasının, hassas bilgileri içermiyor.

- Bağlantı dizesini hassas bilgiler olmadan kaydetmek için seçin **Hayır**.

   Bağlantı dizesi, bir uygulama ayarı olarak depolanır, ancak parola dahil değildir.

## <a name="see-also"></a>Ayrıca bkz.

- [O/R Tasarımcısı iletileri](../data-tools/o-r-designer-messages.md)
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)