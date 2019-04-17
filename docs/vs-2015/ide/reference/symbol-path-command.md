---
title: Sembol yolu komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- debug.symbolpath
helpviewer_keywords:
- symbol path command
- Debug.SymbolPath command
- SymbolPath command
ms.assetid: b697ef2d-3f5d-40df-b113-7068a5bec0d4
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 27c4c8ac23e2524245107d9052642350e9db09d2
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59670409"
---
# <a name="symbol-path-command"></a>Sembol Yolu Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklayıcının simge araması dizinler listesini ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Debug.SymbolPath pathname1;pathname2;... pathnameN  
```  
  
## <a name="arguments"></a>Arguments  
 `pathname`  
 İsteğe bağlı. Noktalı virgül hata ayıklayıcının simge araması yolları bir listesidir.  
  
## <a name="remarks"></a>Açıklamalar  
 Hayır ise `pathname` belirtilirse, komut geçerli simge yollarını listeler.  
  
## <a name="example"></a>Örnek  
 Bu örnek simge dizinleri listesine iki yol ekler.  
  
```  
Debug.SymbolPath C:\Symbol Path 1;C:\Symbol Path 2  
```  
  
## <a name="example"></a>Örnek  
 Bu örnek, geçerli simge yollarının noktalı virgülle ayrılmış bir liste görüntüler.  
  
```  
Debug.SymbolPath  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
