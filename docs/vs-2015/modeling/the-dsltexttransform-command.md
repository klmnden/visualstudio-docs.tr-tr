---
title: DslTextTransform komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, commands
ms.assetid: 7d025d0b-6543-4a49-9f6b-8b8cfcad77ee
caps.latest.revision: 32
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 220ceab29cb2b9bc1b117a98326d22c3c546a162
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62548507"
---
# <a name="the-dsltexttransform-command"></a>DslTextTransform Komutu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

DslTextTransform.cmd TextTransform.exe çağırır ve sık kullanılan seçenekleri ile çalışan bir komut dosyasıdır. DslTextTransformation.cmd, gecelik bir derleme otomatikleştirmek için kullanabileceğiniz, [!INCLUDE[dsl](../includes/dsl-md.md)] projeleri. Daha fazla bilgi için [TextTransform yardımcı programı ile dosya oluşturma](../modeling/generating-files-with-the-texttransform-utility.md).  
  
 DslTextTransform.cmd şu dizinde bulunur:  
  
 **\<Visual Studio SDK'sını yükleme yolu > \VisualStudioIntegration\Tools\Bin**  
  
 Şu bağımsız değişkenler DslTextTransform.cmd giriş olarak belirtebilirsiniz:  
  
- Etki alanı modeli projenin çıkış dizini.  
  
- Tasarımcı tanımı projenin çıkış dizini.  
  
- Metin şablonu dosyasının konumu.  
  
  Varsayılan yönerge işlemcileri ve derlemeler kullanılarak belirtilen bir metin şablonu dosyasını DslTextTransform.cmd işler. Özel yönerge işlemcileri oluşturma, TextTransform.exe çağıran kendi toplu iş dosyası oluşturabilirsiniz. Bu toplu iş dosyasında bütünleştirilmiş kodlarınızı ve ilişkili özel yönerge işlemcisi belirtebilirsiniz.
