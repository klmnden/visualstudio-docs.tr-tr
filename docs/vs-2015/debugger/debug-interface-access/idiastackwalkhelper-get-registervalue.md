---
title: IDiaStackWalkHelper::get_registerValue | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalkHelper2::get_registerValue method
ms.assetid: 46ac5eee-73a3-44a1-8635-6c58ba193cb6
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6c4e8c7c40a1110651451e64b98708713d54e4a5
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49853109"
---
# <a name="idiastackwalkhelpergetregistervalue"></a>IDiaStackWalkHelper::get_registerValue
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir kayıt değeri alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT get_registerValue (   
   DWORD      index,  
   ULONGLONG* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `index`  
 [in] Bir değer [CV_HREG_e numaralandırması](../../debugger/debug-interface-access/cv-hreg-e.md) hangi değerin alınacağı kaydetme belirten sabit listesi.  
  
 `pRetVal`  
 [out] Kayıt geçerli değerini döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Boyutu rağmen `pRetVal` parametresi, bir uygulama yalnızca ne kasa normalde tutan depolamanız gerekir. Örneğin, yalnızca düşük 8 bitlik verilen değer 8-bit kayıt tutar. Bu 8-bit değeri, 64-bit Bu yöntemden döndürülen genişletilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md)   
 [CV_HREG_e Numaralandırması](../../debugger/debug-interface-access/cv-hreg-e.md)



