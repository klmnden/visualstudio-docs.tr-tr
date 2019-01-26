---
title: Hata ayıklama Visual c++ özelliklerini etkinleştirme (-D_DEBUG) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- /D_DEBUG compiler option [C++]
- debugging [C++], enabling debug features
- debugging [MFC], enabling debug features
- assertions, enabling debug features
- D_DEBUG compiler option
- MFC libraries, debug version
- debug builds, MFC
- _DEBUG macro
ms.assetid: 276e2254-7274-435e-ba4d-67fcef4f33bc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 2c18dfec1f6d1581f926fa24d006b3761c2f6fce
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54976254"
---
# <a name="enabling-debug-features-in-visual-c-ddebug"></a>Visual C++'de Hata Ayıklama Özelliklerini Etkinleştirme (/D_DEBUG)
İçinde [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)], programınızı sembolü ile derleme yaparken onaylar etkinleştirilen gibi hata ayıklama özellikleri **_DEBUG** tanımlı. Tanımlayabileceğiniz **_DEBUG** iki yoldan biriyle:  
  
- Belirtin **#define _DEBUG** , kaynak kodunuzdaki veya  
  
- Belirtin **/D_DEBUG** derleyici seçeneği. (Proje sihirbazları kullanarak Visual Studio'da oluşturursanız **/D_DEBUG** hata ayıklama yapılandırmasında otomatik olarak tanımlanır.)  
  
  Zaman **_DEBUG** olan tanımlanan, derleyici tarafından çevrelenen kod bölümlerini derler **#ifdef _DEBUG** ve `#endif`.  
  
  MFC programı hata ayıklama yapılandırmasını MFC Kitaplığı hata ayıklama sürümü ile bağlanması gerekir. MFC üstbilgi dosyalarındaki doğru MFC kitaplığı ile bağlantı için tanımladığınız, gibi semboller üzerinde temel sürümünü **_DEBUG** ve **_UNICODE**. Ayrıntılar için bkz [MFC kitaplık sürümleri](/cpp/mfc/mfc-library-versions).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yerel kodda hata ayıklama](../debugger/debugging-native-code.md)   
 [C++ Hata Ayıklama Yapılandırması Proje Ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md)