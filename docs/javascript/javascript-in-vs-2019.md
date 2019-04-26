---
title: JavaScript ve TypeScript, Visual Studio 2019
ms.date: 03/27/2019
ms.technology: vs-javascript
ms.topic: conceptual
dev_langs:
- JavaScript
- TypeScript
- DHTML
author: mikejo5000
ms.author: mikejo
manager: jillfra
monikerRange: '>= vs-2019'
ms.openlocfilehash: 3000510c6bb6079629a3df05909417593569c932
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62553261"
---
# <a name="javascript-and-typescript-in-visual-studio-2019"></a>JavaScript ve TypeScript, Visual Studio 2019

## <a name="overview"></a>Genel Bakış

Visual Studio 2019 sağlar JavaScript kullanarak doğrudan hem de kullanarak JavaScript geliştirme için zengin Destek [programlama dilini TypeScript](http://www.typescriptlang.org), daha verimli ve eğlenceli bir JavaScript sağlamak için geliştirilmiş Özellikle, uygun ölçekte projeleri geliştirirken geliştirme deneyimi. Birçok uygulama türleri ve hizmetler için Visual Studio'da JavaScript veya TypeScript kodu yazabilirsiniz.

## <a name="javascript-language-service"></a>JavaScript Dil Servisi

Visual Studio 2019 JavaScript deneyim TypeScript desteği sağlayan aynı altyapısı ile desteklenmektedir. Bu, daha iyi özellik desteği, zenginlik ve hemen,-hazır tümleştirme sağlar.

Eski JavaScript language Service'a geri yükleme seçeneği artık kullanılabilir. Kullanıcılar, artık yeni JavaScript dil hizmeti,-hazır vardır. Yeni dil hizmetini yalnızca statik analiz tarafından desteklenen TypeScript dil hizmeti temel alır. Bu JavaScript kodunuzun daha zengin IntelliSense tür tanımlarını temel alarak yararlanabilir, böylece daha iyi araç kullanımı ile sağlamamız sağlar. Yeni hizmet, basit ve kendi kod ölçekler olarak daha iyi performans sağlayan eski hizmet, daha az bellek tüketir. Ayrıca daha büyük projeler işlemek için dil Hizmeti performansını geliştirdik.

## <a name="typescript-support"></a>TypeScript desteği

Visual Studio 2019 projenizde TypeScript derleme tümleştirmeye yönelik çeşitli seçenekler sunar:

* [TypeScript NuGet paketini](https://www.nuget.org/packages/Microsoft.TypeScript.MSBuild). TypeScript 3.2 veya üzeri NuGet paketini projenize yüklendiğinde, karşılık gelen TypeScript dil hizmeti sürümü Düzenleyicisi'nde yüklenen.
* Varsayılan olarak, bir tek başına SDK'sı indirilerek yanı sıra, Visual Studio yükleyicisi TypeScript SDK [VS Market'te](https://marketplace.visualstudio.com/items?itemName=TypeScriptTeam.typescript-331-vs2017).
* [TypeScript npm paket](https://www.npmjs.com/package/typescript). TypeScript 2.1 veya üzeri bir npm paketi projenize yüklendiğinde, karşılık gelen TypeScript dil hizmeti sürümü Düzenleyicisi'nde yüklenen.

Visual Studio 2019 içinde geliştirilen projeleri için TypeScript NuGet ve npm paketleri farklı platformlar ve ortamlar arasında büyük taşınabilirlik için kullanmanızı öneririz.

## <a name="projects"></a>Projeler

UWP JavaScript uygulamaları artık Visual Studio 2019’da desteklenmemektedir. Oluşturun veya açın JavaScript UWP projeleri (uzantısına sahip dosyaların *.jsproj*). Belgelerimizi daha kullanarak öğrenebilirsiniz [aşamalı Web uygulamaları (PWAs) oluşturma](https://docs.microsoft.com/microsoft-edge/progressive-web-apps/get-started) de Windows üzerinde çalışan.
