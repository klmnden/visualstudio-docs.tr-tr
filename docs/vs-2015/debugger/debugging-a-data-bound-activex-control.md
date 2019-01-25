---
title: Veri bağımlı ActiveX denetiminde hata ayıklama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- data-bound controls, ActiveX
- ActiveX controls, debugging
- controls [Visual Studio], ActiveX
ms.assetid: 9f6e1f00-e25b-48a9-8484-7e67a1232461
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 45a2f6e022c753b0fe543f2265c7ac1961fd474a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54752925"
---
# <a name="debugging-a-data-bound-activex-control"></a>Veri Bağımlı ActiveX Denetiminde Hata Ayıklama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir veri kaynak denetimine bağımlı bir ActiveX denetimini geliştiriyorsanız kendi kapsayıcı uygulaması oluşturma ve bu kapsayıcı ActiveX denetiminde hata ayıklama için kullanın.  
  
 Örneğin, bir iletişim kutusu tabanlı MFC uygulaması oluşturmak ve verilere bağlı denetim ve iletişim kutusundaki veri kaynağı denetimi yerleştirin. Bu MFC uygulaması, veri bağımlı ActiveX denetiminde hata ayıklama için yürütülebilir kapsayıcısı ve çalışma zamanı test için kullanabilirsiniz.  
  
## <a name="using-the-test-container"></a>Test kapsayıcı'ı kullanma  
 Çeşitli arabirimleri ya da denetimi desteklemek için kolayca değiştirebileceğiniz kapsayıcı ya da kapsayıcı istiyorsanız, ActiveX Test kapsayıcısı hata ayıklama oturumu için yürütülebilir dosya kullanın. ActiveX Test kapsayıcısında tıklayın **seçenekleri** gelen **kapsayıcı** çeşitli arabirimleri etkinleştirmek için menü. Daha fazla bilgi için [Test kapsayıcısı ile test etme özellikleri ve olayları](http://msdn.microsoft.com/library/626867cf-fe53-4c30-8973-55bb93ef3917).  
  
 Hata ayıklarken kapsayıcının kodda ilerleyebilmeniz gerekiyorsa, kapsayıcınızı hata ayıklama sürümünü kullanın veya ActiveX Test kapsayıcısı hata ayıklama sürümünü kullanın. Daha fazla bilgi için [TSTCON örnek: ActiveX denetimi Test kapsayıcısı](http://msdn.microsoft.com/72fa40ef-27d3-400c-813f-10b03236e600).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [COM ve ActiveX hata ayıklaması](../debugger/com-and-activex-debugging.md)   
 [ActiveX Denetimleri](http://msdn.microsoft.com/library/52aaec4d-3889-402e-b57d-758078f8ac57)
