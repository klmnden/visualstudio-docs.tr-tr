---
title: .NET Framework uzantılarını kaydetme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Add References dialog box, registering extensions of the .NET Framework
- MSBuild, registering extensions of the .NET Framework
- .NET Framework extensions, registering
ms.assetid: deee6f53-ea87-4b88-a120-bea589822e03
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: f1e780a67ee419a8cae661570802e5d85081f1fd
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63445800"
---
# <a name="register-extensions-of-the-net-framework"></a>.NET Framework uzantılarını kaydetme
Belirli bir .NET Framework sürümünü genişleten bir derleme geliştirebilirsiniz. Visual Studio'da görüntülenecek derleme etkinleştirmek için **Add References** iletişim kutusu, sistem kayıt defterine içeren klasöre eklemeniz gerekir.

 Örneğin, Trey Research şirket .NET Framework 4 genişletir ve Kütüphane derlemelerini görünmesini istediği bir kitaplığı geliştirmiştir varsayın **Add References** iletişim kutusuna bir proje .NET Framework 4 hedefliyor. Derlemeleri veya bir 64 bit bilgisayarda çalışan 64 bit derlemelerin 32-bit bilgisayarda çalışan 32 bit derlemeleri olduğunu ve bunlar içinde yüklenecek hızında *C:\TreyResearch\Extensions4\\*  klasör.

 Bu klasör, bu anahtarı kullanarak kaydedin: **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\\.NETFramework\v4.0.21006\AssemblyFoldersEx\TreyResearch\\**. Anahtar, bu varsayılan değeri verin: **C:\TreyResearch\Extensions4**.

> [!NOTE]
> .NET Framework sürümünün derleme numarası farklı olabilir.

 Bir 64 bit bilgisayarda 32 bit derleme kaydedilecek Wow6432 düğümü, örneğin kullanın: **HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\\.NETFramework\v4.0.21006\AssemblyFoldersEx\TreyResearch\\**.

### <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio tümleştirmesi](../msbuild/visual-studio-integration-msbuild.md)