---
title: IDebugSourceServerModule | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- IDebugSourceServerModule interface
ms.assetid: 38213060-451d-46e6-8b4a-efc123e01a2c
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 0dec9408d0cd1907a533a8cabe740832fe652398
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62555702"
---
# <a name="idebugsourceservermodule"></a>IDebugSourceServerModule
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

PDB dosyasında yer alan kaynak sunucu bilgileri temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugSourceServerModule : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu arabirim hata ayıklayıcı motoru tarafından uygulanan ve kullanıcı Arabirimi hata ayıklayıcı tarafından tüketilen.  
  
## <a name="methods"></a>Yöntemler  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugSourceServerModule`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetSourceServerData](../../../extensibility/debugger/reference/idebugsourceservermodule-getsourceserverdata.md)|Kaynak sunucu bilgileri alır.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll
