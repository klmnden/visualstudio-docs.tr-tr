---
title: IDebugAlias2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- IDebugAlias2 interface
ms.assetid: 5252dcbb-8bfe-4d8a-a8e5-b022b194df19
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 2349203c49bc164bb3af6bcf51e39afb56022be0
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54783667"
---
# <a name="idebugalias2"></a>IDebugAlias2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Bir değişken için sayısal bir diğer adı temsil eder ve bir ifade değerlendiricisi uygulama etki alanı diğer adı için elde edilir (EE) sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugAlias2 : IDebugAlias  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu arabirim yönetilen hata ayıklama altyapısı (DE) tarafından uygulanır.  
  
## <a name="methods"></a>Yöntemler  
 Yöntemlere ek olarak [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md) arabirimi bu arabirim, aşağıdaki yöntemi uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetAppDomainId](../../../extensibility/debugger/reference/idebugalias2-getappdomainid.md)|Uygulama etki alanı için tanımlayıcıyı alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir diğer ad, sonrasında # karakteri, örneğin, 1001 # dize biçiminde bir ondalık sayıdır.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Ee.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll
