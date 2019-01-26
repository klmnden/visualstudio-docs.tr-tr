---
title: SccGetEvents işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccGetEvents
helpviewer_keywords:
- SccGetEvents function
ms.assetid: 32f8147d-6dcc-465e-b07b-42da5824f9b0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7da9bce351ef8910f77713bf77d0f5f698193140
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54998319"
---
# <a name="sccgetevents-function"></a>SccGetEvents işlevi
Bu işlev, bir kuyruğa alınmış durumu olayı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
SCCRTN SccGetEvents (  
   LPVOID pvContext,  
   LPSTR  lpFileName,  
   LPLONG lpStatus,  
   LPLONG pnEventsRemaining  
);  
```  
  
### <a name="parameters"></a>Parametreler  
 pvContext  
 [in] Kaynak Denetimi Eklentisi bağlam yapısı.  
  
 lpFileName  
 [out içinde] Arabellek burada verilen dosya adı (en çok _MAX_PATH karakter) kaynak denetimi eklentisi koyar.  
  
 lpStatus  
 [out içinde] Durum kodu döndürür (bkz [durum kodu dosyası](../extensibility/file-status-code-enumerator.md) olası değerler için).  
  
 pnEventsRemaining  
 [out içinde] Kuyrukta Bu çağrıdan sonra sol girdi sayısı bu değeri döndürür. Bu sayı büyükse, çağırana çağırmak karar verebilir [Sccqueryınfo](../extensibility/sccqueryinfo-function.md) tüm bilgileri bir kerede alınacak.  
  
## <a name="return-value"></a>Dönüş değeri  
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|SCC_OK|Başarılı etkinlikleri alın.|  
|SCC_E_OPNOTSUPPORTED|Bu işlev desteklenmiyor.|  
|SCC_E_NONSPECIFICERROR|Belirli olmayan hata oluştu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu işlev boş bir durum güncelleştirmeleri için kaynak denetimi altında dosyaların yapılmadığını görmek için işleme sırasında çağrılır. Kaynak Denetimi Eklentisi bilir tüm dosyaların durumunu korur ve bir değişiklik olduğunda durumu belirtilmiştir eklenti tarafından durumu ve ilişkili dosya bir sırada depolanır. Zaman `SccGetEvents` çağrılır, üst öğe kuyruğun alınır ve döndürülür. Bu işlev yalnızca daha önce önbelleğe alınmış bilgileri döndürmek için kısıtlanmış ve (diğer bir deyişle, disk okuma veya kaynak denetim sistemi durumunun isteyen); çok hızlı bir döngü olmalıdır Aksi takdirde IDE performansının düşmesine başlayabilir.  
  
 Rapor için durum güncelleştirme varsa, kaynak denetimi eklentisi boş bir dize tarafından işaret edilen arabellek depolar `lpFileName`. Dosyanın tam yol adını eklenti'Aksi takdirde, depolar, durum bilgileri değişti ve uygun durum kodunu döndürür (ayrıntılı değerlerinden [durum kodu dosyası](../extensibility/file-status-code-enumerator.md)).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)   
 [Dosya durum kodu](../extensibility/file-status-code-enumerator.md)