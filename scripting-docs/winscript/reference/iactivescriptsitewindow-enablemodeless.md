---
title: IActiveScriptSiteWindow::EnableModeless | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 4cea23890539ca80abf8e3e58b0f8c48b7ca1fc9
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54093021"
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