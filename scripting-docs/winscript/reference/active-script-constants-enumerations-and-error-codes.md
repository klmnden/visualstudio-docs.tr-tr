---
title: Etkin betik sabitleri, numaralandırmaları ve hata kodları | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: aab24471-5817-45c0-be07-ffe4648923ed
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 090b494e904fbef1c0d3d8b380f7a184a6042788
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62954004"
---
# <a name="active-script-constants-enumerations-and-error-codes"></a>Etkin Komut Dosyası Sabitleri, Numaralandırmaları ve Hata Kodları
Bu bölümde, numaralandırmalar ve Windows komut dosyası altyapısına kullanılan hata kodları açıklanmaktadır.  
  
## <a name="constants"></a>Sabitler  
  
|Sabit|Açıklama|  
|--------------|-----------------|  
|[SCRIPTTHREADID Sabitleri](../../winscript/reference/scriptthreadid-constants.md)|İş parçacığı türünü belirtir.|  
  
## <a name="properties"></a>Özellikler  
  
|Özellik|Açıklama|  
|--------------|-----------------|  
|[SCRIPTPROP_HOSTKEEPALIVE Özelliği](../../winscript/reference/scriptprop-hostkeepalive-property.md)|Komut dosyası altyapısı bekleyen başvuru olduğunda tam işlevsel tutulması gereken olup olmadığını belirtmek için kullanılır.|  
  
## <a name="enumerations"></a>Numaralandırmalar  
  
|Sabit Listesi|Açıklama|  
|-----------------|-----------------|  
|[SCRIPTGCTYPE Sabit Listesi](../../winscript/reference/scriptgctype-enumeration.md)|Gerçekleştirilecek çöp toplama türü.|  
|[SCRIPTLANGUAGEVERSION Sabit Listesi](../../winscript/reference/scriptlanguageversion-enumeration.md)|Sürümleri betik olası belirtir.|  
|[SCRIPTSTATE Sabit Listesi](../../winscript/reference/scriptstate-enumeration.md)|Bir komut dosyası altyapısı durumunu belirtir.|  
|||  
|[SCRIPTTHREADSTATE Sabit Listesi](../../winscript/reference/scriptthreadstate-enumeration.md)|Bir komut dosyası altyapısı bir iş parçacığı durumunu belirtir.|  
|[SCRIPTTRACEINFO Sabit Listesi](../../winscript/reference/scripttraceinfo-enumeration.md)|İzlenen betik olayı temsil eder. Kullanılan [Iactivescriptsitetraceınfo::sendscripttraceınfo yöntemi](../../winscript/reference/iactivescriptsitetraceinfo-sendscripttraceinfo-method.md).|  
|[SCRIPTUICHANDLING Sabit Listesi](../../winscript/reference/scriptuichandling-enumeration.md)|UI denetimi işleneceğini yolunu temsil eder.|  
|[SCRIPTUICITEM Sabit Listesi](../../winscript/reference/scriptuicitem-enumeration.md)|Kullanıcı Arabirimi öğesi türünü temsil eder. Kullanılan [Iactivescriptsiteuıcontrol::getuıbehavior metodu](../../winscript/reference/iactivescriptsiteuicontrol-getuibehavior-method.md).|  
  
## <a name="error-codes"></a>Hata Kodları  
  
|Hata Kodu|Açıklama|  
|----------------|-----------------|  
|[SCRIPT_E_PROPAGATE Hata Kodu](../../winscript/reference/script-e-propagate-error-code.md)|Bir betik hatası farklı bir iş parçacığında olabilir çağırana yayılır.|  
|[SCRIPT_E_RECORDED Hata Kodu](../../winscript/reference/script-e-recorded-error-code.md)|Bir hata, komut dosyası altyapısı ile konak geçirildi.|  
|[SCRIPT_E_REPORTED Hata Kodu](../../winscript/reference/script-e-reported-error-code.md)|Komut dosyası altyapısı konağa işlenmeyen bir özel durum bildirdi.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Arabirimleri](../../winscript/reference/active-script-interfaces.md)