---
title: Sccdirqueryınfo işlevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- SccDirQueryInfo
helpviewer_keywords:
- SccDirQueryInfo function
ms.assetid: 459e2d99-573d-47c4-b834-6d82c5e14162
caps.latest.revision: 15
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 7334ddd1ce6c7f9feac63253246e55b65121e18b
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63432447"
---
# <a name="sccdirqueryinfo-function"></a>SccDirQueryInfo İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu işlev, bunların geçerli durum için tam dizinler listesini inceler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
SCCRTN SccDirQueryInfo(  
LPVOID  pContext,  
LONG    nDirs,  
LPCSTR* lpDirNames,  
LPLONG  lpStatus  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 pContext  
 [in] Kaynak Denetimi Eklentisi bağlam yapısı.  
  
 nDirs  
 [in] Sorgulanacak seçili dizinleri sayısı.  
  
 lpDirNames  
 [in] Sorgulanacak dizinlerin tam yollarının dizisi.  
  
 lpStatus  
 [out içinde] Kaynak denetimi durumu bayrakları döndürülecek eklentisi için bir dizi yapısı (bkz [dizin durumu kod](../extensibility/directory-status-code-enumerator.md) Ayrıntılar için).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|SCC_OK|Sorgu başarılı oldu.|  
|SCC_E_OPNOTSUPPORTED|Kaynak kodu denetim sistemi bu işlemi desteklemiyor.|  
|SCC_E_ACCESSFAILURE|Kaynak denetim sistemi, ağ veya çakışma sorunları nedeniyle muhtemelen erişilirken sorun oluştu. Bir yeniden deneme önerilir.|  
|SCC_E_NONSPECIFICERROR<br /><br /> SCC_E_UNKNOWNERROR|Belirli olmayan hata oluştu.|  
  
## <a name="remarks"></a>Açıklamalar  
 İşlev dönüş dizi bitten'ın bir bit maskesi ile doldurur `SCC_DIRSTATUS` ailesi (bkz [dizin durumu kod](../extensibility/directory-status-code-enumerator.md)), verilen her dizin için bir giriş. Durum dizi arayan tarafından ayrılmış.  
  
 Bir dizine karşılık gelen bir proje sahip olup olmadığını sorgulayarak dizini kaynak denetimi altında olup olmadığını denetlemek için yeniden adlandırmadan önce IDE bu işlevi kullanır. Dizin, kaynak denetimi altında değilse, IDE kullanıcıya uygun uyarı sağlayabilir.  
  
> [!NOTE]
> Kaynak Denetimi Eklentisi, bir veya daha fazla durum değerleri uygulamak seçerse uygulanmayan BITS sıfır olarak ayarlanması gerekir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)   
 [Dizin Durumu Kodu](../extensibility/directory-status-code-enumerator.md)
