---
title: DSL tanımlarına uzantılar ekleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
ms.assetid: 07e133be-92ab-4936-a02b-45d2012bd0a6
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: bd45a2345e6e5b28b74cb27fac226514c3f92a04
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54766278"
---
# <a name="adding-extensions-to-dsl-definitions"></a>DSL Tanımlarına Uzantılar Ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

DSL tanımı uzantısı, uzantı bir etki alanına özgü dil (DSL) için bir paket oluşturmanıza olanak sağlar. Bir DSL aynı şekilde bir kullanıcının bilgisayarında bulunan bir Visual Studio Tümleştirme Uzantısı'na (VSIX) DSL uzantısının yüklenebilir. Ek özellikleri dinamik olarak etkin ve çalışma zamanında devre dışı. DSL uzantısı açıkça tasarlanmış olması gerekmez ve uzantıları daha sonra veya üçüncü tarafların genişletilmiş DSL değiştirmeden tasarlanabilir.  
  
 Ek özellikler şunları içerebilir:  
  
- Model ve sunu öğelerinin özellikleri  
  
- Dekoratörler için şekilleri ve bağlayıcıları  
  
- Sınıfları, ilişkilerini, şekiller ve bağlayıcılar  
  
- Doğrulama kısıtlamaları  
  
- Araç kutusu öğeleri ve sekmeler  
  
  Genişletilmiş bir DSL kullanıcısı oluşturun ve ek özellikler örneklerini içeren bir modeli kaydedin ve bunlar uygun uzantısı yüklü diğer kullanıcılar tarafından okunabilir. Uzantı yüklü olmayan kullanıcılar, ek özellikleri kullanamaz, ancak güncelleştirin ve ek özellikler kaybetmeden bir modeli kaydedin.  
  
  Örnek kod ve bu özellik hakkında daha fazla bilgi için bkz: [Visual Studio Görselleştirme ve modelleme SDK'sı](http://go.microsoft.com/fwlink/?LinkID=186128) Web sitesi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Görselleştirme ve modelleme SDK'sı](http://go.microsoft.com/fwlink/?LinkID=186128)
