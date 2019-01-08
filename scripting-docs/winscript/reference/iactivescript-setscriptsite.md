---
title: IActiveScript::SetScriptSite | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.SetScriptSite
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_SetScriptSite
ms.assetid: 47d94c32-09f8-4539-ac56-0236026f627b
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b2a96732e904c7249dc5228ef414c3315012ec56
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097441"
---
# <a name="iactivescriptsetscriptsite"></a>IActiveScript::SetScriptSite
Komut dosyası altyapısı, bildirir [Iactivescriptsite](../../winscript/reference/iactivescriptsite.md) ana bilgisayar tarafından sağlanan arabirim site. Diğer önce bu yöntemi çağıran [IActiveScript](../../winscript/reference/iactivescript.md) arabirim yöntemleri kullanılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SetScriptSite(  
    IActiveScriptSite *pScriptSite  // address of host script site  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pScriptSite`  
 [in] Komut dosyası altyapısının Bu örnekle ilişkilendirilecek komut dosyası ana bilgisayarı tarafından sağlanan site adresi. Site, bu komut dosyası altyapısı örneği için benzersiz olarak atanmalıdır; diğer komut dosyası altyapıları ile paylaşılamaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_FAIL`|Belirtilmeyen bir hata oluştu; komut dosyası altyapısı sitesi başlatılıyor tamamlayamadı.|  
|`E_INVALIDARG`|Bir bağımsız değişken geçersiz.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, bir site zaten ayarlanmış).|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript](../../winscript/reference/iactivescript.md)