---
title: Açık proje komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- file.openproject
helpviewer_keywords:
- op command
- File.OpenProject command
- Open Project command
ms.assetid: baa85f86-041b-49f4-9ced-0c397dc180e1
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 916ea8435571efc01f38e408d4fc2d4563c16f1c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54753491"
---
# <a name="open-project-command"></a>Proje Aç Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Varolan projeyi açar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
File.OpenProject filename  
```  
  
## <a name="arguments"></a>Arguments  
 `filename`  
 Gerekli. Tam yol ve dosya adını projenizi açın.  
  
 Sözdizimi `filename` bağımsız değişken gerektiriyor boşluk içeren yolları tırnak işaretleri kullanın.  
  
## <a name="remarks"></a>Açıklamalar  
 Otomatik Tamamlama, doğru yol ve dosya adı, türü bulmaya çalışır.  
  
 Bu komut hata ayıklama sırasında kullanılamaz.  
  
## <a name="example"></a>Örnek  
 Bu örnek açılır [!INCLUDE[vbprvb](../../includes/vbprvb-md.md)] Test1 proje.  
  
```  
>File.OpenProject "C:\My Projects\Test1\Test1.vbproj"  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
