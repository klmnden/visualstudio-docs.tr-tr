---
title: Iactivescriptsiteuıcontrol::getuıbehavior metodu | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 9a944335-856a-4c6b-b2bc-8872542941b7
caps.latest.revision: 2
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1e3f6247afc70ef1197ea759ffdf475c2d6c0a0c
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58158220"
---
# <a name="iactivescriptsiteuicontrolgetuibehavior-method"></a>IActiveScriptSiteUIControl::GetUIBehavior Yöntemi
Alır bir [SCRIPTUICHANDLING numaralandırması](../../winscript/reference/scriptuichandling-enumeration.md) bir UI denetimine işlenmesi gereken şekilde temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetUIBehavior(     [in] SCRIPTUICITEM UicItem,     [out] SCRIPTUICHANDLING * pUicHandling );   
```  
  
#### <a name="parameters"></a>Parametreler  
 `UicItem`  
 Denetim türü.  
  
 `pUicHandling`  
 Denetim şekilde yapılması gerekir.