---
title: Iperpropertybrowsing2 arabirimi 1 | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: bded7159b72fc8c1ae8408611ce858105e6734da
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54344049"
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