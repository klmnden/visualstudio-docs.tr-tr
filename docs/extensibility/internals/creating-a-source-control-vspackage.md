---
title: Bir kaynak denetimi VSPackage'ı oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control [Visual Studio SDK], creating source control packages
- source control packages
ms.assetid: cca0a9ed-48ff-409f-8036-ed8db0f7533e
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 259273eee51c74eb7cb5ca4534db9bc575fd1758
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66345487"
---
# <a name="create-a-source-control-vspackage"></a>Kaynak denetimi VSPackage'ı oluşturma
Bu belge mimarisine genel bakış ile tümleşik kaynak denetimi paketi bağlantılarını içerir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], uygulanacak arabirimleri ve tüketilmesi Hizmetleri tarafından tanımlanan API ve basit bir kaynağı gösteren bir örnek paket uygulama denetimi.

 Bir kaynak denetimi VSPackage'ı ile kapsamlı tümleştirme yolu ile tümleştirmek kaynak denetimi için oluşturabileceğiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Varsayılan kaynak denetimi tarafından barındırılan UI atlamak için paketi etkinleştirir. [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], proje sistemi kaynak denetimi isteklerine yanıt vermek ve etkileşim [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] bileşenleri gibi **Çözüm Gezgini**. [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] Güçlendirir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] iş ortakları ile tümleştirilebilir bir VSPackage'ı oluşturmak için bir mekanizma [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hizmet modelini kullanma.

## <a name="in-this-section"></a>Bu bölümde
- [Kullanmaya başlama](../../extensibility/internals/getting-started-with-source-control-vspackages.md)

 Kaynak Denetimi Eklentisi Kaynak denetimi uygulamak için daha gelişmiş bir alternatifidir kaynak denetim paketi anlatılmaktadır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

- [Mimari](../../extensibility/internals/source-control-vspackage-architecture.md)

 Bir diyagramını sunar ve kaynak denetimi paket bileşenlerinin açıklar.

- [Özellikler](../../extensibility/internals/source-control-vspackage-features.md)

 Bir kaynak denetim paketi çeşitli özelliklerini açıklar.

- [Tasarım öğeleri](../../extensibility/internals/source-control-vspackage-design-elements.md)

 Bir kaynak denetim paketi için derin tümleştirme uygulamalıdır VSPackage'ı yapısını açıklar.

## <a name="related-sections"></a>İlgili bölümler
- [Kaynak Denetimi Eklentisi oluşturma](../../extensibility/internals/creating-a-source-control-plug-in.md)

 İçinde kaynak denetimi işlevlerini sağlar. kaynak denetimi eklentisi oluşturma anlatılmaktadır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] kaynak denetimi kullanıcı arabirimini (UI).

- [Kaynak denetimi](../../extensibility/internals/source-control.md)

 Tümleşik bir özelliği olarak kaynak denetimi uygulama seçenekleri ele alınmaktadır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].
