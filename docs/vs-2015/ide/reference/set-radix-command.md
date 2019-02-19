---
title: Sayı tabanı komut kümesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- debug.setradix
helpviewer_keywords:
- Set Radix command
- Debug.SetRadix command
ms.assetid: 6ffd1554-7530-4da4-b5f5-e276a5034f3b
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: c315ccb0bc7404ddbaa303430644b404a570e016
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54798096"
---
# <a name="set-radix-command"></a>Sayı Tabanını Ayarla Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Tamsayı değerleri görüntülemek için kullanılan sayısal taban döndürür veya ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Debug.SetRadix [10 | 16 | hex | dec]  
```  
  
## <a name="arguments"></a>Arguments  
 `10` veya `16` veya `hex` veya `dec`  
 İsteğe bağlı. Ondalık gösterir (10 veya Ara) ya da onaltılık (16 veya onaltılık). Ardından bir bağımsız değişken yoksayılırsa geçerli taban değeri döndürülür.  
  
## <a name="example"></a>Örnek  
 Bu örnek, tamsayı değerlerini onaltılık biçimde görüntülemek için ortamı ayarlar.  
  
```  
>Debug.SetRadix hex  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
