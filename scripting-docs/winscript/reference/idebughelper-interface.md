---
title: Idebughelper arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugHelper interface
ms.assetid: ef5691e0-1d82-42c2-997c-888e31c478dd
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d1708b742a484a2e7d6d48cf759f15c08711e13d
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58148066"
---
# <a name="idebughelper-interface"></a>IDebugHelper Arabirimi
Nesne tarayıcı ve basit bağlantı noktaları için bir üreteci olarak görev yapar. İşlem Hata Ayıklama Yöneticisi (PDM) komut dosyası motoru tarafından kullanılan bu arabirimi uygular.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDebugHelper` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugHelper::CreatePropertyBrowser](../../winscript/reference/idebughelper-createpropertybrowser.md)|Bir değişken sarmalayan bir özellik tarayıcısı döndürür.|  
|[IDebugHelper::CreatePropertyBrowserEx](../../winscript/reference/idebughelper-createpropertybrowserex.md)|Bir değişken sarmalar ve değişken değerlerini VARTYPE türleri veya özel dönüştürme dizeleri için sağlayan bir özellik tarayıcısı döndürür.|  
|[IDebugHelper::CreateSimpleConnectionPoint](../../winscript/reference/idebughelper-createsimpleconnectionpoint.md)|Sarmalayan bir olay arabirimi döndüren bir verilen `IDispatch` nesne.|