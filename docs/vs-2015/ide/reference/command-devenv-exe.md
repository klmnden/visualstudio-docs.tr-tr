---
title: -Command (devenv.exe) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- Devenv, /command switch
- /command Devenv switch
ms.assetid: 13c20cd6-f09d-400a-8b7b-ecc266a32cef
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: a87be2f0b60b02588b5ba73e5837caca1b4bd8ab
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65685841"
---
# <a name="command-devenvexe"></a>/Command (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Başlatıldıktan sonra belirtilen komutu yürütür [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] tümleşik geliştirme ortamı (IDE).  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
devenv /command CommandName  
```  
  
## <a name="arguments"></a>Arguments  
 `CommandName`  
 Gerekli. Tam adı bir [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] komut ya da çift tırnak işareti içine alınmış, diğer ad. Komut ve diğer ad sözdizimi hakkında daha fazla bilgi için bkz: [Visual Studio komutları](../../ide/reference/visual-studio-commands.md).  
  
## <a name="remarks"></a>Açıklamalar  
 Başlangıç tamamlandıktan sonra IDE adlandırılmış komutu yürütür. Bu anahtarı kullanırsanız, IDE aşağıdaki dotnetclıtools'u görüntülemiyor [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] başlangıcında başlangıç sayfası.  
  
 Bir eklenti bir komut sunarsa, komut satırından eklentiyi başlatmak için bu anahtarı kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Eklenti Yöneticisi'ni kullanarak eklentileri denetleme](https://msdn.microsoft.com/library/4f60444a-cb48-4cdb-8df4-941f6419aeeb).  
  
## <a name="example"></a>Örnek  
 Bu örnek başlatır [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] ve makro açık sık kullanılan dosyaları otomatik olarak çalıştırır.  
  
```  
devenv /command "Macros.MyMacros.Module1.OpenFavoriteFiles"  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
