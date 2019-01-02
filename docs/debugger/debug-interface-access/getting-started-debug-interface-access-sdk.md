---
title: (Hata ayıklama arabirimi Erişim SDK'sı) Başlarken | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- .dbg files
- DBG files
ms.assetid: cb3d040a-2846-40d7-bdbc-8a5beb5dd2f6
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ee77d4b7f8f1073ce638c8933f468b369d772a71
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53961731"
---
# <a name="getting-started-debug-interface-access-sdk"></a>Başlarken (Arabirim Erişimi SDK'sında Hata Ayıklama)
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