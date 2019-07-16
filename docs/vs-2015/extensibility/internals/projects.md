---
title: Projeleri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- solutions [Visual Studio]
- custom tools [Visual Studio SDK]
- project subtypes [Visual Studio SDK]
- projects [Visual Studio SDK]
- project types [Visual Studio SDK]
ms.assetid: 237742e4-a638-4d5b-a9b3-6a69d627763c
caps.latest.revision: 44
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: a251af12ccf4be5f0f48f789ac59fedaed3299b0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68183944"
---
# <a name="projects"></a>Projeler
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Visual Studio'da projeler kaynak kodu dosyaları ve görüntülenen diğer kaynakları düzenlemek için geliştiricilerin kullanan kapsayıcılardır **Çözüm Gezgini**. Genellikle depolama başvurularının kaynak kod dosyalarını ve kaynak bit eşlem dosyaları gibi dosyalar (örneğin, bir C# projesi için .csproj dosyası) projelerdir. Düzenleme, derleme, hata ayıklama ve kaynak kodunu Dağıt let projeleri, Web Hizmetleri ve veritabanları ve diğer kaynaklara başvuruyor. VSPackage'ları, Visual Studio Proje sistemi üç temel şekilde genişletebilir: *proje türleri*, *proje alt türleri*, ve *özel Araçlar*.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Proje Türleri](../../extensibility/internals/project-types.md)  
 *Proje türleri* programlama gibi projeler, yeni türleri için destek eklendi. Örneğin, Visual Studio'nun desteklediği her bir dilin kendi proje türünde ve IronPython dil için bir proje türü IronPython tümleştirme örneği içerir. C# veya Visual Basic nasıl öğeler yerleşik, hata ayıklama, dağıtılan ve görüntülenen özelleştirmek için dışındaki diller için bir proje türü oluşturmalısınız **Çözüm Gezgini**. Daha fazla bilgi için [proje türleri](../../extensibility/internals/project-types.md).  
  
 [Proje Alt Türleri](../../extensibility/internals/project-subtypes.md)  
 *Proje alt türleri* proje türlerine dayanmaktadır ve projeleri yerleşik, hata ayıklama ve dağıtılan biçimini özelleştirmek için kullanılabilir. Visual Studio Proje alt türleri ile akıllı cihaz projeleri kullanır; Bunlar, yeni oluşturulan bir program geliştirme bilgisayarınızdan hedef cihaza kopyalayarak dağıtımı özelleştirin. C# ve Visual Basic proje türleri için proje alt türleri temeli olarak kullanılabilir; C++ proje türleri olamaz. Kendi proje türleri için temel olarak proje alt türleri için de kullanılabilir. Daha fazla bilgi için [proje alt türleri](../../extensibility/internals/project-subtypes.md).  
  
 [Web Projeleri](../../extensibility/internals/web-projects.md)  
 Hangi sırayla Web uygulamaları oluşturmak ve Web projesi açıklar.  
  
 [Yeni Proje Oluşturma: Bir altyapı öğeleri, bölüm](../../extensibility/internals/new-project-generation-under-the-hood-part-one.md) ve [yeni proje oluşturma: Arka Plan, 2. Bölüm](../../extensibility/internals/new-project-generation-under-the-hood-part-two.md)  
 Yeni bir proje oluşturduğunuzda, aslında neler olduğunu açıklar.  
  
 [VSSDK örnekleri](../../misc/vssdk-samples.md)  
 Projeler ve çözümler ile uğraşmak VSSDK örneklerinde açıklar.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Visual Studio SDK’nın İçinde](../../extensibility/internals/inside-the-visual-studio-sdk.md)  
 Visual Studio genişletilebilirlik farklı yönlerini açıklar.
