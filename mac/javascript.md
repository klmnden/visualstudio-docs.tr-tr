---
title: JavaScript ve TypeScript
description: Mac için Visual Studio JavaScript desteği hakkında bilgi
author: conceptdev
ms.author: crdun
ms.date: 05/03/2018
ms.topic: article
ms.technology: vs-ide-general
ms.assetid: 61432695-5B12-4257-B250-48D37EED106D
ms.openlocfilehash: ed84e5478ae7a15905a5555a318bd656c664710e
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/18/2019
ms.locfileid: "56335213"
---
# <a name="javascript-and-typescript-support"></a>JavaScript ve TypeScript desteği

Mac için Visual Studio, JavaScript ve TypeScript söz dizimi vurgulama, kod biçimlendirme ve IntelliSense desteğini sağlar.

![typescript Düzenleyicisi desteği](https://msdnshared.blob.core.windows.net/media/2018/03/TypeScript-editor.gif)

JavaScript Yazma ile ilgili daha fazla bilgi için bkz [JavaScript kodu yazma](/scripting/javascript/writing-javascript-code) Kılavuzlar.

## <a name="adding-a-javascript-file"></a>Bir JavaScript dosyası ekleme

JavaScript dosyaları ile ASP.NET Core projeleri için çoğunlukla eklenir **yeni dosya** iletişim. Bir javascript dosyası eklemek için projenize sağ tıklayın ve Git **Ekle > yeni dosya**:

![Yeni dosyalar projeye ekleniyor](media/javascript-image1.png)

Gelen **yeni dosya** iletişim kutusunda **Web > boş bir JS dosyasına** veya **Web > TypeScript dosyası**. Bir ad verin ve ardından **yeni**:

![Şablondan Yeni bir typescript dosyası](media/javascript-image2.png)

## <a name="intellisense"></a>IntelliSense

Visual Studio Mac kullanımlar için [JavaScript dil hizmeti](/visualstudio/ide/javascript-intellisense) IntelliSense sağlamak için akıllı kod tamamlama, parametre bilgisi ve üye listelerini kodu yazarken sahip etmenize imkan sağlar.

Tür çıkarımı, JSDoc veya TypeScript Mac için Visual Studio'daki JavaScript IntelliSense temel alabilir bildirimi.

- **Anlam çıkarma** – ile çevreleyen kod bağlamı verdi bir nesnenin türü. Daha fazla bilgi için üzerinde Visual Studio'nun bölümüne bakın. [IntelliSense temel tür çıkarımı üzerinde](/visualstudio/ide/javascript-intellisense#intellisense-based-on-type-inference).
- **JSDoc** – ne tür çıkarımı sunmaz doğru tür bilgilerini zamanlar. Bu durumlarda, tür bilgisi tarafından açık olarak sağlanabilir [JSDoc](http://usejsdoc.org/about-getting-started.html) ek açıklamalar. Daha fazla bilgi için üzerinde Visual Studio'nun bölümüne bakın. [IntelliSense JSDoc tabanlı](/visualstudio/ide/javascript-intellisense#intellisense-based-on-jsdoc)
- **TypeScript bildirim dosyaları** – `.d.ts` dosyaları değerleri için JavaScript IntelliSense sağlamak amacıyla kullanılır. Bu dosyada bildirilen türleri JSDoc yorumları türleri olarak kullanılabilir. Daha fazla bilgi için üzerinde Visual Studio'nun bölümüne bakın. [IntelliSense temel TypeScript bildirim dosyaları](/visualstudio/ide/javascript-intellisense#intellisense-based-on-typescript-declaration-files)

    ![bir typescript tanım dosyası ekleme](media/javascript-image3.png)

## <a name="see-also"></a>Ayrıca bkz.

- [JavaScript IntelliSense (Windows için Visual Studio)](/visualstudio/ide/javascript-intellisense)
