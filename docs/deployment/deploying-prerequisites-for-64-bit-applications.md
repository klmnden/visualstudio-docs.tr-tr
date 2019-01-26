---
title: 64-bit uygulamalar için önkoşulları dağıtma | Microsoft Docs
ms.date: 11/04/2016
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
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6aab5fb7487cc2e79bc2e0e1a7a5dffce96447f9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55024558"
---
# <a name="deploy-prerequisites-for-64-bit-applications"></a>64-bit uygulamalar için önkoşulları dağıtma
ClickOnce dağıtımı, 64-bit platformlarda uygulamaların yüklenmesini destekler. Hedef platformlar **x86** 32-bit platformları için **x64** AMD64 ve EM64T komut kümelerini destekleyen makineler için ve **Itanium** 64-bit Itanium işlemcisi için.  

## <a name="prerequisites"></a>Önkoşullar  
 Aşağıdaki tabloda, 64-bit uygulamanızın kurulum için önkoşul olarak kullanabileceğiniz yeniden dağıtılabilir dosyaları listeler.  

 64-bit bileşen yok. bir önkoşul seçerseniz, seçilen paketleri 64-bit platformu için kullanılabilir olmadığını belirten bir uyarı görebilirsiniz.  


| Yeniden dağıtılabilir | x64 desteği | IA64 desteği |
| - |-------------|--------------|
| [!INCLUDE[vsto_runtime](../deployment/includes/vsto_runtime_md.md)] | Evet | Hayır |
| Visual C++ 2010 Çalışma zamanı kitaplıkları (IA64) | Hayır | Evet |
| Visual C++ 2010 Çalışma zamanı kitaplıkları (x64) | Evet | Hayır |
| Microsoft .NET Framework 4 (x86 ve x64) | Evet | |
| Microsoft .NET Framework 4 istemci profili (x86 ve x64) | Evet | |

## <a name="see-also"></a>Ayrıca bkz.  
 [Uygulamaları, hizmetleri ve bileşenleri dağıtma](../deployment/deploying-applications-services-and-components.md)   
 [Nasıl yapılır: ClickOnce uygulamasıyla Önkoşulları Yükleme](../deployment/how-to-install-prerequisites-with-a-clickonce-application.md)   
 [64-bit uygulamalar](/dotnet/framework/64-bit-apps)