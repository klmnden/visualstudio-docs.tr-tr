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
ms.openlocfilehash: 7c70b58577f8aa6e391215658afb7f8fa43c9bb5
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59666760"
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
- [Uygulamaları, hizmetleri ve bileşenleri dağıtma](../deployment/deploying-applications-services-and-components.md)
- [Nasıl yapılır: ClickOnce uygulamasıyla Önkoşulları Yükleme](../deployment/how-to-install-prerequisites-with-a-clickonce-application.md)
- [64-bit uygulamalar](/dotnet/framework/64-bit-apps)