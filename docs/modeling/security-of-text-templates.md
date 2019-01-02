---
title: Metin Şablonlarının Güvenliği
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- text templates, security
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: bb5ad4348d681a2b7bc59c588bb74e0a27813e73
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53820818"
---
# <a name="security-of-text-templates"></a>Metin Şablonlarının Güvenliği
Metin şablonları aşağıdaki güvenlik sorunları vardır:

-   Metin şablonları, rastgele kod eklemelerin savunmasızdır.

-   Konağın bir yönerge işlemcisi bulmak için kullandığı mekanizması güvenli değilse, kötü amaçlı bir yönerge işlemcisi çalıştırabilir.

## <a name="arbitrary-code"></a>Rastgele kod
 Bir şablon yazdığınızda, içinde herhangi bir kodu koyabilirsiniz \<## > etiketleri. Bu, bir metin şablonu içinde yürütülmek üzere rastgele kod sağlar.

 Güvenilen kaynaklardan gelen şablonları edinmek emin olun. Uygulamanızın güvenilir kaynaklardan gelen şablonları yürütmek için son kullanıcılardan uyar emin olun.

## <a name="malicious-directive-processor"></a>Kötü amaçlı bir yönerge işlemcisi
 Metin şablonu motoru, bir dönüştürme ana bilgisayarı ve bir veya daha fazla yönerge işlemcileri bir çıktı dosyası şablonu metne dönüştürmek için ile etkileşim kurar. Daha fazla bilgi için [metin şablonu dönüştürme süreci](../modeling/the-text-template-transformation-process.md).

 Konağın bir yönerge işlemcisi bulmak için kullandığı mekanizması güvenli değilse, çalışan bir kötü amaçlı bir yönerge işlemcisi riskini çalıştırır. Kötü amaçlı bir yönerge işlemcisi içinde çalışan kodu sağlayabilir `FullTrust` şablonunu çalıştırdığınızda modu. Bir özel metin şablonu dönüştürme ana bilgisayarı oluşturursanız, yönerge işlemcileri bulunacak altyapısı için kayıt defteri gibi güvenli bir mekanizma kullanmanız gerekir.