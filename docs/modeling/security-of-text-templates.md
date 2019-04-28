---
title: Metin Şablonlarının Güvenliği
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- text templates, security
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 66159516c6b1360203130dedb56c0e6c192a118a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62824026"
---
# <a name="security-of-text-templates"></a>Metin Şablonlarının Güvenliği
Metin şablonları aşağıdaki güvenlik sorunları vardır:

- Metin şablonları, rastgele kod eklemelerin savunmasızdır.

- Konağın bir yönerge işlemcisi bulmak için kullandığı mekanizması güvenli değilse, kötü amaçlı bir yönerge işlemcisi çalıştırabilir.

## <a name="arbitrary-code"></a>Rastgele kod
 Bir şablon yazdığınızda, içinde herhangi bir kodu koyabilirsiniz \<## > etiketleri. Bu, bir metin şablonu içinde yürütülmek üzere rastgele kod sağlar.

 Güvenilen kaynaklardan gelen şablonları edinmek emin olun. Uygulamanızın güvenilir kaynaklardan gelen şablonları yürütmek için son kullanıcılardan uyar emin olun.

## <a name="malicious-directive-processor"></a>Kötü amaçlı bir yönerge işlemcisi
 Metin şablonu motoru, bir dönüştürme ana bilgisayarı ve bir veya daha fazla yönerge işlemcileri bir çıktı dosyası şablonu metne dönüştürmek için ile etkileşim kurar. Daha fazla bilgi için [metin şablonu dönüştürme süreci](../modeling/the-text-template-transformation-process.md).

 Konağın bir yönerge işlemcisi bulmak için kullandığı mekanizması güvenli değilse, çalışan bir kötü amaçlı bir yönerge işlemcisi riskini çalıştırır. Kötü amaçlı bir yönerge işlemcisi içinde çalışan kodu sağlayabilir `FullTrust` şablonunu çalıştırdığınızda modu. Bir özel metin şablonu dönüştürme ana bilgisayarı oluşturursanız, yönerge işlemcileri bulunacak altyapısı için kayıt defteri gibi güvenli bir mekanizma kullanmanız gerekir.