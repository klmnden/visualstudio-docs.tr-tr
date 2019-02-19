---
title: Varolan projeyi Ekle komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- file.addexistingproject
helpviewer_keywords:
- Add Existing Project command
- File.AddExistingProject
ms.assetid: 71cf3e31-c76b-405b-ad6a-1b1bc654bd40
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 7523db6598a32c76944c22bfdabe56ee288c6b43
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54771088"
---
# <a name="add-existing-project-command"></a>Varolan Projeyi Ekle Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Mevcut bir projeyi çözüme ekler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
File.AddExistingProject filename  
```  
  
## <a name="arguments"></a>Arguments  
 `filename`  
 İsteğe bağlı. Tam yol ve proje adı, çözüme eklemek için projenin bir uzantıya sahip.  
  
 Varsa `filename` bağımsız değişken boşluk içeriyorsa, tırnak işaretleri içine alınmalıdır.  
  
 Dosya adı belirtilirse, bu kullanıcı, bir proje seçebilir böylece komut dosya iletişim kutusu açılır.  
  
## <a name="remarks"></a>Açıklamalar  
 Otomatik Tamamlama, doğru yol ve dosya adı, türü bulmaya çalışır.  
  
## <a name="example"></a>Örnek  
 Bu örnek ekler [!INCLUDE[vbprvb](../../includes/vbprvb-md.md)] proje, TestProject1, geçerli çözüme.  
  
```  
>File.AddExistingProject "c:\visual studio projects\TestProject1.vbproj"  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
