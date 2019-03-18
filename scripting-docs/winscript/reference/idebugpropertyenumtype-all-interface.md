---
title: Idebugpropertyenumtype_all arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugPropertyEnumType_All
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugPropertyEnumType_All interface
ms.assetid: 4d0f4fd5-e5f7-47cb-b746-860d6363e2cd
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b9ddd9fb24aa83a6027d6d705de6a748a96b2e28
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58149308"
---
# <a name="idebugpropertyenumtypeall-interface"></a>IDebugPropertyEnumType_All Arabirimi
`IDebugPropertyEnumType` Arabirimleri, böylece her biri kendi IID'leri filtre olarak geçirilebilir tanımlanır `IDebugProperty::EnumMembers` uygun Numaralandırıcı isteyen oluştu.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
IDebugPropertyEnumType_All : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugPropertyEnumType_All::GetName](../../winscript/reference/idebugpropertyenumtype-all-getname.md)|Adı açıklayan bir metin dizesi döndürür|  
  
 Aşağıdaki arabirimlerinden devralır `IDebugPropertyEnumType_All`, ve hiçbir ek yöntemleri vardır.  
  
```cpp
IDebugPropertyEnumType_Arguments : IDebugPropertyEnumType_All   
IDebugPropertyEnumType_Locals : IDebugPropertyEnumType_All   
IDebugPropertyEnumType_LocalsPlusArgs : IDebugPropertyEnumType_All   
IDebugPropertyEnumType_Registers : IDebugPropertyEnumType_All  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProperty::EnumMembers](../../winscript/reference/idebugproperty-enummembers.md)