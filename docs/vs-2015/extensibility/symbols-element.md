---
title: Symbols öğesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- Symbols element (VSCT XML schema)
- VSCT XML schema elements, Symbols
ms.assetid: 1cda43d8-42a5-4b1b-a3c8-cf0401c3202f
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c8d28d225bd3a8d5c105bf54b9c63574002aed15
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54784669"
---
# <a name="symbols-element"></a>Symbols Öğesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

GUID'leri ve kimlikleri diğer VSCT öğeleri tarafından kullanılan tanımlar. Yönetilmeyen kod için bu bilgiler genellikle tarafından belirtilen üst bilgi dosyaları geldiği [Extern öğesi](../extensibility/extern-element.md). Kod kullanan bu bilgileri tanımlamak için semboller öğenin alt öğeleri yönetilen.  
  
 Mevcut bir .cto dosyadan .vsct dosyası oluşturma simgeleri Symbols öğesi alt öğesi olarak oluşturulur. Daha fazla bilgi için [nasıl yapılır: Oluşturma bir. Vsct mevcut bir dosya. Cto dosya](../misc/how-to-create-a-dot-vsct-file-from-an-existing-dot-cto-file.md).  
  
 Symbols öğesi ile karıştırılmamalıdır [tanımlama öğesi](../extensibility/define-element.md), önişlemci tarafından kullanılmak üzere ad-değer çiftleri tanımlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<Symbols>  
  <GuidSymbol>... </GuidSymbol>  
  <GuidSymbol>... </GuidSymbol>  
</Symbols>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|Hiçbiri||  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|GuidSymbol|Bir GUID sembolünü tanımlar. GuidSymbol iki gerekli özniteliklere sahip: ad ve değer. Simgenin adını adıdır ve değeri bir dize olarak GUID değeridir.<br /><br /> Örneğin:\<GuidSymbol name = "guidVsPackage1Pkg" value = "{c5f54698-101a-4846-84d3-dc748f9cd848}" / >|  
|Idsymbol|Bir sembolü tanımlar. Idsymbol iki gerekli özniteliklere sahip: ad ve değer. Simgenin adını adıdır ve değer bir dize olarak sembol değerdir.<br /><br /> Örneğin:\<Idsymbol name = "MyMenuGroup" value = "0x1020" / >|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[CommandTable Öğesi](../extensibility/commandtable-element.md)|.Vsct dosyası kök öğesi.|  
  
## <a name="example"></a>Örnek  
  
```  
<Symbols>  
  <GuidSymbol name="guidVsPackage1Pkg" value="{c5f54698-101a-4846-84d3-dc748f9cd848}" />  
  <GuidSymbol name="guidVsPackage1CmdSet" value="{cb9dfd7f-2fcc-4a3e-aae8-f7fe30b1cfac}">  
    <IDSymbol name="MyMenuGroup" value="0x1020" />  
    <IDSymbol name="cmdidMyCommand" value="0x0100" />  
    <IDSymbol name="cmdidMyTool" value="0x0101" />  
  </GuidSymbol>  
</Symbols>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
