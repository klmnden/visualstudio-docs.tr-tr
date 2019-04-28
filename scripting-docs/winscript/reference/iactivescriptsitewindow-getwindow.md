---
title: IActiveScriptSiteWindow::GetWindow | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSiteWindow.GetWindow
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSiteWindow_GetWindow
ms.assetid: 6284e38c-9dfb-4d69-903d-f243f78c0331
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7b6efa066765339375a8315695aa9c1de2f9c46b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992063"
---
# <a name="iactivescriptsitewindowgetwindow"></a>IActiveScriptSiteWindow::GetWindow
Komut dosyası altyapısı görüntülemelidir bir açılır pencere sahibi olarak davranıp bir pencere için işleme alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetWindow(  
    HWND *phwnd  // address of variable for window handle  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `phwnd`  
 [out] Pencere tanıtıcısı alan değişkenin adresi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` başarılı olursa veya `E_FAIL` varsa bir hata oluştu.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem benzer `IOleWindow::GetWindow` yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSiteWindow](../../winscript/reference/iactivescriptsitewindow.md)