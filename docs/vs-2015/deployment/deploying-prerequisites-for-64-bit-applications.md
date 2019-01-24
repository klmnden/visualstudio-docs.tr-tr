---
title: 64-bit uygulamalar için önkoşulları dağıtma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- deploying applications [Visual Studio], 64-bit
- 64-bit [Visual Studio]
- 64-bit programming [Visual Studio]
- 64-bit applications [Visual Studio]
ms.assetid: 87399e20-5510-41e4-b5b7-4a87c5773f21
caps.latest.revision: 25
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 3f416a22bc7cbdd374622c89a1826ebff8af9450
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54775384"
---
# <a name="deploying-prerequisites-for-64-bit-applications"></a>64 bit Uygulamalar için Önkoşulları Dağıtma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

ClickOnce dağıtımı, 64-bit platformlarda uygulamaların yüklenmesini destekler. Hedef platformlar **x86** 32-bit platformları için **x64** AMD64 ve EM64T komut kümelerini destekleyen makineler için ve **Itanium** 64-bit Itanium işlemcisi için.  
  
## <a name="prerequisites"></a>Önkoşullar  
 Aşağıdaki tabloda, 64-bit uygulamanızın kurulum için önkoşul olarak kullanabileceğiniz yeniden dağıtılabilir dosyaları listeler.  
  
 64-bit bileşen yok. bir önkoşul seçerseniz, seçilen paketleri 64-bit platformu için kullanılabilir olmadığını belirten bir uyarı görebilirsiniz.  
  
|Yeniden dağıtılabilir|x64 desteği|IA64 desteği|  
|---------------------|-----------------|------------------|  
|[!INCLUDE[vsto_runtime](../includes/vsto-runtime-md.md)]|Evet|Hayır|  
|Visual C++ 2010 Çalışma zamanı kitaplıkları (IA64)|Hayır|Evet|  
|Visual C++ 2010 Çalışma zamanı kitaplıkları (x64)|Evet|Hayır|  
|Microsoft .NET Framework 4 (x86 ve x64)|Evet||  
|Microsoft .NET Framework 4 istemci profili (x86 ve x64)|Evet||  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uygulamaları, hizmetleri ve bileşenleri dağıtma](../deployment/deploying-applications-services-and-components.md)   
 [Nasıl yapılır: ClickOnce uygulamasıyla Önkoşulları Yükleme](../deployment/how-to-install-prerequisites-with-a-clickonce-application.md)   
 [64 bit Uygulamalar](http://msdn.microsoft.com/library/fd4026bc-2c3d-4b27-86dc-ec5e96018181)
