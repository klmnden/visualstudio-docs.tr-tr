---
title: Visual Studio 2015 SDK kaynak denetimindeki yenilikler | Microsoft Docs
titleSuffix: ''
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- what's new [Visual Studio SDK], source control
- source control [Visual Studio SDK], what's new
ms.assetid: bcf85418-18fb-4824-9dae-d14bf3d56a77
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e12776c21d345d60992eeff4963498bcd7d56678
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66323259"
---
# <a name="whats-new-in-source-control-for-the-visual-studio-2015-sdk"></a>Visual Studio 2015 SDK için kaynak denetimindeki yenilikler

İçinde [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)], kaynak denetimi VSPackage'ı uygulayarak, derin tümleşik kaynak denetimi çözümü sağlayabilirsiniz. Bu bölümde, kaynak denetimi VSPackage'ları özelliklerini açıklar ve uygulama adımlarını genel bir bakış sağlar.

## <a name="the-source-control-vspackage"></a>Kaynak denetimi VSPackage'ı

Visual Studio, iki tür kaynak denetimine çözüm destekler. Tüm Visual Studio sürümlerinde, yine de kaynak denetimi eklentisi API tabanlı tümleştirebilirsiniz eklenti. VSPackage sağlayan bir derin tümleştirme, kaynak denetimi için de oluşturabilirsiniz [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] açıdan çok yönlülük ve otonomi yüksek düzeyde gerektiren kaynak denetim çözümleri için uygun yolu.

VSPackage için Visual Studio neredeyse her çeşit bir işlevselliği ekleyebilirsiniz. Kaynak denetimi VSPackage'ı tam kaynak denetimi özelliği için Visual Studio, kaynak denetim sistemi ile arka uca iletişimi kullanıcıya sunulan kullanıcı arabirimini sağlar.

Kaynak denetimi VSPackage'ı uygulayan bir "tümü veya hiçbiri" stratejisi gerektirir. Kaynak denetimi VSPackage'ı oluşturan arabirimlerin yanı sıra kaynak denetim arabirimleri ve yeni kullanıcı Arabirimi öğeleri (iletişim kutuları, menüler ve araç çubukları) tüm kaynak denetimi işlevini kapsayan bir dizi uygulamaya çabayı önemli ölçüde yatırım gerekir herhangi bir paket başarılı bir şekilde Visual Studio ile tümleştirmek için gerekli.

Aşağıdaki adımları, kaynak denetim paketi uygulamak için gereken genel bir bakış sağlar. Ayrıntılar için bkz [bir kaynak denetimi VSPackage'ı oluşturma](../../extensibility/internals/creating-a-source-control-vspackage.md).

1. Özel kaynak denetimi hizmetini proffers bir VSPackage'ı oluşturun.

2. Visual Studio tarafından proffered kaynak denetimi ile ilgili hizmetler, arabirimler uygulama (örneğin, <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProvider> arabirimi).

3. Kaynak denetimi VSPackage'ı kaydedin.

4. Tüm menü öğelerini, iletişim kutuları, araç çubukları ve bağlam menülerini de dahil olmak üzere kullanıcı Arabirimi, kaynak denetimi uygulayın.

5. Etkin olan ve sizin VSPackage tarafından işlenmesi gereken tüm kaynak denetimi ile ilgili olaylar, kaynak denetimine VSackage geçirilir.

6. Kaynak denetimi VSPackage'ı gerekir dinlemek için olanlar gibi olayları uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEvents3> arabirim yanı sıra izleme proje belge (TPD) olayları (tarafından uygulanan <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocuments2> arabirimi) ve gerekli eylemi gerçekleştirin.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2>
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProvider>
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEvents3>
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocuments2>
- [Genel bakış](../../extensibility/internals/source-control-integration-overview.md)
- [Kaynak Denetimi VSPackage’ı Oluşturma](../../extensibility/internals/creating-a-source-control-vspackage.md)