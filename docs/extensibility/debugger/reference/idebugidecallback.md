---
title: IDebugIDECallback | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugIDECallback interface
ms.assetid: 8d31adc0-1c44-4658-8d4f-f4b73e35f4a6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d05b2ab4c4944cbcce7f920f86eec0ca2f93865a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55008224"
---
# <a name="idebugidecallback"></a>IDebugIDECallback
> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Hata ayıklayıcının çıkış penceresinde bir ileti görüntülemek bir ifade değerlendiricisi (EE) sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugIDECallback : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu geri çağırma yönetilen hata ayıklama altyapısı tarafından gerçekleştirilir.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Çıkış hata ayıklayıcının çıkış penceresinde göndermek için bir ifade değerlendiricisi tarafından tüketilebilir.  
  
## <a name="methods"></a>Yöntemler  
 Bu arabirim, aşağıdaki yöntemi uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[DisplayMessage](../../../extensibility/debugger/reference/idebugidecallback-displaymessage.md)|Belirtilen ileti dizesi hata ayıklayıcının çıkış penceresinde gönderir.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Ee.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll