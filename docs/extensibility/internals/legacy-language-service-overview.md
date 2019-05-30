---
title: Eski dil hizmetine genel bakış | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- language services [managed package framework], about language services
ms.assetid: bb44e27b-d228-463c-b2cf-cd5c24c7c1b5
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: dcc7fa218d5ee4ba92af5ad8316f95ceb268bdf6
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66344901"
---
# <a name="legacy-language-service-overview"></a>Eski Dil Hizmetine Genel Bakış
Dil hizmeti belirli uygulamanıza olanak tanıyan Düzenleyicisi desteği sağlar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] özellikleri. Yönetilen paket Framework (MPF) dil hizmet sınıflarını, sık kullanılan özellikleri ve diğer özellikler için kısmi destek için tam destek sağlar.

## <a name="fully-supported-features-in-the-mpf"></a>MPF tam olarak desteklenen özellikler
 MPF dil hizmeti sınıfları aşağıdaki özellikleri destekler:

- Söz dizimi vurgulama

- Anahat Oluşturma

- Kod blokları açıklama

- Ayraç eşleştirme

- Kod parçacıkları

- Özel belge özellikleri

- IntelliSense parametre bilgileri

- IntelliSense hızlı bilgi

- IntelliSense üye tamamlama

- IntelliSense Sözcük tamamlama

## <a name="partially-supported-features-in-the-mpf"></a>MPF kısmen desteklenen özellikler
 MPF yalnızca kısmi desteği için aşağıdaki özellikleri sağlar. Başka bir deyişle, MPF tarafından çağrılan yöntemlere uygulamalıdır.

- Kodu yeniden biçimlendirme. Siz biçimlendirme uygulayan kod sağlayın.

- Geçerli kod tanımlayarak kesme noktalarını doğrulama yayılır. Siz kodu yayılma tanımlayan kodu sağlayın.

- Hata ayıklayıcı destekleyen **Otolar** değişkenleri görüntüleme penceresi. Siz ne pencerede göstermek belirleyen kod sağlayın.

- Destek **gezinti çubuğu** türler ve üyeler arasında hızlı gezinme için. Uygulama ve listelerinde dolduran bir yardımcı sınıfı döndüren **gezinti çubuğu** birleşik giriş kutuları.

## <a name="implementation"></a>Uygulama
 Dil hizmeti ve dilinizi desteklemek istediğiniz dil hizmeti özellikleri uygulamak için bazı adımları tamamlamanız gerekir. Bu adımlar aşağıdaki konularda ele alınmıştır:

- [Eski Dil Hizmeti Uygulama](../../extensibility/internals/implementing-a-legacy-language-service2.md)

- [Eski Dil Hizmeti Kaydetme](../../extensibility/internals/registering-a-legacy-language-service1.md)

- [Eski Dil Hizmetinde Söz Dizimi Renklendirmesi](../../extensibility/internals/syntax-colorizing-in-a-legacy-language-service.md)

- [Eski Dil Hizmetinde Ayraç Eşleştirme](../../extensibility/internals/brace-matching-in-a-legacy-language-service.md)

- [Eski Dil Hizmetinde Ana Hat Oluşturma](../../extensibility/internals/outlining-in-a-legacy-language-service.md)

- [Eski Dil Hizmetinde Koda Açıklama Ekleme](../../extensibility/internals/commenting-code-in-a-legacy-language-service.md)

- [Eski Dil Hizmetinde Kodu Yeniden Biçimlendirme](../../extensibility/internals/reformatting-code-in-a-legacy-language-service.md)

- [Eski Dil Hizmetinde Özel Belge Özellikleri](../../extensibility/internals/custom-document-properties-in-a-legacy-language-service.md)

- [Eski Dil Hizmetinde Kod Parçacıkları için Destek](../../extensibility/internals/support-for-code-snippets-in-a-legacy-language-service.md)

- [Eski Dil Hizmetinde Otomatik Değişkenler Penceresi için Destek](../../extensibility/internals/support-for-the-navigation-bar-in-a-legacy-language-service.md)

- [Eski Dil Hizmetinde Sözcük Tamamlama](../../extensibility/internals/word-completion-in-a-legacy-language-service.md)

- [Eski Dil Hizmetinde Üye Tamamlama](../../extensibility/internals/member-completion-in-a-legacy-language-service.md)

- [Eski Dil Hizmetinde Parametre Bilgileri](../../extensibility/internals/parameter-info-in-a-legacy-language-service2.md)

- [Eski Dil Hizmetinde Hızlı Bilgiler](../../extensibility/internals/quick-info-in-a-legacy-language-service.md)

- [Eski Dil Hizmetinde Otomatik Değişkenler Penceresi için Destek](../../extensibility/internals/support-for-the-autos-window-in-a-legacy-language-service.md)

- [Eski Dil Hizmetinde Kesme Noktalarını Doğrulama](../../extensibility/internals/validating-breakpoints-in-a-legacy-language-service.md)

## <a name="see-also"></a>Ayrıca Bkz.
- [Eski Dil Hizmeti Uygulama](../../extensibility/internals/implementing-a-legacy-language-service1.md)
- [Eski Dil Hizmeti Genişletilebilirliği](../../extensibility/internals/legacy-language-service-extensibility.md)