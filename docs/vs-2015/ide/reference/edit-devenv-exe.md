---
title: -(Devenv.exe) Düzenle | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- Devenv, /edit switch
- /Edit Devenv swtich
ms.assetid: 02b3d6e7-a2b1-4d83-a747-aa8c2fb758b7
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: c4dabbb0c21fd6b4cabb01655485c8158662adb2
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59667285"
---
# <a name="edit-devenvexe"></a>/Edit (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Mevcut bir örneğini belirtilen dosyayı açar [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Devenv /edit [file1[ file2]]  
```  
  
## <a name="arguments"></a>Arguments  
 `file1`  
 İsteğe bağlı. Mevcut bir örneğini açmak için dosyaya [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]. Hiç bir örneği ise [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] yoksa, yeni bir örneği bir Basitleştirilmiş pencere düzeni ile oluşturulur ve `file1` yeni bir örneğinde açılmış.  
  
 `file2`  
 İsteğe bağlı. Var olan örnekte açmak için bir veya daha fazla ek dosyalar [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
## <a name="remarks"></a>Açıklamalar  
 Hiçbir dosya belirtilir ve var olan bir örneği [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)], var olan örneğinin [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] odağı alır. Hiçbir dosya belirtilir ve mevcut hiçbir örneği [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)], yeni bir örneğini [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] bir Basitleştirilmiş pencere düzeni ile oluşturulur.  
  
 Varsa mevcut örneğini [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] örneğin kalıcı bir durumda olduğundan, [Seçenekler iletişim kutusu](../../ide/reference/options-dialog-box-visual-studio.md) açık dosya olacak mevcut açık örnek [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] kalıcı durumdan çıkar.  
  
## <a name="example"></a>Örnek  
 Bu örnek dosyayı açar `MyFile.cs` var olan bir örneğini [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] veya dosyayı yeni bir örneğini açar [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] biri zaten mevcut değilse.  
  
```  
devenv /edit MyFile.cs  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Devenv Komut Satırı Anahtarları](../../ide/reference/devenv-command-line-switches.md)
