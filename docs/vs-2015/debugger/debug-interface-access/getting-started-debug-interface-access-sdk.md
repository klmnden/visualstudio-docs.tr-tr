---
title: (Hata ayıklama arabirimi Erişim SDK'sı) Başlarken | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- .dbg files
- DBG files
ms.assetid: cb3d040a-2846-40d7-bdbc-8a5beb5dd2f6
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 54f83f00ed2e99d1541e15092cb3ee0ce9e08952
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54759304"
---
# <a name="getting-started-debug-interface-access-sdk"></a>Başlarken (Arabirim Erişimi SDK'sında Hata Ayıklama)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklama arabirimi erişim (DIA) SDK'sı yönerge belgeleri ile DIA API'SİNİN nasıl kullanılacağı gösterilmektedir. bir örnek sağlar. Arabirimler ve yöntemler, .pdb ve .dbg dosyaları açmak ve içeriklerini sembolleri, değerleri, öznitelikler, adresleri ve diğer hata ayıklama bilgileri için arama özel uygulamalar geliştirmek için DIA SDK'yı kullanın. Bu SDK, C++ uygulamalarında bulunan simgeler ile ilişkili özellikler için başvuru tabloları da sağlar.  
  
 DIA SDK en iyi şekilde kullanmak için aşağıdakilerle ilgili bilgi sahibi olması gerekir:  
  
- C++ programlama dili  
  
- COM programlama  
  
- Örnekleri derlemek için visual Studio tümleşik geliştirme ortamı (IDE)  
  
  DIA SDK normalde Visual Studio ile yüklenir ve varsayılan konumu *[sürücü]* \Program Visual Studio 9.0\DIA SDK. Dahil etmek için bunu kullanmak için yapmanız gereken tek şey şekilde yüklemesinin bir parçası olarak DIA SDK uygulayan msdia90.dll otomatik olarak kaydedilir `dia2.h` program ve bağlantı `diaguids.lib`.  
  
  Üstbilgi: include\dia2.h  
  
  Kitaplık: lib\diaguids.lib  
  
  DLL: bin\msdia80.dll  
  
  IDL: idl\dia2.idl  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Genel bakış](../../debugger/debug-interface-access/overview-debug-interface-access-sdk.md)  
 DIA. temel mimarisini gözden geçirmeleri  
  
 [.Pdb Dosyasını Sorgulama](../../debugger/debug-interface-access/querying-the-dot-pdb-file.md)  
 .Pdb dosyasını sorgulama DIA API'yi kullanmak adım adım yönergeler sağlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Arabirim Erişimi SDK'sında Hata Ayıklama](../../debugger/debug-interface-access/debug-interface-access-sdk.md)
