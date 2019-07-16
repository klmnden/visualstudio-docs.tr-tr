---
title: MSBuild yanıt dosyaları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- response files, MSBuild
- MSBuild, response files
- MSBuild, .rsp files
- .rsp files
ms.assetid: 9f53987b-20ee-470a-ab62-fce997bb5e15
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a1ce11edac37368b9c4993a87a8c2b3e734b7862
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68189370"
---
# <a name="msbuild-response-files"></a>MSBuild Yanıt Dosyaları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yanıt (.rsp), MSBuild.exe komut satırı anahtarları içeren metin dosyalarını dosyalarıdır. Her anahtar ayrı bir satıra olabilir veya tek bir satırda tüm anahtarlar olabilir. Yorum Satırları ile giriş yapılmış bir **#** simgesi. **@** Başka bir yanıt dosyası MSBuild.exe'ye geçirilecek anahtar kullanılır.  
  
 Otomatik yanıt dosyası bir proje derlenirken MSBuild.exe kullanan bir özel .rsp dosyasıdır. Bu dosya, MSBuild.rsp, MSBuild.exe ile aynı dizinde olmalıdır, aksi takdirde, bulunmaz. Varsayılan komut satırında MSBuild.exe geçer belirtmek için bu dosyayı düzenleyebilirsiniz. Örneğin, aynı Günlükçü kullanıyorsanız, bir projeyi her derlediğinizde, ekleyebileceğiniz **/logger** geçiş için MSBuild.rsp ve bir proje her zaman MSBuild.exe Günlükçü kullanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)   
 [Komut Satırı Başvurusu](../msbuild/msbuild-command-line-reference.md)
