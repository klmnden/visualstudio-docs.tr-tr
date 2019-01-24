---
title: -DebugExe (devenv.exe) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- Devenv, /DebugExe switch
- DebugExe switch
- /DebugExe [devenv.exe]
ms.assetid: cd700006-1648-418f-924b-4b1e5c1412ab
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 1edbcddd27f2c3637e0e56dd9b4841e17ace16af
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54767569"
---
# <a name="debugexe-devenvexe"></a>/DebugExe (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Ayıklanacak belirtilen yürütülebilir dosyayı açar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Devenv /debugexe ExecutableFile  
```  
  
## <a name="arguments"></a>Arguments  
 `ExecutableFile`  
 Gerekli. Bir .exe dosyası yolu ve dosya adı.  
  
 .Exe dosyası bulunamadı veya yok, hiçbir uyarı veya hata görüntülenir ve [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] normalde başlatır.  
  
## <a name="remarks"></a>Açıklamalar  
 Aşağıdaki dizeleri `ExecutableFile` parametresi, o dosya için bağımsız değişken olarak geçirilir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte dosyayı açar `MyApplication.exe` hata ayıklama.  
  
```  
Devenv.exe /debugexe MyApplication.exe  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Devenv Komut Satırı Anahtarları](../../ide/reference/devenv-command-line-switches.md)
