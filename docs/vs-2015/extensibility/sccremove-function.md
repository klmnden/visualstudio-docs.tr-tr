---
title: SccRemove işlevi | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- SccRemove
helpviewer_keywords:
- SccRemove function
ms.assetid: 20830fdc-c0e9-4a5f-bf60-33f28874442f
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 85e1eb8a4929462e92d848738c4e6e2d15fbc209
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49254026"
---
# <a name="sccremove-function"></a>SccRemove İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu işlev, kaynak denetim sisteminden dosyaları siler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
SCCRTN SccRemove(  
   LPVOID    pvContext,  
   HWND      hWnd,  
   LONG      nFiles,  
   LPCSTR*   lpFileNames,  
   LPCSTR    lpComment,  
   LONG      fOptions,  
   LPCMDOPTS pvOptions  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 pvContext  
 [in] Kaynak Denetimi Eklentisi bağlam yapısı.  
  
 hWnd  
 [in] Kaynak Denetimi Eklentisi sağladığı herhangi bir iletişim kutusu için bir üst öğe olarak kullanabileceğiniz IDE penceresi için bir tanıtıcı.  
  
 nFiles  
 [in] Belirtilen dosya sayısı `lpFileNames` dizisi.  
  
 lpFileNames  
 [in] Dosyaların kaldırılması için tam yerel yol adları dizisi.  
  
 lpComment  
 [in] Kaldırılmakta olan her dosyaya uygulanacak açıklama.  
  
 fOptions  
 [in] Komut bayrakları (kullanılmayan).  
  
 pvOptions  
 [in] Kaynak denetimi fişi özel seçenekleri.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|SCC_OK|Temizleme başarılı oldu.|  
|SCC_E_FILENOTCONTROLLED|Seçili dosya kaynak denetimi altında değil.|  
|SCC_E_OPNOTSUPPORTED|Kaynak denetim sistemi bu işlemi desteklemiyor.|  
|SCC_E_ISCHECKEDOUT|Bir dosya, bir kullanıcı şu anda kullanıma sahip olduğundan kaldırılamıyor.|  
|SCC_E_ACCESSFAILURE|Kaynak denetim sistemi, ağ veya çakışma sorunları nedeniyle muhtemelen erişilirken sorun oluştu.|  
|SCC_E_NOTAUTHORIZED|Kullanıcı bu işlemi gerçekleştirmek için izin verilmiyor.|  
|SCC_E_NONSPECIFICERROR|Belirli olmayan hata; Dosya kaldırılmadı.|  
|SCC_I_OPERATIONCANCELED|İşlem tamamlanmadan önce iptal edildi.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu işlev, kaynak denetim sisteminden dosyaları kaldırır ancak kullanıcının yerel disk sürücünüzden silinmez.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)

