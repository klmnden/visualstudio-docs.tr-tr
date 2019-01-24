---
title: IDiaStackWalkHelper::get_registerValue | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalkHelper2::get_registerValue method
ms.assetid: 46ac5eee-73a3-44a1-8635-6c58ba193cb6
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 4dde30ebcda46d75271b15ec5b7f7c1ac49f384b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54788611"
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
