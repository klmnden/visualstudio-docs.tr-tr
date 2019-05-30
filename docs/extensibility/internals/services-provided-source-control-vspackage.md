---
title: Sağlanan hizmetler (kaynak denetimi VSPackage'ı) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- services, source control packages
- source control packages, services
ms.assetid: 9db07d70-87d2-4401-bc88-e3a49d81e9a2
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 72c95b0cf5b89588f5436663046829dc589bc9f2
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66322665"
---
# <a name="services-provided-source-control-vspackage"></a>Sağlanan Hizmetler (Kaynak Denetimi VSPackage’ı)
Yönelik birincil mekanizmadır üzerinden işlevselliği Vspackage'lar arasında ve Visual Studio tümleşik geliştirme ortamı (IDE) ve kendi yüklü Vspackage'lar arasında paylaşılan hizmetlerdir. Hizmetleri ve Visual Studio IDE'de önemini ayrıntılı açıklaması için bkz:[kullanma ve sağlama Hizmetleri](../../extensibility/using-and-providing-services.md).

## <a name="the-source-control-service"></a>Kaynak denetimi hizmeti
 Visual Studio, hizmetlerin, IDE düzeyi hizmetler ve paket düzeyinde hizmetlerinin iki katman sağlar. Visual Studio IDE, IDE düzeyi Hizmetleri yerel olarak sağlar. Kaynak Denetim paketi bu hizmetlerden bazıları tüketir. VSPackage olarak kaynak denetimi paketi, kaynak denetim işlevselliğini bir özel kaynak denetimi hizmetini kendi sağlayarak paylaşır. Kaynak Denetim paketi, Visual Studio IDE tarafından kullanılabilecek bir sözleşme biçiminde tarafından uygulanan kaynak denetimi ile ilgili arabirimler kümesini yalıtır.

## <a name="see-also"></a>Ayrıca Bkz.
- [Tasarım Öğeleri](../../extensibility/internals/source-control-vspackage-design-elements.md)