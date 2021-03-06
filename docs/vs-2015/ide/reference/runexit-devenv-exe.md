---
title: -Runexit (devenv.exe) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- runexit Devenv switch
- Devenv, /runexit switch
- /runexit Devenv switch
ms.assetid: bfc94875-5fc0-4110-b961-d59c0b403790
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 0206f01df517c2dbd0c1c4052201dc8ded1bcbf9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68163403"
---
# <a name="runexit-devenvexe"></a>/Runexit (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Derler ve belirtilen proje veya çözüm çalıştırır ve ardından tümleşik geliştirme ortamı (IDE) kapatır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
devenv /runexit {SolutionName|ProjectName}  
```  
  
## <a name="arguments"></a>Arguments  
 `SolutionName`  
 Gerekli. Bir çözüm dosyası adını ve tam yolu.  
  
 `ProjectName`  
 Gerekli. Bir proje dosyasının adını ve tam yolu.  
  
## <a name="remarks"></a>Açıklamalar  
 Derler ve belirtilen proje veya çözümü etkin çözüm yapılandırması için belirtilen ayarlara göre çalıştırır. IDE projeyi sırasında bu anahtar en aza indirir veya çözümü çalıştırın, sonra projeyi IDE'yi kapatır ve çözüm çalışması tamamlandıktan.  
  
- Çift tırnak içine boşluk dizeleri alın.  
  
- Hataları dahil olmak üzere Özet bilgileri görüntülenebilir **komut** penceresinde veya belirtilen herhangi bir günlük dosyasını `/out` geçin.  
  
## <a name="example"></a>Örnek  
 Bu örnek çözüm çalıştırılır `MySolution` simge durumuna küçültülmüş IDE'de etkin dağıtım yapılandırması kullanan ve daha sonra IDE'yi kapatır.  
  
```  
devenv /runexit "C:\Documents and Settings\someuser\My Documents\Visual Studio\Projects\MySolution\MySolution.sln"  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)   
 [/ Çalıştırma (devenv.exe)](../../ide/reference/run-devenv-exe.md)   
 [/ Derleme (devenv.exe)](../../ide/reference/build-devenv-exe.md)   
 [/ Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)   
 [/ (Devenv.exe out)](../../ide/reference/out-devenv-exe.md)
