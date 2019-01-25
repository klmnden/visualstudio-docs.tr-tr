---
title: -Setup (devenv.exe) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- setup Devenv switch
- /setup Devenv switch
- Devenv, /setup switch
ms.assetid: 87608b7f-a156-400c-80f5-fc823f843e61
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 0df3b74b6c5acc4b8630dcf5759dd3fd6e7a1afe
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54805371"
---
# <a name="setup-devenvexe"></a>/Setup (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Zorlar [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] menüleri, araç çubukları ve komut gruplarından tüm kullanılabilir VSPackages tanımlayan kaynak meta verileri birleştirmek için.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
devenv /setup  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Bu anahtar hiçbir bağımsız değişkeni alır. `devenv /setup` Komut genellikle yükleme işleminin son adımı verilir. Kullanım `/setup` anahtar başlamıyor [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
 Çalıştırmalısınız `devenv` kullanabilmek için yönetici olarak [/Setup (devenv.exe)](../../ide/reference/setup-devenv-exe.md) ve [/InstallVSTemplates (devenv.exe)](../../ide/reference/installvstemplates-devenv-exe.md) anahtarlar.  
  
## <a name="example"></a>Örnek  
 Bu örnek, bir sürümünü yükleme işleminin son adımında gösterir [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] VSPackage içeren.  
  
```  
devenv /setup  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Devenv Komut Satırı Anahtarları](../../ide/reference/devenv-command-line-switches.md)
