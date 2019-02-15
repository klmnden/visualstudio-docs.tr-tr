---
title: Komut kodu numaralandırıcısı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- command code enumerator
- source control plug-ins, command code enumeration
ms.assetid: 5d2c360c-59e4-4da8-bcb4-dd07c7441e40
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 97b856b0c22631b3e4f9b8860f9aaba728e6944d
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56315501"
---
# <a name="command-code-enumerator"></a>Komut kodu numaralandırıcısı
Bu Numaralandırıcının seçenekleri kullanılır [SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md) ve [SccPopulateList](../extensibility/sccpopulatelist-function.md)seçenekler belirtilir komutu belirtmek için.

## <a name="syntax"></a>Sözdizimi

```
enum SCCCOMMAND {
   SCC_COMMAND_GET,
   SCC_COMMAND_CHECKOUT,
   SCC_COMMAND_CHECKIN,
   SCC_COMMAND_UNCHECKOUT,
   SCC_COMMAND_ADD,
   SCC_COMMAND_REMOVE,
   SCC_COMMAND_DIFF,
   SCC_COMMAND_HISTORY,
   SCC_COMMAND_RENAME,
   SCC_COMMAND_PROPERTIES,
   SCC_COMMAND_OPTIONS
};
```

## <a name="members"></a>Üyeler
SCC_COMMAND_GET  
Karşılık gelen [SccGet](../extensibility/sccget-function.md).

SCC_COMMAND_CHECKOUT  
Karşılık gelen [SccCheckout](../extensibility/scccheckout-function.md).

SCC_COMMAND_CHECKIN  
Karşılık gelen [SccCheckin](../extensibility/scccheckin-function.md).

SCC_COMMAND_UNCHECKOUT  
Karşılık gelen [SccUncheckout](../extensibility/sccuncheckout-function.md).

SCC_COMMAND_ADD  
Karşılık gelen [SccAdd](../extensibility/sccadd-function.md).

SCC_COMMAND_REMOVE  
Karşılık gelen [SccRemove](../extensibility/sccremove-function.md).

SCC_COMMAND_DIFF  
Karşılık gelen [SccDiff](../extensibility/sccdiff-function.md).

SCC_COMMAND_HISTORY  
Karşılık gelen [SccHistory](../extensibility/scchistory-function.md).

SCC_COMMAND_RENAME  
Karşılık gelen [SccRename](../extensibility/sccrename-function.md).

SCC_COMMAND_PROPERTIES  
Karşılık gelen [SccProperties](../extensibility/sccproperties-function.md).

SCC_COMMAND_OPTIONS  
Karşılık gelen [SccSetOption](../extensibility/sccsetoption-function.md).

## <a name="see-also"></a>Ayrıca bkz.
[Kaynak denetimi eklentileri](../extensibility/source-control-plug-ins.md)  
[SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md)  
[SccPopulateList](../extensibility/sccpopulatelist-function.md)
