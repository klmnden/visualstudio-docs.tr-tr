---
title: IDebugCustomViewer::DisplayValue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugCustomViewer::DisplayValue
helpviewer_keywords:
- IDebugCustomViewer::DisplayValue
ms.assetid: 7a538248-5ced-450e-97cd-13fabe35fb1c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e711fc91a1d234957a136572cc4f5fddb9a47944
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54991093"
---
# <a name="idebugcustomviewerdisplayvalue"></a>IDebugCustomViewer::DisplayValue
Bu yöntem, belirtilen değeri görüntülemek için çağrılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT DisplayValue(  
   HWND             hwnd,  
   DWORD            dwID,  
   IUnknown *       pHostServices,  
   IDebugProperty3* pDebugProperty);  
);  
```  
  
```csharp  
int DisplayValue(  
   IntPtr          hwnd,   
   uint            dwID,   
   object          pHostServices,   
   IDebugProperty3 pDebugProperty  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `hwnd`  
 [in] Ana penceresi  
  
 `dwID`  
 [in] Birden fazla tür destekleyen özel görüntüleyiciler kimliği.  
  
 `pHostServices`  
 [in] Ayrılmış. Her zaman null.  
  
 `pDebugProperty`  
 [in] Görüntülenecek değerini almak için kullanılan arabirim.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem gerekli penceresi oluştur, değerini görüntülemek, giriş bekle ve, tüm çağırana döndürmeden önce pencereyi görüntüle "modal" olmamasıdır. Başka bir deyişle, yöntem özelliğin değeri, bir pencere yok etme için kullanıcı girişini beklerken için çıktı penceresini oluşturmasını görüntüleme tüm yönlerini işlemesi gerekir.  
  
 Değer değiştirme desteklemek için verilen [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) nesne kullanabileceğiniz [SetValueAsStringWithError](../../../extensibility/debugger/reference/idebugproperty3-setvalueasstringwitherror.md) yöntemi — değeri bir dize olarak ifade edilebilir değilse. Aksi takdirde, özel arabirim oluşturmak gerekli olan — bunu uygulama ifade değerlendiricisi özel `DisplayValue` yöntemi — uygulayan aynı nesne üzerinde `IDebugProperty3` arabirimi. Bu özel arabirim yöntemleri bir rastgele boyut ve karmaşıklıktaki verileri değiştirmek için sağlamanız.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCustomViewer](../../../extensibility/debugger/reference/idebugcustomviewer.md)   
 [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)   
 [SetValueAsStringWithError](../../../extensibility/debugger/reference/idebugproperty3-setvalueasstringwitherror.md)