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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c3777be5701e9876352db41a5454d5e12668f6f1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54932123"
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