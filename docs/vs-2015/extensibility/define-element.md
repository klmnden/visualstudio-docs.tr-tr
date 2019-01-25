---
title: Define öğesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- VSCT XML schema elements, Define
- Define element (VSCT XML schema)
ms.assetid: 5aee74e3-de41-4dc6-9618-93e158af56dd
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 8cc543a07176f307641c53a2ef3e132881821ce7
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54752553"
---
# <a name="define-element"></a>Define Öğesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Sembol ad ve değer çifti tanımlar. Bu simge, koşullu özniteliklere göre değerlendirilebilir. Daha fazla bilgi için [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md). Ayrıca bkz: [Symbols öğesi](../extensibility/symbols-element.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<Define name="Mode" value="Standard" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|name|Gerekli. Sembol adı:<br /><br /> ad = "Modu"|  
|value|Gerekli. Sembol değeri:<br /><br /> değer = "Standart"|  
|Koşul|İsteğe bağlı. Daha fazla bilgi için [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[CommandTable Öğesi](../extensibility/commandtable-element.md)|VSPackage sağlayan komutlar tümleşik geliştirme ortamı (IDE) temsil eden tüm öğeleri tanımlar. Örneğin, menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları.|  
  
## <a name="example"></a>Örnek  
  
```  
<Define name="DEMO_UI"/>  
<Define name="MODE" value="Standard"/>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
