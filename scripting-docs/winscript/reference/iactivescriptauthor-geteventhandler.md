---
title: IActiveScriptAuthor::GetEventHandler | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptAuthor.GetEventHandler
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptAuthor::GetEventHandler
ms.assetid: 87c7a71d-46b9-448c-b34d-394105e20982
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7bba60df6485ddaac0363a3416739efd7be69389
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58145648"
---
# <a name="iactivescriptauthorgeteventhandler"></a>IActiveScriptAuthor::GetEventHandler
Belirtilen öznitelikleri scriptlet döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetEventHandler(  
   IDispatch          *pdisp,  
   LPCOLESTR          pszItem,  
   LPCOLESTR          pszSubItem,  
   LPCOLESTR          pszEvent,  
   IScriptEntry       **ppse  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pdisp`  
 [in] `IDispatch` Karşılık gelen nesne `NamedItem` scriptlet ekli olduğu için.  
  
 `pszItem`  
 [in] Üst düzey konak tam kod oluşturma adı tanıtıcısı arabellek adresi.  
  
 `pszSubItem`  
 [in] Ana bilgisayarın tam kod oluşturma adı ikinci düzey tanıtıcısı arabellek adresi. Tek düzey adı varsa, NULL olarak ayarlayın.  
  
 `pszEvent`  
 [in] Olay adını içeren bir arabellek adresi. Kod oluşturma, bu olay için olay işleyicisidir.  
  
 `ppse`  
 [out] Bir işaretçiye alan değişkenin adresini `IScriptEntry` belirtilen öznitelikleri ayrıldığında arabirimi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iactivescriptauthor arabirimi](../../winscript/reference/iactivescriptauthor-interface.md)   
 [IScriptEntry Arabirimi](../../winscript/reference/iscriptentry-interface.md)