---
title: Git komut | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- edit.goto
helpviewer_keywords:
- Debug.Goto command
- Go To command
ms.assetid: 201e1dd2-6701-467d-8cc1-faec2ef20511
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 50f91c4bdb17612d56534290a7b83b7df1d771c9
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54790026"
---
# <a name="go-to-command"></a>Git Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
İmleci belirtilen satıra taşır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Edit.GoTo [linenumber]  
```  
  
## <a name="arguments"></a>Arguments  
 `linenumber`  
 İsteğe bağlı. Gitmek için satır sayısını temsil eden bir tamsayı.  
  
## <a name="remarks"></a>Açıklamalar  
 Satır numaraları tek başlar. Varsa değerini `linenumber` değerden daha az, ilk satır görüntüler. Varsa değerini `linenumber` son satırın son satır görüntüler sayısından büyüktür.  
  
 İçin bir değer `linenumber` belirtilmezse, **satıra Git** iletişim kutusu görüntüler.  
  
 Bu komut diğer GoToLn adıdır.  
  
## <a name="example"></a>Örnek  
  
```  
>Edit.GoTo 125  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
