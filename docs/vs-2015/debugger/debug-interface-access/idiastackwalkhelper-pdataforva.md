---
title: IDiaStackWalkHelper::pdataForVA | Microsoft Docs
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
- IDiaStackWalkHelper2::pdataByVA method
ms.assetid: fafc38fe-74dc-4726-9a51-eebf3a673d7f
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 525a19a997d5902da5d69d5804281d472b5d6a26
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49906227"
---
# <a name="idiastackwalkhelperpdataforva"></a>IDiaStackWalkHelper::pdataForVA
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Sanal adresle ilişkilendirilen PDATA veri bloğu döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT pdataForVA(   
   ULONGLONG  va,  
   DWORD      cbData,  
   DWORD*     pcbData,  
   BYTE*      pbData  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `va`  
 [in] Sanal adres edinmek için verilerin belirtir.  
  
 `cbData`  
 [in] Veri almak için bayt cinsinden boyutu.  
  
 `pcbData`  
 [out] Gerçek veri boyutunu edinilen bayt cinsinden döndürür.  
  
 `pbData`  
 [out içinde] İstenen veriler ile doldurulmuş bir arabellek. Olamaz `NULL`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` hiçbir PDATA belirtilen adresi için varsa. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 PDATA (".pdata" adlı bölümde) bir derlenecek özel durum işleme için işlevleri hakkında bilgi içerir.  
  
 Çağıran, arayan için ne kadar veri kullanılabilir isteyin gerek yoktur. Bu nedenle döndürülecek ne kadar veri olduğunu bilir. Bu nedenle, bu yöntemin bir hata ise döndürülecek bir uygulama için kabul edilebilir `pbData` parametresi `NULL`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md)



