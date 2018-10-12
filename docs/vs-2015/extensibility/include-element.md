---
title: Öğe dahil | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- Include
helpviewer_keywords:
- Include element (VSCT XML schema)
- VSCT XML schema elements, Include
ms.assetid: c923dfe6-084a-4105-aec1-f0a3f8399c54
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 9fdc57962b101b864370e2a70fdc6327ef7e6110
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49302336"
---
# <a name="include-element"></a>Include Öğesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

INCLUDE öğesi bulunabilir dosyayı belirtir. sağlanan üzerinde geçerli dosyasına ekleme yolu ekleyin.  Tüm semboller ve tanımlanan türleri derlenen sonuçtaki bir parçası olur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```csharp  
<Include href="stdidcmd.h" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|href|Gerekli. Üstbilgi dosyası yolu:<br /><br /> href="stdidcmd.h"|  
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|Yok.|Yok.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[CommandTable Öğesi](../extensibility/commandtable-element.md)|Tüm komutları temsil eden öğeler tanımlar — diğer bir deyişle, menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları — IDE'ye VSPackage sağlayan.|  
  
## <a name="example"></a>Örnek  
  
```  
<Include href="PackagePlacements.vsct"/>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)

