---
title: Idisperror arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDispError interface
ms.assetid: 3dc7b55e-94ba-4669-b20a-1e011f2d07cf
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2c67ff6e458f8350ef36a8a454e017b3ce6ea114
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58144933"
---
# <a name="idisperror-interface"></a>IDispError Arabirimi
Ayrıntılı bağlamsal hata bilgilerini sağlar.  
  
> [!NOTE]
>  Bu arabirim gerçekleştirilmedi.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDispError` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDispError::QueryErrorInfo](../../winscript/reference/idisperror-queryerrorinfo.md)|Belirli bir tür hata bilgilerini alır.|  
|[IDispError::GetNext](../../winscript/reference/idisperror-getnext.md)|Sonraki alır `IDispError` nesne.|  
|[IDispError::GetHresult](../../winscript/reference/idisperror-gethresult.md)|Gelen hata kodunu alır `IDispError` nesne.|  
|[IDispError::GetSource](../../winscript/reference/idisperror-getsource.md)|Sınıf veya hataya neden olan uygulama için dile bağlı programlı tanımlayıcı döndürür.|  
|[IDispError::GetHelpInfo](../../winscript/reference/idisperror-gethelpinfo.md)|Yardım dosyasının yolu ve mümkünse, hatayı açıklayan bir konu bağlam Kimliğini döndürür.|  
|[IDispError::GetDescription](../../winscript/reference/idisperror-getdescription.md)|Hata metinsel açıklaması döndürür.|