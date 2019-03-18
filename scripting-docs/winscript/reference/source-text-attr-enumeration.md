---
title: SOURCE_TEXT_ATTR numaralandırması | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- SOURCE_TEXT_ATTR constants
ms.assetid: 459384b0-1463-4841-a2b3-a993207163bf
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 05faeddf43c91ce0f45d54d2f6b6ed46cf8d2a4f
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58157993"
---
# <a name="sourcetextattr-enumeration"></a>SOURCE_TEXT_ATTR Numaralandırması
Kaynak metnin tek bir karakterinin özniteliklerini açıklar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
enum enum_SOURCE_TEXT_ATTR{    SOURCETEXT_ATTR_KEYWORD    = 0x0001,    SOURCETEXT_ATTR_COMMENT    = 0x0002,    SOURCETEXT_ATTR_NONSOURCE    = 0x0004,    SOURCETEXT_ATTR_OPERATOR   = 0x0008,    SOURCETEXT_ATTR_NUMBER    = 0x0010,    SOURCETEXT_ATTR_STRING    = 0x0020,    SOURCETEXT_ATTR_FUNCTION_START  = 0x0040};  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Değer|Açıklama|  
|------------|-----------|-----------------|  
|SOURCETEXT_ATTR_KEYWORD|0x0001|Karakter, bir dil anahtar sözcüğü, örneğin, VBScript anahtar sözcük parçasıdır `While`.|  
|SOURCETEXT_ATTR_COMMENT|0x0002|Karakter, bir açıklama bloğu bir parçasıdır.|  
|SOURCETEXT_ATTR_NONSOURCE|0x0004|Karakter derlenmiş dil kaynak metin parçası değil. Örneğin, bir komut dosyası bloğu çevreleyen HTML.|  
|SOURCETEXT_ATTR_OPERATOR|0x0008|Karakter, bir dil işleci bir parçasıdır. Örneğin:, aritmetik işleç **+**.|  
|SOURCETEXT_ATTR_NUMBER|0x0010|Karakter, bir dil sayısal sabit bir parçasıdır.  Örneğin, sabit olarak 3,14159.|  
|SOURCETEXT_ATTR_STRING|0x0020|Karakter, bir dil dizesi sabit bir parçasıdır. Örneğin, dize "Hello World".|  
|SOURCETEXT_ATTR_FUNCTION_START|0x0040|İşlev bloğu başlangıcı karakteri gösterir|  
  
## <a name="remarks"></a>Açıklamalar  
 Genellikle, `IDebugDocumentHost::GetScriptTextAttributes`, `IActiveScriptDebug::GetScriptletTextAttributes`, ve `IActiveScriptDebug::GetScriptTextAttributes` yöntemleri sürece her karakter, bir metin özniteliği döndürür:  
  
-   Bu durumda yöntem SOURCETEXT_ATTR_IDENTIFIER ve SOURCETEXT_ATTR_MEMBERLOOKUP bayrakları döndürebilir GETATTRTYPE_DEPSCAN bayrağı ayarlandığından,  
  
-   Bu durumda yöntem SOURCETEXT_ATTR_THIS bayrağı döndürebilir GETATTRFLAG_THIS bayrağı ayarlandığından,  
  
-   Bu durumda yöntem SOURCETEXT_ATTR_HUMANTEXT bayrağı döndürebilir GETATTRFLAG_HUMANTEXT bayrağı ayarlanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Hata Ayıklayıcı Sabitleri, Sabit Listeleri ve Yapıları](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)