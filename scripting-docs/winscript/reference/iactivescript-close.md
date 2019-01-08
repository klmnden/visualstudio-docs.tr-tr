---
title: IActiveScript::Close | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 886ab1c4c39cf7c64571862bfd28f2fbd1062694
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097051"
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