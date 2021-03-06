---
title: İçeri ve dışarı aktarma ayarları komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- Tools.ImportandExportSettings
helpviewer_keywords:
- Tools.ImportandExportSettings
- Import and Export Settings command
ms.assetid: 94a06468-a44d-403d-a931-77bbc9d06e56
caps.latest.revision: 12
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 91b34183e36c86290c14e3da7d17687d45cfe180
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65694653"
---
# <a name="import-and-export-settings-command"></a>Ayarları İçeri ve Dışarı Aktar Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Alır, dışa aktarır veya sıfırlar [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] ayarları.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Tools.ImportandExportSettings [/export:filename | /import:filename | /reset]  
```  
  
## <a name="switches"></a>Anahtarlar  
 / Export:`filename`  
 İsteğe bağlı. Geçerli ayarları, belirtilen dosyaya dışarı aktarır.  
  
 / import:`filename`  
 İsteğe bağlı. Belirtilen dosyasındaki ayarlar içeri aktarır.  
  
 Reset  
 İsteğe bağlı. Geçerli ayarları sıfırlar.  
  
## <a name="remarks"></a>Açıklamalar  
 Açılır anahtarları olmadan bu komutu çalıştırmak **içeri ve dışarı aktarma ayarları** Sihirbazı. Daha fazla bilgi için [nasıl yapılır: Paylaşım ayarları bilgisayarlar veya Visual Studio sürümleri arasında](https://msdn.microsoft.com/1131fb10-35c1-42da-9cd8-91aa3235b882).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki komut, geçerli ayarları dosyasına aktarır. `MyFile.vssettings`.  
  
```  
Tools.ImportandExportSettings /export:"c:\Files\MyFile.vssettings"  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio'da geliştirme ayarlarını özelleştirme](https://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3)   
 [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
