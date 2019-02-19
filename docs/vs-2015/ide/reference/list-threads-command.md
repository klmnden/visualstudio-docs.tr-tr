---
title: Liste komut iş parçacıkları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- debug.listthreads
helpviewer_keywords:
- ListThreads command
- list threads command
- Debug.ListThreads command
ms.assetid: 34b665c0-d46f-4c1a-a066-b678eba5ac54
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 627e361fca63522f47a1d472655573c14a44035a
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54804614"
---
# <a name="list-threads-command"></a>İş Parçacıklarını Listele Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Geçerli programdaki iş parçacıklarının listesini görüntüler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Debug.ListThreads [index]  
```  
  
## <a name="arguments"></a>Arguments  
 `index`  
 İsteğe bağlı. Bir iş parçacığı geçerli iş parçacığı olarak dizine göre seçer.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu seçenek belirtildiğinde, `index` bağımsız değişkeni, belirtilen iş parçacığı geçerli iş parçacığı olarak işaretler. Bir yıldız işareti (*), geçerli iş parçacığı yanındaki listede görüntülenir.  
  
## <a name="example"></a>Örnek  
  
```  
>Debug.ListThreads   
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çağrı yığınını Listele komutu](../../ide/reference/list-call-stack-command.md)   
 [Ayrıştırılmış kodu Listele komutu](../../ide/reference/list-disassembly-command.md)   
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
