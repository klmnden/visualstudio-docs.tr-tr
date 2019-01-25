---
title: IManagedAddin::Load
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords: ''
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 267e2ec1b2ec2dbb5b72a100185ce6b68d455c39
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54865899"
---
# <a name="imanagedaddinload"></a>IManagedAddin::Load
  Yönetilen bir VSTO Eklenti yüklendiğinde çağrılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```csharp
HRESULT Load([in] BSTR bstrManifestURL,   
             [in] IDispatch *pdispApplication);  
```  
  
### <a name="parameters"></a>Parametreler  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|*bstrManifestURL*|İçin VSTO eklentisi bildiriminin tam yolu.|  
|*pdispApplication*|VSTO eklentisi yükleniyor ana bilgisayar uygulaması temsil IDispatch yönelik işaretçi.|  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntemi başarıyla tamamlanıp tamamlanmadığını belirten bir HRESULT değer.  
  
## <a name="remarks"></a>Açıklamalar  
 VSTO eklentisi yükünü dengeleyebilmek için kullanılan bilgileri sağlayan bir dosya (genellikle, bir XML dosyası) bildirimidir. Örneğin, bir bildirim VSTO eklenti derlemesi ve giriş noktası sınıfını VSTO Eklenti yüklendiğinde örneklemek için konumu belirtebilirsiniz.  
  
 *BstrManifestURL* parametre değerini içeren `Manifest` altında girdisi **HKEY_CURRENT_USER\Software\Microsoft\Office\\_\<uygulama adı >_ \Addins\\_\<eklenti kimliği >_**  VSTO eklentisi için kayıt defteri anahtarı. Daha fazla bilgi için [Imanagedaddin arabirimi](../vsto/imanagedaddin-interface.md).  
  
 Uygulama [IManagedAddIn::Load](../vsto/imanagedaddin-load.md) VSTO yüklenmekte eklentisi için uygulama etki alanı ve güvenlik ilkesi yapılandırma gibi görevleri gerçekleştirmek için yöntemi.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Imanagedaddin arabirimi](../vsto/imanagedaddin-interface.md)   
 [IManagedAddin::Unload](../vsto/imanagedaddin-unload.md)  
