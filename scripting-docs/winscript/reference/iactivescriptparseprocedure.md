---
title: Iactivescriptparseprocedure | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptParseProcedure interface
ms.assetid: 741a35bb-5b92-489e-ba8a-a406b42125fc
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5ed07ce5ed48abfb377dde5fc4d5dc128d881b4a
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58151355"
---
# <a name="iactivescriptparseprocedure"></a>IActiveScriptParseProcedure
Kaynak kod metni komut dosyasına eklenecek yordamlar için Windows komut dosyası altyapısı izin veriyorsa, bunu uygulayan `IActiveScriptParseProcedure` arabirimi. VBScript gibi hiçbir bağımsız geliştirme ortamına sahip yorumlanan komut dosyası dilleri için bu alternatif bir mekanizma sağlar (dışında `IActiveScriptParse` veya `IPersist`*) betik yordamları ad alanına eklemek için.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|||  
|-|-|  
|Yöntem|Açıklama|  
|[IActiveScriptParseProcedure::ParseProcedureText](../../winscript/reference/iactivescriptparseprocedure-parseproceduretext.md)|Verilen kod yordamı ayrıştırır ve yordam, ad alanına ekler.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Arabirimleri](../../winscript/reference/active-script-interfaces.md)