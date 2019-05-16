---
title: -ResetSettings (devenv.exe) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- Devenv, /ResetSettings switch
- ResetSettings switch
- /ResetSettings Devenv switch
ms.assetid: 1d41021c-6f58-4bd5-b122-d1c995812192
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 1b35026140b424da0f7fa71cb9e70b72c3dba243
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65689655"
---
# <a name="resetsettings-devenvexe"></a>/ResetSettings (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Geri yükler [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] varsayılan ayarları ve otomatik olarak başlatan [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] IDE. İsteğe bağlı olarak belirtilen .vssettings dosya ayarlarını sıfırlar.  
  
 Varsayılan ayarlar, profili tarafından belirlenir seçilen [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] önce başlatıldı.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Devenv /ResetSettings SettingsFile  
```  
  
## <a name="arguments"></a>Arguments  
 `SettingsFile`  
 Uygulanacak .vssettings dosyasının adını ve tam yolunu [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
 Genel Geliştirme Ayarları profilini geri yüklemek için kullanın `General`.  
  
## <a name="remarks"></a>Açıklamalar  
 Hayır ise `SettingsFile` belirtilirse, sonraki başlatışınızda ayar varsayılan koleksiyonunu seçmek için istenir [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
## <a name="example"></a>Örnek  
 Aşağıdaki komut satırını dosyasında depolanan ayarları uygular `MySettings.vssettings`.  
  
```  
Devenv.exe /ResetSettings "C:\My Files\MySettings.vssettings"  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio'da geliştirme ayarlarını özelleştirme](https://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3)   
 [Devenv Komut Satırı Anahtarları](../../ide/reference/devenv-command-line-switches.md)
