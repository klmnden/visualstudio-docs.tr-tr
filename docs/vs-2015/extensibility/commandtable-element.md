---
title: CommandTable öğesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- CommandTable
helpviewer_keywords:
- CommandTable element (VSCT XML schema)
- VSCT XML schema elements, CommandTable
ms.assetid: 15c38159-660a-4ef4-9643-aa6fcfca82a9
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 22cbe4fc34ae41f89709d5b20f2c1188edcd0de3
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65685296"
---
# <a name="commandtable-element"></a>CommandTable Öğesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

CommandTable .vsct dosyası kök öğesidir. Bu gerçek düzeni ve IDE VSPackage sağlayan komut türü tanımlayan dosyasıdır. Komutlarını, menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları içerebilir. Daha fazla bilgi için [Visual Studio komut tablosu (. Vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<CommandTable xmlns="http://schemas.microsoft.com/VisualStudio/2005-10-18/CommandTable" xmlns:xs="http://www.w3.org/2001/XMLSchema" >  
  <Extern>... </Extern>  
  <Include>... </Include>  
  <Define>... </Define>  
  <Commands>... </Commands>  
  <CommandPlacements>... </CommandPlacements>  
  <VisibilityConstraints>... </VisibilityConstraints>  
  <KeyBindings>... </KeyBindings>  
  <UsedCommands... </UsedCommands>  
  <Symbols>... </Symbols>  
</CommandTable>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
| Öznitelik |                                                                                                                   Açıklama                                                                                                                   |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   xmlns   |                                   Gerekli. XML ad alanları:<br /><br /> xmlns="<http://schemas.microsoft.com/VisualStudio/2005-10-18/CommandTable>"<br /><br /> xmlns:xs="<http://www.w3.org/2001/XMLSchema>"                                   |
| dil  | İsteğe bağlı. Language özniteliği, tüm varsayılan dili belirtmek için kullanılabilir \<dizeleri > komut tablosu öğeleri.  Dil belirtilmezse, geçerli işlemin dil kullanılır:<br /><br /> Dil = "en-us" |
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Extern Öğesi](../extensibility/extern-element.md)|İsteğe bağlı. Derleyici için ön işlemci yönergeleri içerir.|  
|[Include Öğesi](../extensibility/include-element.md)|İsteğe bağlı. Derleme içinde içerecek şekilde tüm dosyalara olan yolları içerir.|  
|[Define Öğesi](../extensibility/define-element.md)|İsteğe bağlı. Kendi ad ve değer verilen bir sembolü tanımlar.|  
|[Commands Öğesi](../extensibility/commands-element.md)|İsteğe bağlı. Tüm diğer öğeleri içeren bir VSPackage için tüm komutları tanımlayan üst öğe.|  
|[CommandPlacements Öğesi](../extensibility/commandplacements-element.md)|İsteğe bağlı. Komut çubuğundaki komutları yerleştirilecek nerede tanımlar.|  
|[VisibilityConstraints Öğesi](../extensibility/visibilityconstraints-element.md)|İsteğe bağlı. Komutlar ve araç çubukları statik görünürlüğünü belirler.|  
|[KeyBindings Öğesi](../extensibility/keybindings-element.md)|İsteğe bağlı. Kısayol tuş birleşimleri, komutları belirtir.|  
|[UsedCommands Öğesi](../extensibility/usedcommands-element.md)|İsteğe bağlı. İsteğe bağlı olarak kendi özgün diğer VSPackage'ları tarafından desteklenen sürümüne uygulamak bir VSPackage sağlar.|  
|[Symbols Öğesi](https://msdn.microsoft.com/f2ddd0aa-c3dd-439e-834d-28f136a27ffa)|İsteğe bağlı. Derleyici için herhangi bir sembol verilerini--GUID'leri, kimlikleri ve benzeri--içerir.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|None||  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
