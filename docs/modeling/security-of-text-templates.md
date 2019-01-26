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
ms.prod: visual-studio-dev15
ms.openlocfilehash: 94b2520ffafe3e99420bf77577b59341b6d216aa
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54957214"
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