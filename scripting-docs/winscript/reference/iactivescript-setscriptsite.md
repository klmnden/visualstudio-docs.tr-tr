---
title: IActiveScript::SetScriptSite | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 3fdf5f3ae84d1a991d67170b5f2b02114b91ee05
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58157074"
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