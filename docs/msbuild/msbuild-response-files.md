---
title: MSBuild yanıt dosyaları | Microsoft Docs
ms.date: 11/04/2016
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
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 33156a0614ad47839187056e4e0a24b5ee2f7ae2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53989678"
---
# <a name="msbuild-response-files"></a>MSBuild yanıt dosyaları
Yanıt (*.rsp*) dosyalar içeren metin dosyalarını *MSBuild.exe* komut satırı anahtarları. Her anahtar ayrı bir satıra olabilir veya tek bir satırda tüm anahtarlar olabilir. Yorum Satırları ile giriş yapılmış bir **#** simgesi. **@** Başka bir yanıt dosyasına aktarmak için kullanılan anahtar *MSBuild.exe*.  
  
## <a name="msbuildrsp"></a>MSBuild.rsp
Özel bir autoresponse dosyasıdır *.rsp* dosya *MSBuild.exe* otomatik olarak bir proje derlenirken kullanır. Bu dosya *MSBuild.rsp*, aynı dizinde olmalıdır *MSBuild.exe*, aksi takdirde, bulunamayacaktır. Varsayılan komut satırı anahtarları için belirtmek için bu dosyayı düzenleyebilirsiniz *MSBuild.exe*. Örneğin, aynı Günlükçü kullanıyorsanız, bir projeyi her derlediğinizde, ekleyebileceğiniz **-Günlükçü** geçin *MSBuild.rsp*, ve *MSBuild.exe* Günlükçü her zaman kullanacağı bir Proje oluşturulur. 

## <a name="directorybuildrsp"></a>Directory.Build.rsp
Sürüm 15.6 ve üzeri MSBuild adlı bir dosya için projenin üst dizininde arar *Directory.Build.rsp*.  Bu, varsayılan bağımsız değişkenleri komut satırı derlemeleri sırasında sağlamak için kaynak kodu deposu yardımcı olabilir.  Ayrıca, barındırılan derlemeler komut satırı bağımsız değişkenlerini belirtmek için de kullanılabilir. 

## <a name="see-also"></a>Ayrıca bkz.  
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)   
 [Komut satırı başvurusu](../msbuild/msbuild-command-line-reference.md)