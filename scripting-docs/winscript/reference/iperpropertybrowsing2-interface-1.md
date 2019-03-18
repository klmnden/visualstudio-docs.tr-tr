---
title: Iperpropertybrowsing2 arabirimi 1 | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IPerPropertyBrowsing2
apilocation:
- scrobj.dll
helpviewer_keywords:
- IPerPropertyBrowsing2 interface
ms.assetid: 1e50b3f7-cc1c-495a-93c7-3ee03aea0b8a
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 156cf9a1e104b8a2d7ffe4e48bd39642ef1abbd0
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58159588"
---
# <a name="iperpropertybrowsing2-interface-1"></a>Iperpropertybrowsing2 arabirimi 1
Erişim bilgiler özellik sayfaları, bir nesne tarafından sunulan.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|`GetDisplayString`|Belirtilen özellik açıklayan bir metin dizesi döndürür.|  
|`MapPropertyToPage`|Belirtilen özellik işlenmesini izin veren özellik sayfasını CLSID değeri döndürür.|  
|`GetPredefinedStrings`|Sayılan bir dizisini döndürür (`LPOLESTR` işaretçiler) açıklamaları belirtilen özellik kabul edebilen izin verilen değerler listesi.|  
|`SetPredefinedValue`|Özelliğinin değeri, belirteci tarafından tanımlanan önceden tanımlanmış değere ayarlar. `dwCookie.`|  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: dbgprop.h