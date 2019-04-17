---
title: -Updateconfiguration (devenv.exe) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- /updateconfiguration Devenv switch
- Devenv, /updateconfiguration switch
- updateconfiguration Devenv switch
ms.assetid: 9a1084cc-8b68-4ccc-aaea-f95939164338
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 9ffc9410d64f58fff771a0e9b251ee1131eaea5e
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59670037"
---
# <a name="updateconfiguration-devenvexe"></a>/ Updateconfiguration (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bildirir [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] birleştirilecek [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] sistem ve MEF paketleri önbelleğe herhangi bir değişiklik.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
devenv /updateconfiguration  
```  
  
## <a name="remarks"></a>Açıklamalar  
 [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] Bu komut, bir VSIX paketi yüklediğinizde otomatik olarak çalıştırır. Çalıştırmalısınız `devenv.exe /updateconfiguration` dosyalarınızı düzeltme eki uygulama sonra böylece [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] MEF önbelleği güncelleştirir. Bu, düzeltmenizi yeterli olup olmadığını değerlendirmek sağlar.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki komut satırı nedenleri [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] birleştirilecek [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] sistem ve MEF paketleri önbelleğe herhangi bir değişiklik.  
  
```  
Devenv.exe /updateconfiguration  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio'da geliştirme ayarlarını özelleştirme](http://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3)   
 [Devenv Komut Satırı Anahtarları](../../ide/reference/devenv-command-line-switches.md)
