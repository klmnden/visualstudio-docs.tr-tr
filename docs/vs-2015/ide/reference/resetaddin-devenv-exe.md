---
title: -ResetAddin (devenv.exe) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- disable addin
- addin state
- reset addin
ms.assetid: 9e339c8d-d768-4d86-8f45-2f479fc8255b
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 241d97dd7b2b939ff49656e2cef2c93e4cb9b57b
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59656052"
---
# <a name="resetaddin-devenvexe"></a>/ResetAddin (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Komutlar ve komut belirtilen eklenti ilişkili UI kaldırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Devenv /ResetAddin AddIn  
```  
  
## <a name="arguments"></a>Arguments  
 `AddIn`  
 İsteğe bağlı. Eklentinin komut adı.  
  
## <a name="remarks"></a>Açıklamalar  
 Varsayılan olarak, eklentinin komut adı eşittir  *\<AddInSolutionName >*. Connect<em>.\< AddInSolutionName ></em>ve olarak Connect.CS'de görünür `commandName` parametresinin `Exec` yöntemi. Visual Studio'da komutlar penceresine adını yazmaya başlayarak ve geri kalanı doldurmak için IntelliSense kullanarak da komut adını doğrulayabilirsiniz.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, Visual Studio başlatılır ve engeller `MyAddin` başlangıçta çalışan eklentiden.  
  
```  
Devenv.exe /ResetAddin MyAddin.Connect.MyAddin  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio'da geliştirme ayarlarını özelleştirme](http://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3)   
 [Devenv Komut Satırı Anahtarları](../../ide/reference/devenv-command-line-switches.md)
