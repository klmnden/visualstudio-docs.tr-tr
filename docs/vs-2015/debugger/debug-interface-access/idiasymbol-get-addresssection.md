---
title: Idiasymbol::get_addresssection | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_addressSection method
ms.assetid: fe80d479-3bb5-4f55-9b62-1bd58d0a60ce
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 85e6ffac13f25e79f51af13ac134cf538e6af5af
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "64782513"
---
# <a name="idiasymbolgetaddresssection"></a>IDiaSymbol::get_addressSection
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Adres konum bölüm parçası alır. Şu durumlarda kullanın [LocationType numaralandırması](../../debugger/debug-interface-access/locationtype.md) ayarlanır `LocIsStatic`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT get_addressSection (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Adres konum bölüm bölümünü döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için mevcut olmadığı anlamına gelir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem sanal adres üyenin edinmek alacağından dış bir DLL içinde yer alan statik üyeleri için bu yöntem tarafından döndürülen bölüm 0 olabilir. Sanal adres geçerli yalnızca [Idiasession::put_loadaddress](../../debugger/debug-interface-access/idiasession-put-loadaddress.md) yönteminde [Idiasession](../../debugger/debug-interface-access/idiasession.md) arabirimi çağrılıp çağrılmadığını DLL yük adresini belirtmek için sıfır olmayan bir parametre.  
  
 Bir adresi uzaklık parçası almak için arama [Idiasymbol::get_addressoffset](../../debugger/debug-interface-access/idiasymbol-get-addressoffset.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
  
|Gereksinim|Açıklama|  
|-----------------|-----------------|  
|Üst bilgi:|dia2.h|  
|Sürüm:|DIA SDK v7.0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [LocationType Numaralandırması](../../debugger/debug-interface-access/locationtype.md)
