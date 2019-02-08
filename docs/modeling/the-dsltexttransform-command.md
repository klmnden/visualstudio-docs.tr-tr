---
title: DslTextTransform Komutu
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, commands
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 89d83da450014ebf29e2882438d27f9284c9bbbb
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55939040"
---
# <a name="the-dsltexttransform-command"></a>DslTextTransform Komutu
DslTextTransform.cmd TextTransform.exe çağırır ve sık kullanılan seçenekleri ile çalışan bir komut dosyasıdır. DslTextTransformation.cmd, gecelik bir derleme otomatikleştirmek için kullanabileceğiniz, [!INCLUDE[dsl](../modeling/includes/dsl_md.md)] projeleri. Daha fazla bilgi için [TextTransform yardımcı programı ile dosya oluşturma](../modeling/generating-files-with-the-texttransform-utility.md).

 DslTextTransform.cmd şu dizinde bulunur:

 **\<Visual Studio SDK'sını yükleme yolu > \VisualStudioIntegration\Tools\Bin**

 Şu bağımsız değişkenler DslTextTransform.cmd giriş olarak belirtebilirsiniz:

- Etki alanı modeli projenin çıkış dizini.

- Tasarımcı tanımı projenin çıkış dizini.

- Metin şablonu dosyasının konumu.

  Varsayılan yönerge işlemcileri ve derlemeler kullanılarak belirtilen bir metin şablonu dosyasını DslTextTransform.cmd işler. Özel yönerge işlemcileri oluşturma, TextTransform.exe çağıran kendi toplu iş dosyası oluşturabilirsiniz. Bu toplu iş dosyasında bütünleştirilmiş kodlarınızı ve ilişkili özel yönerge işlemcisi belirtebilirsiniz.