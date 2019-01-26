---
title: SccCheckout işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccCheckout
helpviewer_keywords:
- SccCheckout function
ms.assetid: 06e9ecd7-fc09-40c1-9dd1-2b56c622c80b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2a01ee4e4010782570d267d5b2e35d56fedb45a1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54984983"
---
# <a name="scccheckout-function"></a>SccCheckout işlevi
Tam olarak nitelenmiş dosya adlarının bir listesini göz önünde bulundurulduğunda, bu işlev bunları yerel sürücüye kullanıma. Açıklama kullanıma alınan tüm dosyalar için geçerlidir. Açıklama bağımsız değişken olabilir bir `null` dize.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
SCCRTN SccCheckout (  
   LPVOID    pvContext,  
   HWND      hWnd,  
   LONG      nFiles,  
   LPCSTR*   lpFileNames,  
   LPCSTR    lpComment,  
   LONG      fOptions,  
   LPCMDOPTS pvOptions  
);  
```  
  
### <a name="parameters"></a>Parametreler  
 pvContext  
 [in] Kaynak Denetimi Eklentisi bağlam yapısı.  
  
 hWnd  
 [in] Kaynak Denetimi Eklentisi sağladığı herhangi bir iletişim kutusu için bir üst öğe olarak kullanabileceğiniz IDE penceresi için bir tanıtıcı.  
  
 nFiles  
 [in] Kullanıma alınması için seçilen dosya sayısı.  
  
 lpFileNames  
 [in] Dosya kullanıma alınması tam yerel yol adları dizisi.  
  
 lpComment  
 [in] Seçili dosyaları kullanıma alınmış uygulanması için açıklama.  
  
 fOptions  
 [in] Komut bayrakları (bkz [özel komutlar tarafından kullanılan bit bayrakları](../extensibility/bitflags-used-by-specific-commands.md)).  
  
 pvOptions  
 [in] Kaynak denetimi fişi özel seçenekleri.  
  
## <a name="return-value"></a>Dönüş değeri  
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|SCC_OK|Kullanıma alma başarılı oldu.|  
|SCC_E_FILENOTCONTROLLED|Seçili dosya kaynak kodu denetimi altında değil.|  
|SCC_E_ACCESSFAILURE|Kaynak denetim sistemi, ağ veya çakışma sorunları nedeniyle muhtemelen erişilirken sorun oluştu. Bir yeniden deneme önerilir.|  
|SCC_E_NOTAUTHORIZED|Kullanıcı bu işlemi gerçekleştirmek için izin verilmiyor.|  
|SCC_E_NONSPECIFICERROR|Belirli olmayan hata oluştu. Dosya kullanıma alındı değil.|  
|SCC_E_ALREADYCHECKEDOUT|Kullanıcının kullanıma alınmış dosyası zaten var.|  
|SCC_E_FILEISLOCKED|Yeni sürümler oluşturulması yasaklanması dosyası kilitli.|  
|SCC_E_FILEOUTEXCLUSIVE|Başka bir kullanıcı, bu dosya bir özel kullanıma alma yapmıştır.|  
|SCC_I_OPERATIONCANCELED|İşlem tamamlanmadan önce iptal edildi.|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)   
 [Özel komutlar tarafından kullanılan bit bayrakları](../extensibility/bitflags-used-by-specific-commands.md)