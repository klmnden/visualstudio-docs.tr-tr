---
title: IActiveScriptSiteWindow::EnableModeless | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSiteWindow.EnableModeless
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSiteWindow_EnableModeless
ms.assetid: 83fe4f62-8e97-4f03-bc6f-d90aa888657d
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4f15135273b98a65903a5d03de87c541fc032cce
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992932"
---
# <a name="iactivescriptsitewindowenablemodeless"></a>IActiveScriptSiteWindow::EnableModeless
Etkinleştirmek veya kalıcı olmayan iletişim kutuları yanı sıra ana penceresi devre dışı bırakmak için ana neden olur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT EnableModeless(  
    BOOL fEnable  // enable flag  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `fEnable`  
 [in] Bayrak `TRUE`, kalıcı olmayan iletişim kutuları ve ana pencereyi etkinleştirir veya `FALSE`, bunları devre dışı bırakır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` başarılı olursa veya `E_FAIL` varsa bir hata oluştu.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem `IOleInPlaceFrame::EnableModeless` yöntemi.  
  
 Bu yönteme çağrıları yuvalanabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSiteWindow](../../winscript/reference/iactivescriptsitewindow.md)