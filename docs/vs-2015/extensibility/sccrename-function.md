---
title: SccRename işlevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- SccRename
helpviewer_keywords:
- SccRename function
ms.assetid: b467ade6-a1db-4c0b-b60f-7850ec4f79eb
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: e78975acab0bf30f1f188cdd7b6454fd6e74ce6f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54783743"
---
# <a name="sccrename-function"></a>SccRename İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu işlev, kaynak denetimi Sistemi'nde bir dosyayı yeniden adlandırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
SCCRTN SccRename(  
   LPVOID pvContext,  
   HWND   hWnd,  
   LPCSTR lpFileName,  
   LPCSTR lpNewName  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 pvContext  
 [in] Kaynak Denetimi Eklentisi bağlam yapısı.  
  
 hWnd  
 [in] Kaynak Denetimi Eklentisi sağladığı herhangi bir iletişim kutusu için bir üst öğe olarak kullanabileceğiniz IDE penceresi için bir tanıtıcı.  
  
 lpFileName  
 [in] Adlandırılan dosyasının tam dosya adı.  
  
 lpNewName  
 [in] Tam yeni adı. Dizin yolu farklı ise, ardından dosyayı bir alt dizinden başka taşınmıştır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|SCC_OK|Yeniden adlandırma işlemi başarıyla tamamlandı.|  
|SCC_E_PROJNOTOPEN|Proje kaynak denetimi altında açık değil.|  
|SCC_E_FILENOTCONTROLLED|Dosya kaynak denetimi altında değil.|  
|SCC_E_ACCESSFAILURE|Kaynak denetim sistemi, ağ veya çakışma sorunları nedeniyle muhtemelen erişilirken sorun oluştu.|  
|SCC_E_NOTAUTHORIZED|Kullanıcı bu işlemi tamamlamak için yetkili değil.|  
|SCC_E_COULDNOTCREATEPROJECT|Projeyi yeniden adlandırma işleminin bir parçası oluşturulamadı.|  
|SCC_E_OPNOTPERFORMED|İşlem gerçekleştirilmedi.|  
|SCC_E_NONSPECIFICERROR|Belirtilmemiş veya genel bir hata oluştu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu işlev, bir dosyayı yeniden adlandırmak veya taşımak bir konumdan diğerine kaynak denetim sistemi için kullanılabilir. Diskteki dosya erişmek kaynak denetimi eklentisi çalışmamalıdır. Yerel dosyayı yeniden adlandır IDE'nin sorumluluğundadır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)
