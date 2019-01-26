---
title: DSL Tanımlarına Uzantılar Ekleme
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: 25eeb42fe4fda0ed2f4ac88e1caf0e00d74f0259
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54979289"
---
# <a name="add-extensions-to-dsl-definitions"></a>DSL Tanımlarına Uzantı Ekleme

DSL tanımı uzantısı, uzantı bir etki alanına özgü dil (DSL) için bir paket oluşturmanıza olanak sağlar. Bir DSL aynı şekilde bir kullanıcının bilgisayarında bulunan bir Visual Studio Tümleştirme Uzantısı'na (VSIX) DSL uzantısının yüklenebilir. Ek özellikleri dinamik olarak etkin ve çalışma zamanında devre dışı. DSL uzantısı açıkça tasarlanmış olması gerekmez ve uzantıları daha sonra veya üçüncü tarafların genişletilmiş DSL değiştirmeden tasarlanabilir.

DSL uzantıları aşağıdaki özellikleri içerebilir:

-   Model ve sunu öğelerinin özellikleri

-   Dekoratörler için şekilleri ve bağlayıcıları

-   Sınıfları, ilişkilerini, şekiller ve bağlayıcılar

-   Doğrulama kısıtlamaları

-   Araç kutusu öğeleri ve sekmeler

Genişletilmiş bir DSL kullanıcısı oluşturabilir ve ek özellikler örneklerini içeren bir modeli kaydedin. Model uygun uzantısı yüklü diğer kullanıcılar tarafından okunabilir. Uzantı yüklü olmayan kullanıcılar, ek özellikleri kullanamaz, ancak güncelleştirin ve ek özellikler kaybetmeden bir modeli kaydedin.

[!INCLUDE[modeling_sdk_info](includes/modeling_sdk_info.md)]

## <a name="see-also"></a>Ayrıca Bkz.

- [İlgili blog gönderileri](https://blogs.msdn.microsoft.com/visualstudioalm/tag/code-index/)
