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
ms.openlocfilehash: 94e8e87f4440644f76906a70ea09a46282b109c2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68163374"
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
