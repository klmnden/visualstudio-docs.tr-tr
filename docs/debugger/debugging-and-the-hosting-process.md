---
title: Hata ayıklama ve barındırma işlemi | Microsoft Docs
ms.date: 08/01/2018
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [Visual Studio], hosting process
- hosting process
ms.assetid: d0f0b9a6-2a6e-463d-b6ea-9518ee727933
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: af0d57e39fa8d1312032bacbbd9af95d44449ca1
ms.sourcegitcommit: 3ca33862c1cfc3ccb83de3e95f1e69e860ab143a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57525836"
---
# <a name="debugging-and-the-hosting-process"></a>Hata Ayıklama ve Barındırma İşlemi
Visual Studio barındırma işlemini, hata ayıklayıcı performansı artırır ve kısmi güven hata ayıklama ve tasarım zamanı ifade değerlendirmesi gibi yeni hata ayıklayıcı özelliklerini etkinleştirir. Gerekirse, barındırma işlemini devre dışı bırakabilirsiniz. Aşağıdaki bölümlerde, barındırma işlemi olmadan ve hata ayıklama arasındaki bazı farklar açıklanmaktadır.

> [!NOTE]
> Visual Studio 2017'den itibaren barındırma işlemi kullanarak hata ayıklama seçeneği artık gerekli değildir ve kaldırıldı. Daha fazla bilgi için [hata ayıklama: Az sık kullanılan işinizi hızlandırmak için Visual Studio 2017 Aıms](https://vslive.com/Blogs/News-and-Tips/2017/02/Debugging-Visual-Studio-2017-aims-to-speed-up-your-least-favorite-job.aspx).

## <a name="partial-trust-debugging-and-click-once-security"></a>Kısmi güven hata ayıklama ve tıklayın-bir kez güvenlik
 Kısmi güven hata ayıklama barındırma işlemini gerektiriyor. Barındırma işlemini devre dışı bırakırsanız, kısmi güven güvenliği etkinleştirilmiş olsa dahi kısmi güven hata ayıklama çalışmaz **güvenlik** sayfasının **proje özellikleri**. Daha fazla bilgi için [nasıl yapılır: Kısmen güvenilen uygulamada hata ayıklama](/visualstudio/debugger/debugger-security).

## <a name="design-time-expression-evaluation"></a>Tasarım zamanı ifade değerlendirmesi
 Tasarım zamanı ifade her zaman, barındırma işlemi kullanır. Barındırma devre dışı bırakma işlemi **proje özellikleri** sınıf kitaplığı projeleri için tasarım zamanı ifade değerlendirmesi devre dışı bırakır. Diğer proje türleri için tasarım zamanı ifade değerlendirmesi devre dışı değil. Bunun yerine, Visual Studio gerçek yürütülebilir başlar ve barındırma işlemi olmadan tasarım zamanı değerlendirmesi için kullanır. Bu fark, farklı sonuçlar üretebilir.

## <a name="appdomaincurrentdomainfriendlyname-differences"></a>AppDomain.CurrentDomain.FriendlyName farkları
 `AppDomain.CurrentDomain.FriendlyName` barındırma işlemi etkin olup olmadığını bağlı olarak farklı sonuçlar döndürür. Eğer `AppDomain.CurrentDomain.FriendlyName` barındırma işlemi etkin döndürür *app_name*`.vhost.exe`. Bunu devre dışı barındırma işlemini çağırdığınızda, döndürür *app_name*`.exe`.

## <a name="assemblygetcallingassemblyfullname-differences"></a>Assembly.GetCallingAssembly(). FullName farkları
 `Assembly.GetCallingAssembly().FullName` barındırma işlemi etkin olup olmadığını bağlı olarak farklı sonuçlar döndürür. Eğer `Assembly.GetCallingAssembly().FullName` barındırma işlemi etkin döndürür `mscorlib`. Eğer `Assembly.GetCallingAssembly().FullName` barındırma işlemini devre dışı uygulama adını döndürür.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Kısmen Güvenilen Uygulamada Hata Ayıklama](/visualstudio/debugger/debugger-security)