---
title: Metin şablonlarının güvenliği | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- text templates, security
ms.assetid: 567a2383-7d43-4acc-af4a-cd70b7a0151e
caps.latest.revision: 25
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f21bfadd540ce365c7f585a35991c27395558c6e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68202687"
---
# <a name="security-of-text-templates"></a>Metin Şablonlarının Güvenliği
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Metin şablonları aşağıdaki güvenlik sorunları vardır:  
  
- Metin şablonları, rastgele kod eklemelerin savunmasızdır.  
  
- Konağın bir yönerge işlemcisi bulmak için kullandığı mekanizması güvenli değilse, kötü amaçlı bir yönerge işlemcisi çalıştırabilir.  
  
## <a name="arbitrary-code"></a>Rastgele kod  
 Bir şablon yazdığınızda, içinde herhangi bir kodu koyabilirsiniz \<## > etiketleri. Bu, bir metin şablonu içinde yürütülmek üzere rastgele kod sağlar.  
  
 Güvenilen kaynaklardan gelen şablonları edinmek emin olun. Uygulamanızın güvenilir kaynaklardan gelen şablonları yürütmek için son kullanıcılardan uyar emin olun.  
  
## <a name="malicious-directive-processor"></a>Kötü amaçlı bir yönerge işlemcisi  
 Metin şablonu motoru, bir dönüştürme ana bilgisayarı ve bir veya daha fazla yönerge işlemcileri bir çıktı dosyası şablonu metne dönüştürmek için ile etkileşim kurar. Daha fazla bilgi için [metin şablonu dönüştürme süreci](../modeling/the-text-template-transformation-process.md).  
  
 Konağın bir yönerge işlemcisi bulmak için kullandığı mekanizması güvenli değilse, çalışan bir kötü amaçlı bir yönerge işlemcisi riskini çalıştırır. Kötü amaçlı bir yönerge işlemcisi içinde çalışan kodu sağlayabilir `FullTrust` şablonunu çalıştırdığınızda modu. Bir özel metin şablonu dönüştürme ana bilgisayarı oluşturursanız, yönerge işlemcileri bulunacak altyapısı için kayıt defteri gibi güvenli bir mekanizma kullanmanız gerekir.
