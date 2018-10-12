---
title: Kullanılan değiştirme dizeleri. Pkgdef ve. Pkgundef dosyaları | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Visual Studio shell, isolated mode%2C .pkgdef and .pkgundef files
ms.assetid: b1755d63-d794-4fd7-864b-70a9684881c2
caps.latest.revision: 5
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f679f5c4f817002fa92475a1fba7dc38caa34984
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49175298"
---
# <a name="substitution-strings-used-in-pkgdef-and-pkgundef-files"></a>Kullanılan değiştirme dizeleri. Pkgdef ve. Pkgundef dosyaları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

.Pkgdef aşağıda listelenen değiştirme dizeleri kullanabilirsiniz ve .pkgundef dosyaları, Visual Studio için tanımladığınız yalıtılmış Kabuk uygulaması.  
  
## <a name="substitution-strings"></a>Değiştirme dizeleri  
  
|Dize|Açıklama|  
|------------|-----------------|  
|$=*RegistryEntry*$|Değerini *RegistryEntry* girişi. Kayıt defteri girişi dizesi bir ters eğik çizgiyi sona ererse (\\), kayıt defteri alt anahtarının varsayılan değeri kullanılır. Örneğin, değiştirme dizesi $$, geçerli kullanıcının geçici klasöre genişletilir HKEY_CURRENT_USER\Environment\TEMP =.|  
|$AppName$|AppEnv.dll Giriş noktalarının geçirilen uygulamanın tam adı. Uygulama adı, alt çizgi ve proje .pkgdef dosyasında ThisVersionDTECLSID ayarının değeri olarak kaydedilir uygulama Otomasyon nesnesi sınıfı tanımlayıcısı (CLSID) tam adı oluşur.|  
|$AppDataLocalFolder|Bu uygulama için % LOCALAPPDATA % altındaki alt klasörü.|  
|$BaseInstallDir$|Visual Studio'nın yüklendiği konumun tam yolu.|  
|$CommonFiles$|% CommonProgramFiles % ortam değişkeninin değeri.|  
|$MyDocuments$|Geçerli kullanıcının Belgelerim klasörün tam yolu.|  
|$PackageFolder$|Uygulama için paket derleme dosyalarını içeren dizinin tam yolu.|  
|$ProgramFiles$|% ProgramFiles % ortam değişkeninin değeri.|  
|$RootFolder$|Uygulamanın kök dizininin tam yolu.|  
|$RootKey$|Uygulama kök kayıt defteri anahtarı. Varsayılan olarak HKEY_CURRENT_USER\Software köküdür\\*CompanyName*\\*ProjectName*\\*VersionNumber* (ne zaman "uygulamasını çalıştıran, bu anahtara _Config eklenir). RegistryRoot değer olarak ayarlanmış *SolutionName*.pkgdef dosyası.<br /><br /> $RootKey$ dizesi, bir uygulama alt anahtarı altındaki kayıt defteri değeri almak için kullanılabilir. Örneğin, dize "$$RootKey \AppIcon$ =" uygulama kökü altındaki AppIcon giriş değeri döndürür.<br /><br /> Ayrıştırıcının .pkgdef dosyası sırayla işler ve yalnızca giriş önceden tanımlanmış bir uygulama alt anahtarı altındaki kayıt defteri girişi erişebilirsiniz|  
|$ShellFolder$|Visual Studio'nın yüklendiği konumun tam yolu.|  
|$System$|Windows\system32 klasörüne.|  
|$WINDIR$|Windows klasörü.|  
  
 Ayrıştırıcının değiştirme dizesini tanımadığından veya bir kayıt defteri girişi veya bir ortam değişkeni değeri belirlenemiyor, ardından bu değiştirme dizesi, bir parçası gerçekleştirmez.

