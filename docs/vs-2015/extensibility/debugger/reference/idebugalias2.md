---
title: IDebugAlias2 | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- IDebugAlias2 interface
ms.assetid: 5252dcbb-8bfe-4d8a-a8e5-b022b194df19
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a8e1fb2ee13b41d1b41961d0a24a2da0bc852660
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49307605"
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
 Üstbilgi: Ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

