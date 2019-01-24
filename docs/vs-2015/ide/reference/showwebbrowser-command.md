---
title: ShowWebBrowser komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- view.showwebbrowser
helpviewer_keywords:
- ShowWebBrowser command
- View.ShowWebBrowser command
ms.assetid: c6a4fbd6-8e9d-45cc-8b2f-93990d065e78
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: c1fca2c1c1dde167c8028d6ad4d543e108a488b4
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54798219"
---
# <a name="showwebbrowser-command"></a>ShowWebBrowser Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Tümleşik geliştirme ortamı (IDE) veya IDE dışında içindeki bir Web tarayıcı penceresinde belirttiğiniz URL'yi görüntüler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
View.ShowWebBrowser URL [/new][/ext]  
```  
  
## <a name="arguments"></a>Arguments  
 `URL`  
 Gerekli. Web sitesi için URL (Tekdüzen Kaynak Konum Belirleyicisi).  
  
## <a name="switches"></a>Anahtarlar  
 / Yeni  
 İsteğe bağlı. Sayfayı yeni bir Web tarayıcısı örneğini görüntüleneceğini belirtir.  
  
 /ext  
 İsteğe bağlı. Sayfa IDE dışında varsayılan Web tarayıcısında görüntüleneceğini belirtir.  
  
## <a name="remarks"></a>Açıklamalar  
 Diğer **ShowWebBrowser** komutu **gidin** veya **nav**.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, IDE dışında bir Web tarayıcısında MSDN Online Giriş sayfasında gösterilir. Web tarayıcısının bir örneği zaten açıksa kullanılır; Aksi halde yeni bir örneğini başlattınız.  
  
```  
>View.ShowWebBrowser http://msdn.microsoft.com /ext  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
