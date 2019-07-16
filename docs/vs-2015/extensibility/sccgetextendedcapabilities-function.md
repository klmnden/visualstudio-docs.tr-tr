---
title: SccGetExtendedCapabilities işlevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- SccGetExtendedCapabilities
helpviewer_keywords:
- SccGetExtendedCapabilities function
ms.assetid: 588c6a92-2147-4d8b-a357-96ca7da0a092
caps.latest.revision: 17
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: f02591eac6a3f69ae5513aa9dc0abed381cd1c8a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68200105"
---
# <a name="sccgetextendedcapabilities-function"></a>SccGetExtendedCapabilities İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu işlev, kaynak denetimi eklentisi tarafından desteklenen ek özellikleri döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
SCCRTN SccGetExtendedCapabilities(  
   LPVOID pContext,  
   LONG lSccExCaps,  
   LPBOOL pbSupported  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 pContext  
 [in] Kaynak Denetimi Eklentisi bağlam işaretçisi.  
  
 lSccExCaps  
 [in] Test etmek istediğiniz genişletilmiş bir özellik belirten bir bayrak (genişletilmiş özelliği kodu tablosuna bakın [özellik bayrakları](../extensibility/capability-flags.md) olası bayrakları için).  
  
 pbSupported  
 [out] Sıfır olmayan döndürür (`TRUE`) belirtilen yeteneği desteklenir; Aksi takdirde, sıfır döndürür (`FALSE`).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|SCC_OK|Alma özelliği işlemi başarıyla tamamlandı.|  
|SCC_E_UNKNOWNERROR<br /><br /> SCC_E_NONSPECIFICERROR|Bilinmeyen veya belirtilmeyen bir hata oluştu.|  
  
## <a name="remarks"></a>Açıklamalar  
 İsteğe bağlı olarak bu yöntem çağrılır; Test edilecek bir yetenek gerektiğinde, diğer bir deyişle, bu yöntem belirlemek için özellik desteklenen çağrılır. Aynı anda yalnızca bir bayrağı belirtilmiş.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)   
 [Hata kodları](../extensibility/error-codes.md)   
 [Özellik Bayrakları](../extensibility/capability-flags.md)
