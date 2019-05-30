---
title: Proje türleri mimarisi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], architecture
ms.assetid: 9c1d940f-8a54-41f7-a8aa-c870e324371c
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6d77524097509c45c23d6a3d9cc147e5aba6691d
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66318893"
---
# <a name="project-types-architecture"></a>Proje Türleri Mimarisi
Bu bölümde proje türleri mimarisi hakkında ayrıntılı bilgi içeren [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

## <a name="in-this-section"></a>Bu Bölümde
- [Proje Modeli Öğeleri](../../extensibility/internals/elements-of-a-project-model.md)

 Bir proje türü kullanabilir hizmetlerini ve bunu uygulamalıdır arabirimler listelenmiştir.

- [Proje Modeli Çekirdek Bileşenleri](../../extensibility/internals/project-model-core-components.md)

 Proje türleri hem uygulamalıdır ve isteğe bağlı olarak ek işlevsellik sağlamak için uygulayabileceğiniz arabirimler açıklanmaktadır.

- [Proje Türlerinin Oluşturulacağı Durumlar](../../extensibility/internals/when-to-create-project-types.md)

 Karar bir proje oluşturduğunuzda gerekir yardımcı yazın ve ne zaman kullanabileceğiniz başka [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] gibi VSPackages ve düzenleyicileri aynı hedefe ulaşmak için genişletilebilirlik özelliği.

- [Hiyerarşiler ve Seçim](../../extensibility/internals/hierarchies-and-selection.md)

 Açıklayan nasıl [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tutarlı ve Basitleştirilmiş kullanıcı deneyimi sağlamak için hiyerarşiler ve seçim bağlamını kullanır.

## <a name="related-sections"></a>İlgili Bölümler
- [Proje Alt Türleri](../../extensibility/internals/project-subtypes.md)

 Proje alt türleri proje sistemleri davranışını özelleştirmenize izin nasıl açıklar [!INCLUDE[vbprvb](../../code-quality/includes/vbprvb_md.md)] ve [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)].

- [Proje Türleri](../../extensibility/internals/project-types.md)

 Temel yapı taşları projelerine genel bir bakış sağlar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı (IDE). Projeler oluşturmak ve kodu derleme nasıl kontrol açıklayan ek konulara bağlantılar sağlanmaktadır.