---
title: IDebugApplicationNode100::GetExcludedDocuments | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationNode100::GetExcludedDocuments
ms.assetid: d44583a7-0b0b-4799-b075-837ad1da1946
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1120b85ded35dbbe9c8c038350080e4071b19cf8
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58152229"
---
# <a name="idebugapplicationnode100getexcludeddocuments"></a>IDebugApplicationNode100::GetExcludedDocuments
Belirtilen filtre tarafından gizlenen metin belgeleri alır.  
  
> [!IMPORTANT]
>  [Idebugapplicationnode100 arabirimi](../../winscript/reference/idebugapplicationnode100-interface.md) PDM v10.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetExcludedDocuments(        [in] APPLICATION_NODE_EVENT_FILTER filter,        [out] TEXT_DOCUMENT_ARRAY* pDocuments        );  
```  
  
#### <a name="parameters"></a>Parametreler  
 `filter`  
 Filtre.  
  
 `pDocuments`  
 Belge kümesini.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplicationNode100 Arabirimi](../../winscript/reference/idebugapplicationnode100-interface.md)