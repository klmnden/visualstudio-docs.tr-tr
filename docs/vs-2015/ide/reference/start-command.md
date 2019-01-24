---
title: Başlat komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- debug.start
helpviewer_keywords:
- Start command
- Debug.Start command
ms.assetid: dc4e4aa2-b0ab-4e00-92db-6dc3058ddc21
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f08baa8c27debf6493ca090a2a5e80f02b3da982
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54774461"
---
# <a name="start-command"></a>Başlat Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Başlangıç projesinde hata ayıklamaya başlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Debug.Start [address]  
```  
  
## <a name="arguments"></a>Arguments  
 `address`  
 İsteğe bağlı. Adres, program yürütme bir kesme noktası kaynak kodundaki benzer askıya alır. Bu bağımsız değişken, yalnızca hata ayıklama modunda geçerlidir.  
  
## <a name="remarks"></a>Açıklamalar  
 **Başlat** komut çalıştırıldığında, belirtilen adresi için bir RunToCursor işlemi gerçekleştirir.  
  
## <a name="example"></a>Örnek  
 Bu örnekte, hata ayıklayıcıyı başlatır ve oluşan özel durumları yok sayar.  
  
```  
>Debug.Start  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
