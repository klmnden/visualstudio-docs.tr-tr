---
title: Öğe dahil | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- Include
helpviewer_keywords:
- Include element (VSCT XML schema)
- VSCT XML schema elements, Include
ms.assetid: c923dfe6-084a-4105-aec1-f0a3f8399c54
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4f79a05268a6c1741f7c5d341b0d56e316dbce9c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54940537"
---
# <a name="include-element"></a>Öğe Ekle
INCLUDE öğesi bulunabilir dosyayı belirtir. sağlanan üzerinde geçerli dosyasına ekleme yolu ekleyin.  Tüm semboller ve tanımlanan türleri derlenen sonuçtaki bir parçası olur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```csharp  
<Include href="stdidcmd.h" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|href|Gerekli. Üstbilgi dosyası yolu:<br /><br /> href="stdidcmd.h"|  
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|  
  
### <a name="child-elements"></a>Alt öğeleri  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|Yok.|Yok.|  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[CommandTable öğesi](../extensibility/commandtable-element.md)|Tüm komutları temsil eden öğeler tanımlar — diğer bir deyişle, menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları — IDE'ye VSPackage sağlayan.|  
  
## <a name="example"></a>Örnek  
  
```  
<Include href="PackagePlacements.vsct"/>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)