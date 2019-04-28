---
title: IScriptNode::CreateChildHandler | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IScriptNode.CreateChildHandler
apilocation:
- scrobj.dll
helpviewer_keywords:
- IScriptNode::CreateChildHandler
ms.assetid: 4ce5eb10-1a3f-43b0-a4b7-599a397ed3a2
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bca8b30021d39638f3755bace2625bb38a44242d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62787150"
---
# <a name="iscriptnodecreatechildhandler"></a>IScriptNode::CreateChildHandler
Bir kod oluşturma ekler alt örnek olarak bir `IScriptNode`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT CreateChildHandler(  
   LPCOLESTR          pszDefaultName,  
   LPCOLESTR          *prgpszNames,  
   ULONG              cpszNames,  
   LPCOLESTR          pszEvent,  
   LPCOLESTR          pszDelimiter,  
   ITypeInfo*         ptiSignature,  
   ULONG              iMethodSignature,  
   ULONG              isn,  
   DWORD              dwCookie,  
   IScriptEntry       **ppse  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pszDefaultName`  
 [in] Kod oluşturma yöntemiyle ilişkilendirmek için varsayılan adı adresi.  
  
 `prgpszNames`  
 ['de size_is (`cpszNames`)] tanımlayıcılar tam nitelikli ad konak üzerindeki bir listesi.  
  
 `cpszNames`  
 [in] Tanımlayıcıları sayısı `prgpszNames` parametresi.  
  
 `pszEvent`  
 [in] Kod oluşturma yöntemiyle ilişkili olay adı tanımlayan arabellek adresi.  
  
 `pszDelimiter`  
 [in] Sonlandırma, betik bloğu sınırlayıcısı adresi. Ayrıştırma için konak betik bloğunun sonu algılamak için bir sınırlayıcı (örneğin, iki tek tırnak), genellikle kullanır.  
  
 Sınırlayıcı altyapısı geliştirme komut dosyası tarafından ön işleme sağlar. Örneğin, altyapı, tek tırnak işareti ayırıcı olarak kullanılacak iki tek tırnak işaretleri ile değiştirebilir. Altyapısı sınırlayıcı nasıl kullanıldığını belirler.  
  
 Betik bloğunun sonu tanımlamak için kullanılan sınırlayıcı NULL olarak ayarlayın.  
  
 `ptiSignature`  
 [in] Bir işlev nesnesi için tür bilgisi.  
  
 `iMethodSignature`  
 [in] İşlevin dizini `ITypeInfo``ptiSignature` parametresi.  
  
 `isn`  
 [in] Üst alt dizini.  
  
 `dwCookie`  
 [in] Giriş konak nesnesiyle ilişkilendirmek için kullanılan bir uygulama tanımlı bir değer.  
  
 `ppse`  
 [out] Bir işaretçiye alan değişkenin adresini `IScriptEntry` alt örneğinin arabirimi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir kod oluşturma yöntemi, bir olay işleyicisi belirtir. Tarafından çağrılır, bu yöntem, bir kod oluşturma yöntemi oluşturur. bir `IScriptNode` Web sayfasını temsil eden nesne. Bu yöntem tarafından diğer arabirimleri çağrılırsa başarılı olmaz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iscriptnode arabirimi](../../winscript/reference/iscriptnode-interface.md)   
 [IScriptEntry Arabirimi](../../winscript/reference/iscriptentry-interface.md)