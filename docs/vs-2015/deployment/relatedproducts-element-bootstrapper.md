---
title: '&lt;RelatedProducts&gt; öğesi (Önyükleyici) | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
f1_keywords:
- MSBuild.GenerateBootstrapper.MissingDependency
- MSBuild.GenerateBootstrapper.DuplicateItems
- MSBuild.GenerateBootstrapper.IncludedProductIncluded
- MSBuild.GenerateBootstrapper.DependencyNotFound
- MSBuild.GenerateBootstrapper.PackageFileNotFound
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- <RelatedProducts> element [bootstrapper]
ms.assetid: bf152712-4c1e-48bd-9b7f-311cf0fdb832
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 70afe724be5b782bc90e162fd65f83ad1b0d0d23
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54791857"
---
# <a name="ltrelatedproductsgt-element-bootstrapper"></a>&lt;RelatedProducts&gt; öğesi (Önyükleyici)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

`RelatedProducts` Öğe bağlı ya da geçerli ürün dahil diğer ürünleri tanımlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<RelatedProducts>  
    <DependsOnProduct  
        Code  
    />  
    <EitherProducts>  
        <DependsOnProduct  
            Code  
        />  
    </EitherProducts>  
    <IncludesProduct  
        Code  
    />  
</RelatedProducts>  
```  
  
## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler  
 `RelatedProducts` Öğesi alt öğesi olan `Product` öğesi. Bu öznitelikleri yok.  
  
## <a name="dependsonproduct"></a>DependsOnProduct  
 `DependsOnProduct` Öğesi geçerli ürün adlandırılmış ürüne bağlı bağlıdır ve önce geçerli bir adlandırılmış ürünün yüklenmesi gerektiğini belirtir. Bir alt öğesidir `RelatedProducts` öğesi. A `RelatedProducts` öğesi bir veya daha fazla olabilir `DependsOnProduct` öğeleri.  
  
 `DependsOnProduct` Aşağıdaki özniteliklere sahiptir.  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`Code`|Kod adı tarafından belirtilen bulunan ürünün `ProductCode` özniteliği `Product` öğesi. Daha fazla bilgi için [ \<ürün > öğesi](../deployment/product-element-bootstrapper.md).|  
  
## <a name="eitherproducts"></a>EitherProducts  
 `EitherProducts` Sıfır veya daha fazla öğe tanımlar `DependsOnProduct` öğeleri ve öznitelikleri yok. En az bir `DependsOnProduct` bu kümesinde geçerli bir ürün önce yüklenmelidir. A `RelatedProducts` öğesi sıfır veya daha fazla olabilir `EitherProducts` öğeleri.  
  
## <a name="includesproduct"></a>IncludesProduct  
 `IncludesProduct` Öğeyi belirten bir ürünün geçerli yükleme işlemine dahildir ve ayrı bir yükleme gerektirmez. Bir alt öğesidir `RelatedProducts` öğesi. A `RelatedProducts` öğesi bir veya daha fazla olabilir `IncludesProduct` öğeleri.  
  
 `IncludesProduct` Aşağıdaki özniteliklere sahiptir.  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`Code`|Kod adı tarafından belirtilen bulunan ürünün `ProductCode` özniteliği `Product` öğesi. Daha fazla bilgi için [ \<ürün > öğesi](../deployment/product-element-bootstrapper.md).|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği ile Microsoft Installer yüklendiğini belirtir [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)]ve bu nedenle ayrı bir yükleme gerekmez.  
  
```  
<RelatedProducts>  
    <IncludesProduct Code="Microsoft.Windows.Installer.2.0" />  
</RelatedProducts>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [\<Ürün > öğesi](../deployment/product-element-bootstrapper.md)
