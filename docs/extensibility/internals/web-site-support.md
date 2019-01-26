---
title: Web sitesi desteği | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- web site projects
ms.assetid: ce9f4266-bb64-4c09-be88-4bd6413f60d0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a84b59085e2850a7c889e3468788fb8ef23414ca
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54959920"
---
# <a name="web-site-support"></a>Web Sitesi Desteği
Bir Web sitesi proje sistemi Web projeleri oluşturan bir proje sistemidir. Web projeleri sırayla Web uygulamaları oluşturun. Bir Web sitesi projesi kod ilişkili her bir Web sayfası için bir yürütülebilir dosya oluşturur. Ek yürütülebilir dosyalar /App_Code klasöründeki kaynak kodu dosyasından oluşturulur.  
  
 Web sitesi proje sistemleri, varolan bir proje sistemine şablonları ve kaydı öznitelikleri ekleyerek oluşturulur. Bu öznitelikler dil için IntelliSense sağlayıcı seçer. IntelliSense sağlayıcı uygulaması başvuruları işler ve önbelleğe alınmamış akıllı bir Web sayfası istenen dil derleyicisini çağırır.  
  
 Web sayfaları derlemek için kullanılan dil derleyici ile kaydedilmelidir [!INCLUDE[vstecasp](../../code-quality/includes/vstecasp_md.md)]. Kullanabileceğiniz [ \<derleyici > öğesi](/dotnet/framework/configure-apps/file-schema/compiler/compiler-element) Web.config dosyasında aşağıdaki örnekte olduğu gibi derleyici kaydetmek için:  
  
```  
<system.codedom>  <compilers>    <compiler language="py;IronPython" extension=".py"       type="IronPython.CodeDom.PythonProvider, IronPython,       Version=1.0.2391.18146, Culture=neutral,       PublicKeyToken=b03f5f7f11d50a3a" />  </compilers></system.codedom>  
```  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Web Sitesi Destek Şablonları](../../extensibility/internals/web-site-support-templates.md)  
 Yeni Web sitesi projeleri ve ilişkili öğeleri oluşturmak için kullanabileceğiniz şablonları listeler.  
  
 [Web Sitesi Destek Öznitelikleri](../../extensibility/internals/web-site-support-attributes.md)  
 Bir Web sitesi projesine bağlanmak kaydı öznitelikleri gösterir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ve [!INCLUDE[vstecasp](../../code-quality/includes/vstecasp_md.md)].  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Web Projeleri](../../extensibility/internals/web-projects.md)  
 Web projeleri, Web sitesi projeleri ve Web Uygulama projeleri iki tür genel bir bakış sunar.