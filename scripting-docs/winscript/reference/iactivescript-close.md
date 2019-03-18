---
title: IActiveScript::Close | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.Close
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_Close
ms.assetid: cc7dd63b-1d7e-410a-857b-09ea3aade275
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 53b71471ada55751de301391fdcc70387c1bb6c2
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58157055"
---
# <a name="iactivescriptclose"></a>IActiveScript::Close
Yüklü tüm betik iptal durumuna kaybetmek ve bu nedenle bir kapalı durumuna girmesini diğer nesnelere sahip herhangi bir arabirim işaretçilerini yayın komut dosyası altyapısı neden olur. Olay havuzlarını hemen çalıştırılan komut metni ve devam etmekte olan makro çağrısı durum değişikliklerini önce tamamlanır (kullanın [IActiveScript::InterruptScriptThread](../../winscript/reference/iactivescript-interruptscriptthread.md) çalışan bir betik iş parçacığının iptal etmek için). Döngüsel başvuru sorunları önlemek için arabirim yayımlanmadan önce bu yöntemi oluşturma ana bilgisayar tarafından çağrılmalıdır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Close(void);  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|`S_OK`|Başarılı.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı zaten kapalı durumda olan).|  
|`OLESCRIPT_S_PENDING`|Yöntemi başarıyla kuyruğa alındı, ancak durumu henüz değişmedi. Durum değişiklikleri site olduğunda üzerinde aranmak [IActiveScriptSite::OnStateChange](../../winscript/reference/iactivescriptsite-onstatechange.md) yöntemi.|  
|`S_FALSE`|Yöntem başarılı oldu, ancak komut zaten kapatıldı.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript](../../winscript/reference/iactivescript.md)