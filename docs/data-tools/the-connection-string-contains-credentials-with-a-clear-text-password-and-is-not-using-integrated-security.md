---
title: Bağlantı dizesi şifresiz parola içeren kimlik bilgileri içeriyor ve tümleşik güvenliği kullanmıyor
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 501d85af-92e0-4471-b280-8a59c0688575
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: b270290c948807ff0f66d3d142312245475cd33c
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65460602"
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

- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)