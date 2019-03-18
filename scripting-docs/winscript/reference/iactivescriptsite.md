---
title: Iactivescriptsite | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptSite interface
ms.assetid: 4d604a11-5365-46cf-ab71-39b3dbbe9f22
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 67e16e2825f03c9ae452e639d6a086bee584ac95
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58152648"
---
# <a name="iactivescriptsite"></a>IActiveScriptSite
Windows komut dosyası altyapısı için bir site oluşturmak için ana bilgisayar tarafından uygulanır. Genellikle, bu site (örneğin, ActiveX denetimlerini) komut dosyası için görünür olan tüm nesnelerin kapsayıcısı ile ilişkilendirilecek. Genellikle, bu kapsayıcı, belge veya görüntülenen sayfasına karşılık gelir. Microsoft Internet Explorer, örneğin, görüntülenen her bir HTML sayfası için bir tür bir kapsayıcı oluşturursunuz. Her bir ActiveX denetimi (veya diğer Otomasyon nesnesi) sayfasında ve komut dosyası altyapısı kendisini bu kapsayıcıda numaralandırılabilir.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|||  
|-|-|  
|Yöntem|Açıklama|  
|[IActiveScriptSite::GetLCID](../../winscript/reference/iactivescriptsite-getlcid.md)|Kullanıcı arabirimi öğelerini görüntülemek için konağın kullandığı yerel ayar tanımlayıcısını alır.|  
|[IActiveScriptSite::GetItemInfo](../../winscript/reference/iactivescriptsite-getiteminfo.md)|Altyapının yapılan bir çağrıyla eklenmiş olan bir öğe hakkında bilgi edinir [IActiveScript::AddNamedItem](../../winscript/reference/iactivescript-addnameditem.md) yöntemi.|  
|[IActiveScriptSite::GetDocVersionString](../../winscript/reference/iactivescriptsite-getdocversionstring.md)|Geçerli belge sürümü ana bilgisayarın açısından benzersiz olarak tanımlayan ve ana bilgisayar tanımlı bir dize alır.|  
|[IActiveScriptSite::OnScriptTerminate](../../winscript/reference/iactivescriptsite-onscriptterminate.md)|Betik yürütmeyi tamamladığında çağrılır.|  
|[IActiveScriptSite::OnStateChange](../../winscript/reference/iactivescriptsite-onstatechange.md)|Konak, komut dosyası altyapısı durumları değiştiğini bildirir.|  
|[IActiveScriptSite::OnScriptError](../../winscript/reference/iactivescriptsite-onscripterror.md)|Ana bilgisayara altyapısı betik çalıştırılırken bir yürütme hatası oluştu bildirir.|  
|[IActiveScriptSite::OnEnterScript](../../winscript/reference/iactivescriptsite-onenterscript.md)|Konak, komut dosyası altyapısı betik kodu yürüten başlatıldığını bildirir.|  
|[IActiveScriptSite::OnLeaveScript](../../winscript/reference/iactivescriptsite-onleavescript.md)|Konak, komut dosyası altyapısı betik kodu yürütülmesini döndürdüğünü bildirir.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Arabirimleri](../../winscript/reference/active-script-interfaces.md)