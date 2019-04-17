---
title: Geçerli işlemi Ayarla | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- Debug.SetCurrentProcess command
- Set Current Process command
ms.assetid: 1e016ebd-aadd-411f-a606-03bf69d3f8aa
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: ed19c5b95351f8e9c34255a915fc6a446800f761
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59669946"
---
# <a name="set-current-process"></a>Geçerli Süreci Ayarla
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Belirtilen işlemi Hata ayıklayıcıdaki etkin işlem olarak ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Debug.SetCurrentProcess index  
```  
  
## <a name="arguments"></a>Arguments  
 `index`  
 Gerekli. İşlem dizini.  
  
## <a name="remarks"></a>Açıklamalar  
 Hata ayıklama, ancak yalnızca bir işlem dublajcı içerisinde belirli bir zamanda birden çok işleme iliştirebilirsiniz. Kullanabileceğiniz `SetCurrentProcess` etkin işlemi ayarlamak için komutu.  
  
## <a name="example"></a>Örnek  
  
```  
>Debug.SetCurrentProcess 1  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
