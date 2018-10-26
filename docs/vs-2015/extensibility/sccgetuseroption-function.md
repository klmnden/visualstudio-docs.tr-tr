---
title: SccGetUserOption işlevi | Microsoft Docs
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
- SccGetUserOption
helpviewer_keywords:
- SccGetUserOption function
ms.assetid: 17863747-1901-4c53-a2b3-ed996085e120
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 40832984886aeb96e0a58279ef1c91c352b7c1c9
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49853824"
---
# <a name="sccgetuseroption-function"></a>SccGetUserOption İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu işlev, çeşitli kullanıcıya özgü seçenekleri alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
SCCRTN SccGetUserOption(  
   LPVOID pContext,  
   LONG nOption,  
   LPLONG lpVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 pContext  
 [in] Kaynak Denetimi Eklentisi bağlam işaretçisi.  
  
 nOption  
 [in] (Olası seçenekleri için bkz. Notlar) almak için seçenek.  
  
 lpVal  
 [out] Seçeneği ile ilişkili değer.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|SCC_OK|Seçenek başarıyla alındı.|  
|SCC_E_OPNOTSUPPORTED|seçeneği desteklenmez.|  
|SCC_E_NONSPECIFICERROR|Belirtilmeyen bir hata oluştu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Aşağıdaki seçenekler, bu komut tarafından desteklenir:  
  
|Kullanıcı seçeneği|Açıklama|  
|-----------------|-----------------|  
|`SCC_USEROPT_CHECKOUT_LOCALVER`|Kullanıcının dosyaları yerel sürümü kullanıma alma isteyip istemediğini belirler. `lpVal` atanan `SCC_USEROPT_COLV_YES` (kullanıcının istediği yerel dosyaları kullanıma almayı) veya `SCC_USEROPT_COLV_NO`.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)   
 [Hata Kodları](../extensibility/error-codes.md)

