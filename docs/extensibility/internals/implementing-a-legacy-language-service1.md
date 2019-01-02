---
title: Bir eski dil hizmeti Uygulama1 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- language services, managed
ms.assetid: df638f24-166d-4b80-be82-c9c39ca7a556
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d3218a8cf1c61fb9b88520702a953f2288e19b3c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53855893"
---
# <a name="implementing-a-legacy-language-service"></a>Eski dil hizmetinde uygulama
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
 Bir dil MPF tabanlı hizmetiyle kaydetmek için gerekli adımları açıklayan [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].  
  
 [Eski Dil Hizmeti Ayrıştırıcısı ve Tarayıcısı](../../extensibility/internals/legacy-language-service-parser-and-scanner.md)  
 MPF dil hizmetinin tüm özellikleri uygulamak için gereken iki Çözümleyicileri açıklar.  
  
 [İzlenecek yol: Eski dil hizmeti oluşturma](../../extensibility/internals/walkthrough-creating-a-legacy-language-service.md)  
 VSPackage'ı içinde bir MPF dil hizmeti uygulamak için gerekli temel adımlar sağlanmaktadır.  
  
 [İzlenecek yol: (Eski uygulama) yüklü kod parçacıklarının listesini alma](../../extensibility/internals/walkthrough-getting-a-list-of-installed-code-snippets-legacy-implementation.md)  
 Yüklü kod parçacıklarının listesini alma teknikleri gösterir.  
  
 [Eski Dil Hizmeti Özellikleri](../../extensibility/internals/legacy-language-service-features1.md)  
 Ne MPF dil hizmetinin tüm özellikleri uygulamak için yapılması gereken bu ayrıntılı konulara bağlantılar sağlar.