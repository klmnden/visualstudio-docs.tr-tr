---
title: -Log (devenv.exe) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- Devenv, /Log switch
- Log switch [devenv.exe]
- /Log Devenv switch
ms.assetid: ae23c4ae-2376-4fe3-b8d2-81d34e61c8ba
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 8e9e5178be0301bcf2ab14b0d52d6aa3b54bc52a
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54763179"
---
# <a name="log-devenvexe"></a>/Log (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Tüm etkinliği, sorun giderme amacıyla günlük dosyasına kaydeder. Bu dosya çağırdıktan sonra görünür `devenv /log` en az bir kez. Varsayılan olarak, bu günlük dosyasıdır:  
  
 *%APPDATA%* \Microsoft\VisualStudio\\*Version*\ActivityLog.xml  
  
 Burada *sürüm* Visual Studio sürümüdür. Ancak, farklı bir yol ve dosya adı belirtebilirsiniz.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Devenv /log Path\NameOfLogFile  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Bu anahtar, diğer tüm anahtarlardan sonra komut satırının en sonunda görünmelidir.  
  
 Günlük, / log anahtarı ile çağrılan Visual Studio'nun tüm örnekleri için yazılır. Anahtar olmadan çağrılan Visual Studio örneklerini oturumu değil.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Devenv Komut Satırı Anahtarları](../../ide/reference/devenv-command-line-switches.md)
