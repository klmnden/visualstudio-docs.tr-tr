---
title: Web sitesi destek öznitelikleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- web site projects, registration
ms.assetid: 46d52e2c-ca2a-4bbd-8500-5b0129768aec
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: ea55937318d22a40b90cddb54490b87ab0c44325
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53916828"
---
# <a name="web-site-support-attributes"></a>Web Sitesi Destek Öznitelikleri
[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Web sitesi projesi Web desteği sağlamak için programlama genişletilebilir. Dil kendisi ile kaydetmelisiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] böylece proje şablonları görünebilen **yeni Web sitesi** dil seçildiğinde iletişim kutusu.

IronPython Studio örnek web sitesi desteği içerir. Örnek, IronPython, yeni Web projeleri için bir codebehind dili olarak kaydetmek için aşağıdaki öznitelik sınıfları içerir.

## <a name="websiteprojectattribute"></a>WebSiteProjectAttribute
 Bu öznitelik, dil projede yer alır. Web programlama dilleri listesini dili ekler **dil** listesinde **yeni Web sitesi** iletişim kutusu. Örneğin, aşağıdaki kod, IronPython listeye ekler:

```
[WebSiteProject("IronPython", "Iron Python")]
public class PythonProjectPackage : ProjectPackage
```

 Bu öznitelik, ayrıca şablonları klasörüne işaret edecek şekilde şablonları yolunu ayarlar. Şablonları klasörünün konumu hakkında daha fazla bilgi için bkz. [Web sitesi destek şablonları](../../extensibility/internals/web-site-support-templates.md).

## <a name="websiteprojectrelatedfilesattribute"></a>WebSiteProjectRelatedFilesAttribute
 Bu öznitelik, dil projede yer alır. Bir dosya türü (ilgili) içine yerleştirmek Web sitesi projesi başka bir dosya türü altında (birincil) verir **Çözüm Gezgini**.

 Örneğin, aşağıdaki kod bir IronPython codebehind dosya bir .aspx dosyasına ilgili olup olmadığını belirtir. Yeni bir .aspx Web sayfası bir IronPython Web sitesini çözümde oluşturulduğunda, yeni .py kaynak dosyası oluşturulur ve .aspx sayfasına bir alt düğüm olarak görünür.

```
[WebSiteProjectRelatedFiles("aspx", "py")]
public class PythonProjectPackage : ProjectPackage
```

## <a name="provideintellisenseproviderattribute"></a>ProvideIntellisenseProviderAttribute
 Bu öznitelik dil proje pakete yerleştirildi. Bu dil için IntelliSense sağlayıcısı seçer.

 Örneğin, aşağıdaki kodu belirtir uygulayan PythonIntellisenseProvider örneğini <xref:Microsoft.VisualStudio.Shell.Interop.IVsIntellisenseProject>, dil hizmetleri sağlamak amacıyla isteğe bağlı olarak oluşturulmalıdır.

```
[ProvideIntellisenseProvider(typeof(PythonIntellisenseProvider), "IronPythonCodeProvider", "Iron Python", ".py", "IronPython;Python", "IronPython")]
public class PythonPackage : Package, IOleComponent
```

 IVsIntellisenseProject uygulama başvuruları işler ve bir Web sayfası koduna sahip istenen ancak önbelleğe dil derleyicisini çağırır.

## <a name="see-also"></a>Ayrıca Bkz.
 [Web Sitesi Desteği](../../extensibility/internals/web-site-support.md)