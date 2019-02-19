---
title: -Güvenli modda (devenv.exe) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- /SafeMode Devenv switch
- Devenv, /SafeMode switch
- SafeMode switch
ms.assetid: b191f6a5-8f12-47ec-bcc7-b68149a22aa8
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 4c1cd4b15c3ce3462d6d49eca39fedbc64c744c7
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54767308"
---
# <a name="safemode-devenvexe"></a>/SafeMode (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Başlar [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] güvenli modda, yalnızca varsayılan ortama ve Hizmetleri Yükleniyor.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
devenv /SafeMode   
```  
  
## <a name="remarks"></a>Açıklamalar  
 Bu anahtar, ne zaman yüklenmesini tüm üçüncü taraf VSPackages engeller [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] böylece kararlı yürütme sağlamaya başlar.  
  
## <a name="description"></a>Açıklama  
 Aşağıdaki örnek başlatır [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] güvenli modda.  
  
## <a name="code"></a>Kod  
  
```  
Devenv.exe /SafeMode  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Devenv Komut Satırı Anahtarları](../../ide/reference/devenv-command-line-switches.md)
