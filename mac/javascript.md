---
title: JavaScript
description: Mac için Visual Studio Javascript desteği hakkında bilgi
author: conceptdev
ms.author: crdun
ms.date: 05/03/2018
ms.topic: article
ms.technology: vs-ide-general
ms.assetid: 61432695-5B12-4257-B250-48D37EED106D
ms.openlocfilehash: 6efc22f916973f292daa97bdd6b5129ac9311f04
ms.sourcegitcommit: 71218ffc33da325cc1b886f69ff2ca50d44f5f33
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/09/2018
ms.locfileid: "48881078"
---
# <a name="javascript-support"></a>JavaScript desteği

Mac için Visual Studio, Javascript ve Typescript söz dizimi vurgulama, kod biçimlendirme ve IntelliSense desteğini sağlar. 

![typescript Düzenleyicisi desteği](https://msdnshared.blob.core.windows.net/media/2018/03/TypeScript-editor.gif)

JavaScript Yazma ile ilgili daha fazla bilgi için bkz [Javascript kodu yazma](https://docs.microsoft.com/scripting/javascript/writing-javascript-code) Kılavuzlar.

## <a name="adding-a-javascript-file"></a>Bir JavaScript dosyası ekleme

JavaScript dosyaları ile ASP.NET Core projeleri için çoğunlukla eklenir **yeni dosya** iletişim. Bir javascript dosyası eklemek için projenize sağ tıklayın ve Git **Ekle > yeni dosya**: 

![Yeni dosyalar projeye ekleniyor](media/javascript-image1.png)

Yeni dosya iletişim kutusundan seçin **Web > boş bir JS dosyasına** veya **Web > Typescript dosyası**. Bir ad verin ve ardından **yeni**:

![Şablondan Yeni bir typescript dosyası](media/javascript-image2.png)

## <a name="intellisense"></a>IntelliSense

Visual Studio Mac kullanımlar için [Javascript dil hizmeti](/visualstudio/ide/javascript-intellisense) IntelliSense sağlamak için akıllı kod tamamlama, parametre bilgisi ve üye listelerini kodu yazarken sahip etmenize imkan sağlar.

Tür çıkarımı, JSDoc veya Typescript Mac için Visual Studio'daki JavaScript IntelliSense temel alabilir bildirimi.

- **Anlam çıkarma** – ile çevreleyen kod bağlamı verdi bir nesnenin türü. Daha fazla bilgi için üzerinde Visual Studio'nun bölümüne bakın. [IntelliSense temel tür çıkarımı üzerinde](https://docs.microsoft.com/visualstudio/ide/javascript-intellisense#intellisense-based-on-type-inference).
- **JSDoc** – ne tür çıkarımı sunmaz doğru tür bilgilerini zamanlar. Bu durumlarda, tür bilgisi tarafından açık olarak sağlanabilir [JSDoc](http://usejsdoc.org/about-getting-started.html) ek açıklamalar. Daha fazla bilgi için üzerinde Visual Studio'nun bölümüne bakın. [IntelliSense JSDoc tabanlı](https://docs.microsoft.com/visualstudio/ide/javascript-intellisense#intellisense-based-on-jsdoc)
- **TypeScript bildirim dosyaları** – `.d.ts` dosyaları değerleri için Javascript IntelliSense sağlamak amacıyla kullanılır. Bu dosyada bildirilen türleri JSDoc yorumları türleri olarak kullanılabilir. Daha fazla bilgi için üzerinde Visual Studio'nun bölümüne bakın. [IntelliSense temel TypeScript bildirim dosyaları üzerinde](https://docs.microsoft.com/visualstudio/ide/javascript-intellisense#intellisense-based-on-typescript-declaration-files) ![typescript tanım dosyası ekleme](media/javascript-image3.png)