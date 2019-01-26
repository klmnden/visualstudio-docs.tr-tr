---
title: ClickOnce yönetilmeyen API Başvurusu | Microsoft Docs
ms.date: 11/04/2016
api_name:
- CleanOnlineAppCache
- GetDeploymentDataFromManifest
- LaunchApplication
api_location:
- dfshim.dll
api_type:
- COM
topic_type:
- apiref
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- LaunchApplication [ClickOnce unmanaged]
- ClickOnce, unmanaged APIs
- CleanOnlineAppCache [ClickOnce unmanaged]
- CleanOnlineAppCacheW interface [ClickOnce unmanaged]
- GetDeploymentDataFromManifest [ClickOnce unmanaged]
ms.assetid: ec002138-4054-456d-bcc1-79ac2f4a4fd7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: ae06a978f1ce75ce174ea610453d8b9b7acc713a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54986676"
---
# <a name="clickonce-unmanaged-api-reference"></a>ClickOnce yönetilmeyen API Başvurusu
[!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] Yönetilmeyen genel API'ler dfshim.DLL'den.  
  
## <a name="cleanonlineappcache"></a>CleanOnlineAppCache  
 Temizler ve çevrimiçi tüm uygulamaları kaldırır [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama önbelleği.  
  
### <a name="return-value"></a>Dönüş değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde hata temsil eden HRESULT döndürür. Yönetilen bir özel durum oluşursa 0x80020009 (DISP_E_EXCEPTION) döndürür.  
  
### <a name="remarks"></a>Açıklamalar  
 CleanOnlineAppCache çağırma başlayacak [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] zaten çalışmıyorsa hizmet.  
  
## <a name="getdeploymentdatafrommanifest"></a>GetDeploymentDataFromManifest  
 Dağıtım bilgileri, bildirim ve etkinleştirme URL'den alır.  
  
### <a name="parameters"></a>Parametreler  
  
|Parametre|Açıklama|Tür|  
|---------------|-----------------|----------|  
|`pcwzActivationUrl`|Bir işaretçi `ActivationURL`.|LPCWSTR|  
|`pcwzPathToDeploymentManifest`|Bir işaretçi `PathToDeploymentManifest`.|LPCWSTR|  
|`pwzApplicationIdentity`|Tam uygulama kimliğini belirten bir NULL ile sonlandırılmış dize almak için arabellek için işaretçi.|LPWSTR|  
|`pdwIdentityBufferLength`|Bir işaretçi uzunluğu bir DWORD `pwzApplicationIdentity` arabelleğinde WCHAR'lar. Bu alanı boş sonlandırma karakter içerir.|LPDWORD|  
|`pwzProcessorArchitecture`|Uygulama dağıtımı, bildirimden işlemci mimarisinden belirten bir NULL ile sonlandırılmış dize almak için arabellek için işaretçi.|LPWSTR|  
|`pdwArchitectureBufferLength`|Bir işaretçi uzunluğu bir DWORD `pwzProcessorArchitecture` arabelleğinde WCHAR'lar.|LPDWORD|  
|`pwzApplicationManifestCodebase`|Uygulama bildiriminin bildirimindeki bir kod temelinde belirten bir NULL ile sonlandırılmış dize almak için arabellek için işaretçi.|LPWSTR|  
|`pdwCodebaseBufferLength`|Bir işaretçi uzunluğu bir DWORD `pwzApplicationManifestCodebase` arabelleğinde WCHAR'lar.|LPDWORD|  
|`pwzDeploymentProvider`|Arabellek için NULL ile sonlandırılmış bir dize almak için bir işaretçi bildirimi dağıtım sağlayıcısından varsa belirtir. Aksi takdirde, boş bir dize döndürülür.|LPWSTR|  
|`pdwProviderBufferLength`|Bir işaretçi uzunluğu bir DWORD `pwzProviderBufferLength`.|LPDWORD|  
  
### <a name="return-value"></a>Dönüş değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde hata temsil eden HRESULT döndürür. Arabellek çok küçük olduğunda HRESULTFROMWIN32(ERROR_INSUFFICIENT_BUFFER) döndürür.  
  
### <a name="remarks"></a>Açıklamalar  
 İşaretçileri null olmamalıdır. `pcwzActivationUrl` ve `pcwzPathToDeploymentManifest` boş olmamalıdır.  
  
 Etkinleştirme URL'sini temizlemek çağrı sahibinin sorumluluğundadır. Örneğin, kaçış ekleme gereken yerlere veya sorgu dizesi kaldırma karakter.  
  
 Giriş uzunluğunu sınırla çağrı sahibinin sorumluluğundadır. Örneğin, URL uzunluğu üst sınırı 2 KB'tır.  
  
## <a name="launchapplication"></a>LaunchApplication  
 Başlatır ve dağıtım URL'yi kullanarak bir uygulamayı yükler.  
  
### <a name="parameters"></a>Parametreler  
  
|Parametre|Açıklama|Tür|  
|---------------|-----------------|----------|  
|`deploymentUrl`|Dağıtım bildirimi URL'sini içeren bir NULL ile sonlandırılmış dizeye bir işaretçi.|LPCWSTR|  
|`data`|Daha sonraki kullanımlar için ayrılmıştır. NULL olmalıdır.|LPVOID|  
|`flags`|Daha sonraki kullanımlar için ayrılmıştır. 0 olmalıdır.|DWORD|  
  
### <a name="return-value"></a>Dönüş değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde hata temsil eden HRESULT döndürür. Yönetilen bir özel durum oluşursa 0x80020009 (DISP_E_EXCEPTION) döndürür.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 <xref:System.Deployment.Application.DeploymentServiceCom.CleanOnlineAppCache%2A>