---
title: IActiveScript | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScript interface
ms.assetid: d8acee11-7f0d-4999-b97a-66774af16f71
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5b7e3a0172a798eab9a743f446dff3d339a785b2
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58151005"
---
# <a name="iactivescript"></a>IActiveScript
Komut dosyası altyapısı'nı başlatmak için gereken yöntemleri sağlar. Komut dosyası altyapısı uygulamalıdır `IActiveScript` arabirimi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScript::SetScriptSite](../../winscript/reference/iactivescript-setscriptsite.md)|Komut dosyası altyapısı, bildirir [Iactivescriptsite](../../winscript/reference/iactivescriptsite.md) ana bilgisayar tarafından sağlanan site.|  
|[IActiveScript::GetScriptSite](../../winscript/reference/iactivescript-getscriptsite.md)|Windows komut dosyası motoruyla ilişkili site nesnesi alır.|  
|[IActiveScript::SetScriptState](../../winscript/reference/iactivescript-setscriptstate.md)|Komut dosyası altyapısı, belirtilen bir duruma koyar.|  
|[IActiveScript::GetScriptState](../../winscript/reference/iactivescript-getscriptstate.md)|Komut dosyası altyapısının geçerli durumunu alır.|  
|[IActiveScript::Close](../../winscript/reference/iactivescript-close.md)|Yüklü tüm betik iptal durumuna kaybetmek ve bu nedenle bir kapalı durumuna girmesini diğer nesnelere sahip herhangi bir arabirim işaretçilerini yayın komut dosyası altyapısı neden olur.|  
|[IActiveScript::AddNamedItem](../../winscript/reference/iactivescript-addnameditem.md)|Komut dosyası altyapısının ad alanı için bir kök düzey öğesi adını ekler.|  
|[IActiveScript::AddTypeLib](../../winscript/reference/iactivescript-addtypelib.md)|Komut dosyası için ad alanı için bir tür kitaplığı ekler.|  
|[IActiveScript::GetScriptDispatch](../../winscript/reference/iactivescript-getscriptdispatch.md)|Alır `IDispatch` çalışan betik için arabirim.|  
|[IActiveScript::GetCurrentScriptThreadID](../../winscript/reference/iactivescript-getcurrentscriptthreadid.md)|Şu anda çalışan bir iş parçacığı için bir komut dosyası altyapısı-tanımlı tanımlayıcı alır.|  
|[IActiveScript::GetScriptThreadID](../../winscript/reference/iactivescript-getscriptthreadid.md)|Belirli Microsoft Win32 iş parçacığı ile ilişkili iş parçacığı için bir komut dosyası altyapısı-tanımlı tanımlayıcı alır.|  
|[IActiveScript::GetScriptThreadState](../../winscript/reference/iactivescript-getscriptthreadstate.md)|Bir betik iş parçacığı geçerli durumunu alır.|  
|[IActiveScript::InterruptScriptThread](../../winscript/reference/iactivescript-interruptscriptthread.md)|Çalışan bir betik iş parçacığının yürütülmesini keser.|  
|[IActiveScript::Clone](../../winscript/reference/iactivescript-clone.md)|Geçerli iş parçacığındaki hiçbir sitede yüklü bir komut dosyası altyapısı döndüren geçerli komut dosyası altyapısı (tüm geçerli yürütme durumu), eksi kopyalar.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Windows Betik Arabirimleri Başvurusu](../../winscript/reference/windows-script-interfaces-reference.md)