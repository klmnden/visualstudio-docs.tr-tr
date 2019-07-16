---
title: Kesme noktası komutu Değiştir | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- debug.togglebreakpoint
helpviewer_keywords:
- ToggleBreakpoint command
- Debug.ToggleBreakPoint command
- Toggle Breakpoint command
ms.assetid: d50dfadb-ce79-4d5e-9c09-1cfddd57876d
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 5a57f02a7c1b9845f4248daf2282b6f285f95489
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68193367"
---
# <a name="toggle-breakpoint-command"></a>Kesim Noktasını Değiştir Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Dosyadaki geçerli konumda geçerli durumuna bağlı olarak kesme noktasını açar veya devre dışı bırakır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Debug.ToggleBreakpoint [text]  
```  
  
## <a name="arguments"></a>Arguments  
 `text`  
 İsteğe bağlı. Metin belirtilmezse, satır adlandırılmış bir kesme noktası işaretlenir. Aksi takdirde, satır F9 tuşuna bastığınızda ne olacağını için benzer olan adlandırılmamış bir kesme noktası işaretlenir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek geçerli kesme noktasını açar veya kapatır.  
  
```  
>Debug.ToggleBreakpoint  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
