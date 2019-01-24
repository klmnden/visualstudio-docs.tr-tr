---
title: .NET Framework uzantılarını kaydetme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
helpviewer_keywords:
- Add References dialog box, registering extensions of the .NET Framework
- MSBuild, registering extensions of the .NET Framework
- .NET Framework extensions, registering
ms.assetid: deee6f53-ea87-4b88-a120-bea589822e03
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 18df04fc706ea716f7c22baa6508930f0f94a6f6
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54801472"
---
# <a name="registering-extensions-of-the-net-framework"></a>.NET Framework Uzantılarını Kaydetme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Belirli bir .NET Framework sürümünü genişleten bir derleme geliştirebilirsiniz. Visual Studio'da görüntülenecek derleme etkinleştirmek için **Add References** iletişim kutusu, sistem kayıt defterine içeren klasöre eklemeniz gerekir.  
  
 Örneğin, Trey Research şirket .NET Framework 4 genişletir ve Kütüphane derlemelerini görünmesini istediği bir kitaplığı geliştirmiştir varsayın **Add References** iletişim kutusuna bir proje .NET Framework 4 hedefliyor. Ayrıca derlemelerin 32 bit bilgisayar veya 64 bit bilgisayarda çalışan 64-bit derlemeler üzerinde çalışan 32 bit derlemeleri olduğundan ve bunların C:\TreyResearch\Extensions4\ klasörüne yükleneceğini varsayılır.  
  
 Bu klasör, bu anahtarı kullanarak kaydedin: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\\.NETFramework\v4.0.21006\AssemblyFoldersEx\TreyResearch\\. Anahtar, bu varsayılan değeri verin: C:\TreyResearch\Extensions4.  
  
> [!NOTE]
>  .NET Framework sürümünün derleme numarası farklı olabilir.  
  
 Bir 64 bit bilgisayarda 32 bit derleme kaydedilecek Wow6432 düğümü, örneğin kullanın: HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\\.NETFramework\v4.0.21006\AssemblyFoldersEx\TreyResearch\\.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Tümleştirmesi](../msbuild/visual-studio-integration-msbuild.md)
