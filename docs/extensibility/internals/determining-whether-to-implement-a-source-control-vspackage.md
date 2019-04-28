---
title: Bir kaynak denetimi VSPackage'ı uygulanmayacağını belirleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control packages, about source control packages
ms.assetid: 60b3326e-e7e2-4729-95fc-b682e7ad5c99
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fd3e0888cb45facbf2946e6a4656147dab75350e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62910052"
---
# <a name="determine-whether-to-implement-a-source-control-vspackage"></a>Kaynak denetimi VSPackage'ı uygulanacağını belirleme
Bu bölümde, kaynak denetimi uygun tümleştirme yolu seçme hakkında çözümler ve verir geniş yönergeleri genişletmek için kaynak denetimi eklentileri ve kaynak denetimi VSPackage'ları seçimleri elaborates.

## <a name="small-source-control-solution-with-limited-resources"></a>Küçük kaynak denetimine çözüm sınırlı kaynaklarla
 Kaynakların sınırlı ve kaynak denetimi paketi yazma yüklerle burdened, kaynak denetimi eklentisi API tabanlı eklentiler oluşturabilirsiniz. Bunun yapılması kaynak denetimi paketleri ile yan yana çalışmanıza olanak sağlar ve kaynak denetimi eklentileri ve isteğe bağlı paketleri arasında geçiş yapabilirsiniz. Daha fazla bilgi için [kayıt ve seçim](../../extensibility/internals/registration-and-selection-source-control-vspackage.md).

## <a name="large-source-control-solution-with-a-rich-feature-set"></a>Büyük kaynak denetimi çözümü ile zengin bir özellik kümesi
 Kaynak Denetimi Eklentisi API kullanarak yeterince yakalanmaz bir zengin kaynak denetimi modeli sağlayan bir kaynak denetimi çözümü uygulamak istiyorsanız, bir kaynak denetim paketi tümleştirme yolu olarak düşünebilirsiniz. Özellikle yerine kaynak denetimi bağdaştırıcısı (kaynak denetimi eklentileri ile iletişim kurar ve bir temel kaynak denetim UI sağlar) paketini yerini alır, kaynak denetim olayları özel bir şekilde işleyebilmeniz bu kendi geçerlidir. UI denetim ve bu deneyimi korumak istiyorsanız tatmin edici bir kaynak zaten varsa [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], kaynak denetimi paket seçeneği bunu yapmanıza olanak tanır. Kaynak Denetim paketi genel değildir ve yalnızca ile kullanılmak üzere tasarlanmış [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE.

 Esneklik ve daha zengin denetim Kaynak Denetim mantığı ve UI olanağı sağlayan bir kaynak denetimi çözümü uygulamak istiyorsanız, kaynak denetimi paket tümleştirme yolu tercih edebilirsiniz. Şunları yapabilirsiniz:

1. Kendi kaynak denetimi VSPackage'ı kaydetmek (bkz [kayıt ve seçim](../../extensibility/internals/registration-and-selection-source-control-vspackage.md)).

2. Varsayılan kaynak denetimi UI özel kullanıcı Arabirimi ile değiştirin (bkz [özel kullanıcı arabirimi](../../extensibility/internals/custom-user-interface-source-control-vspackage.md)).

3. Kullanılması ve Çözüm Gezgini glif olayları işlemek için karakter belirtin (bkz [karakter denetimi](../../extensibility/internals/glyph-control-source-control-vspackage.md)).

4. Sorgu düzenleme ve sorguyu kaydedin olaylarını işleme (bkz [sorgu düzenleme sorgu kaydetme](../../extensibility/internals/query-edit-query-save-source-control-vspackage.md)).

## <a name="see-also"></a>Ayrıca bkz.
- [Kaynak Denetimi Eklentisi oluşturma](../../extensibility/internals/creating-a-source-control-plug-in.md)