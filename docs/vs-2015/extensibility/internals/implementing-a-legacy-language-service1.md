---
title: Bir eski dil hizmeti Uygulama1 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- language services, managed
ms.assetid: df638f24-166d-4b80-be82-c9c39ca7a556
caps.latest.revision: 19
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: b28db87dafc5ce6f247e49c8a0b765a29faa938c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54782686"
---
# <a name="implementing-a-legacy-language-service"></a>Eski dil hizmetinde uygulama
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Söz dizimi vurgulama, ayraç eşleştirme ve IntelliSense tamamlama gibi çok çeşitli özelliklerini destekleyen eski dil hizmeti uygulamak için yönetilen paket çerçevesini (MPF) sınıfları kullanabilirsiniz.  
  
 Eski dil Hizmetleri bir VSPackage'ı bir parçası olarak uygulanır, ancak dil hizmeti özellikleri uygulamak için daha yeni MEF uzantıları kullanmaktır. Dil hizmeti uygulamak için en yeni yolu hakkında daha fazla bilgi için bkz: [düzenleyici ve dil hizmeti uzantıları](../../extensibility/editor-and-language-service-extensions.md).  
  
> [!NOTE]
>  Yeni bir düzenleyici API hemen kullanmaya başlamak öneririz. Bu dil hizmetinizin performansını ve yeni düzenleyici özellikleri yararlanmanıza olanak tanır.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Eski Dil Hizmetine Genel Bakış](../../extensibility/internals/legacy-language-service-overview.md)  
 İçinde MPF desteklenen dil hizmeti özelliklerine genel bakış.  
  
 [Eski Dil Hizmeti Uygulama](../../extensibility/internals/implementing-a-legacy-language-service2.md)  
 Dil hizmeti MPF uygulamak için gereken açıklar.  
  
 [Eski Dil Hizmeti Kaydetme](../../extensibility/internals/registering-a-legacy-language-service1.md)  
 Bir dil MPF tabanlı hizmetiyle kaydetmek için gerekli adımları açıklayan [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
 [Eski Dil Hizmeti Ayrıştırıcısı ve Tarayıcısı](../../extensibility/internals/legacy-language-service-parser-and-scanner.md)  
 MPF dil hizmetinin tüm özellikleri uygulamak için gereken iki Çözümleyicileri açıklar.  
  
 [İzlenecek yol: Eski dil hizmeti oluşturma](../../extensibility/internals/walkthrough-creating-a-legacy-language-service.md)  
 VSPackage'ı içinde bir MPF dil hizmeti uygulamak için gerekli temel adımlar sağlanmaktadır.  
  
 [İzlenecek yol: (Eski uygulama) yüklü kod parçacıklarının listesini alma](../../extensibility/internals/walkthrough-getting-a-list-of-installed-code-snippets-legacy-implementation.md)  
 Yüklü kod parçacıklarının listesini alma teknikleri gösterir.  
  
 [Eski Dil Hizmeti Özellikleri](../../extensibility/internals/legacy-language-service-features1.md)  
 Ne MPF dil hizmetinin tüm özellikleri uygulamak için yapılması gereken bu ayrıntılı konulara bağlantılar sağlar.
