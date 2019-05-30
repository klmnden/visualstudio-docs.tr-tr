---
title: Bir eski dil hizmeti Uygulama1 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- language services, managed
ms.assetid: df638f24-166d-4b80-be82-c9c39ca7a556
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 626838b0e82846f66b817465fca2df353af42dd5
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66315642"
---
# <a name="implementing-a-legacy-language-service"></a>Eski dil hizmetinde uygulama
Söz dizimi vurgulama, ayraç eşleştirme ve IntelliSense tamamlama gibi çok çeşitli özelliklerini destekleyen eski dil hizmeti uygulamak için yönetilen paket çerçevesini (MPF) sınıfları kullanabilirsiniz.

 Eski dil Hizmetleri bir VSPackage'ı bir parçası olarak uygulanır, ancak dil hizmeti özellikleri uygulamak için daha yeni MEF uzantıları kullanmaktır. Dil hizmeti uygulamak için en yeni yolu hakkında daha fazla bilgi için bkz: [düzenleyici ve dil hizmeti uzantıları](../../extensibility/editor-and-language-service-extensions.md).

> [!NOTE]
> Yeni bir düzenleyici API hemen kullanmaya başlamak öneririz. Bu dil hizmetinizin performansını ve yeni düzenleyici özellikleri yararlanmanıza olanak tanır.

## <a name="in-this-section"></a>Bu Bölümde
- [Eski Dil Hizmetine Genel Bakış](../../extensibility/internals/legacy-language-service-overview.md)

 İçinde MPF desteklenen dil hizmeti özelliklerine genel bakış.

- [Eski Dil Hizmeti Uygulama](../../extensibility/internals/implementing-a-legacy-language-service2.md)

 Dil hizmeti MPF uygulamak için gereken açıklar.

- [Eski Dil Hizmeti Kaydetme](../../extensibility/internals/registering-a-legacy-language-service1.md)

 Bir dil MPF tabanlı hizmetiyle kaydetmek için gerekli adımları açıklayan [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

- [Eski Dil Hizmeti Ayrıştırıcısı ve Tarayıcısı](../../extensibility/internals/legacy-language-service-parser-and-scanner.md)

 MPF dil hizmetinin tüm özellikleri uygulamak için gereken iki Çözümleyicileri açıklar.

- [İzlenecek yol: Eski Dil Hizmeti Oluşturma](../../extensibility/internals/walkthrough-creating-a-legacy-language-service.md)

 VSPackage'ı içinde bir MPF dil hizmeti uygulamak için gerekli temel adımlar sağlanmaktadır.

- [İzlenecek yol: Yüklü Kod Parçacıklarının Listesini Alma (Eski Uygulama)](../../extensibility/internals/walkthrough-getting-a-list-of-installed-code-snippets-legacy-implementation.md)

 Yüklü kod parçacıklarının listesini alma teknikleri gösterir.

- [Eski Dil Hizmeti Özellikleri](../../extensibility/internals/legacy-language-service-features1.md)

 Ne MPF dil hizmetinin tüm özellikleri uygulamak için yapılması gereken bu ayrıntılı konulara bağlantılar sağlar.