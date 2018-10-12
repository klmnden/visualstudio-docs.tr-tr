---
title: IDebugComPlusSymbolProvider2 | Microsoft Docs
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
- IDebugComPlusSymbolProvider2 interface
ms.assetid: fa2f9b49-03ad-43c7-92d6-6dcb9c3d0531
caps.latest.revision: 7
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6aed363d7f3571fa26d291858ce63ba654afaec1
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49186231"
---
# <a name="idebugcomplussymbolprovider2"></a>IDebugComPlusSymbolProvider2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Yönetilen kod için özel yöntemler ile bir COM + simgesi sağlayıcısını temsil eder ve genişleten **IDebugComPlusSymbolProvider**[IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugComPlusSymbolProvider2 : IDebugComPlusSymbolProvider  
```  
  
## <a name="methods"></a>Yöntemler  
 Yöntemlere ek olarak [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md) arabirimi bu arabirim, aşağıdaki yöntemleri uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[FunctionHasLineInfo](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2-functionhaslineinfo.md)|Belirtilen yöntem satır bilgileri olup olmadığını belirler.|  
|[GetTypesByName](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2-gettypesbyname.md)|Adı verilen bir türü alır.|  
|[GetTypeFromToken](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2-gettypefromtoken.md)|Kendi belirteci verilen bir türü alır.|  
|[IsAddressSequencePoint](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2-isaddresssequencepoint.md)|Belirtilen hata ayıklama adresi bir dizi noktası olup olmadığını belirler.|  
|[LoadSymbolsFromCallback](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2-loadsymbolsfromcallback.md)|Yükler, belirtilen geri çağırma yöntemi kullanarak simgeleri hata ayıklayın.|  
|[LoadSymbolsFromStreamWithCorModule](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2-loadsymbolsfromstreamwithcormodule.md)|Verilen veri akışından hata ayıklama sembolleri **Icordebugmodule** nesne.|  
|[LoadSymbolsWithCorModule](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2-loadsymbolswithcormodule.md)|Yükleri hata ayıklama sembolleri verilen **Icordebugmodule** nesne.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

