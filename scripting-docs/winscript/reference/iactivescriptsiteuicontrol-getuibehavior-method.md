---
title: Iactivescriptsiteuıcontrol::getuıbehavior metodu | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 9a944335-856a-4c6b-b2bc-8872542941b7
caps.latest.revision: 2
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b52c94e9c8b14218362000df401fba24568ea426
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54344804"
---
# <a name="iactivescriptsiteuicontrolgetuibehavior-method"></a>IActiveScriptSiteUIControl::GetUIBehavior Metodu
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