---
title: Sembol sağlayıcısı arabirimleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- interfaces, symbol handler
- symbol handler, interfaces
- symbol handler, evaluating variables
ms.assetid: 4201f10e-c9f7-4b38-bb45-40fe0082d5bf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 908e597d9ee0a1db4e78de02f3dd4ade1a9aa119
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54945365"
---
# <a name="symbol-provider-interfaces"></a>Sembol Sağlayıcısı Arabirimleri
Sembol işleme arabirimleri için verilmiştir [!INCLUDE[vsipsdk](../../../extensibility/includes/vsipsdk_md.md)].  
  
## <a name="discussion"></a>Tartışma  
 Bu arabirimler, kesme modu sırasında çağrı yığınını değişkenleri değerlendirmek için kullanılır. Bunlar yalnızca ortak dil çalışma zamanı sembol sağlayıcıları için (SP) uygulanır.  
  
|Arabirim|Uygulayan|Açıklama|  
|---------------|--------------------|-----------------|  
|[IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)|SP|Bir öğenin adresi temsil eder.|  
|[IDebugAddress2](../../../extensibility/debugger/reference/idebugaddress2.md)|SP|İşlem kimliğine erişim sağlayan, bir öğenin adresi temsil eder|  
|[IDebugArrayField](../../../extensibility/debugger/reference/idebugarrayfield.md)|SP|Bir dizi simge ya da dizi türü temsil eder.|  
|[IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)|SP|Bir sınıf sembol veya sınıf türü temsil eder.|  
|[IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md)|SP|Yönetilen kod için özel yöntemler ile bir COM + simgesi sağlayıcısını temsil eder.|  
|[IDebugComPlusSymbolProvider2](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2.md)|SP|Yönetilen kod için özel yöntemler ile bir COM + simgesi sağlayıcısını temsil eder ve genişleten **IDebugComPlusSymbolProvider**.|  
|[IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md)|SP|Sembolü veya diğer semboller veya türler için bir kapsayıcı türü temsil eder.|  
|[IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md)|SP|Bir simgeye bağlı özel bir özniteliği temsil eder.|  
|[IDebugCustomAttributeQuery](../../../extensibility/debugger/reference/idebugcustomattributequery.md)|SP|Bir sorgu için bir yöntem veya türü özel öznitelikleri temsil eder.|  
|[IDebugCustomAttributeQuery2](../../../extensibility/debugger/reference/idebugcustomattributequery2.md)|SP|Özel özniteliklere erişim üzerinde bir sembol sağlar.|  
|[IDebugDynamicField](../../../extensibility/debugger/reference/idebugdynamicfield.md)|SP|Çalışma zamanında belirlenebilir herhangi bir türü için temel arabirim.|  
|[IDebugDynamicFieldCOMPlus](../../../extensibility/debugger/reference/idebugdynamicfieldcomplus.md)|SP|Dinamik bir alan için temsil eden bir [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md) nesne.|  
|[IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)|SP|Bir numaralandırma türü temsil eder.|  
|[IDebugExtendedField](../../../extensibility/debugger/reference/idebugextendedfield.md)|SP|Yönetilen kod genel türleri desteklemek için kullanılabilir alan türlerini genişletir.|  
|[IDebugField](../../../extensibility/debugger/reference/idebugfield.md)|SP|Tüm alanlar için temel sınıf; sembolü veya tür açıklamasını temsil eder.|  
|[IDebugGenericFieldDefinition](../../../extensibility/debugger/reference/idebuggenericfielddefinition.md)|SP|Yönetilen kod genel bir tür için bir alan tanımını temsil eder.|  
|[IDebugGenericFieldInstance](../../../extensibility/debugger/reference/idebuggenericfieldinstance.md)|SP|Yönetilen kod genel bir tür için bir alan örneğini temsil eder.|  
|[IDebugGenericParamField](../../../extensibility/debugger/reference/idebuggenericparamfield.md)|SP|Yönetilen kod genel bir tür için bir parametreyi temsil eder.|  
|[IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)|SP|Bir yöntemi temsil eder.|  
|[IDebugModOpt](../../../extensibility/debugger/reference/idebugmodopt.md)|SP|Hata ayıklama isteğe bağlı bir değiştirici temsil eder.|  
|[IDebugPointerField](../../../extensibility/debugger/reference/idebugpointerfield.md)|SP|Bir işaretçiyi temsil eder.|  
|[IDebugPrimitiveTypeField](../../../extensibility/debugger/reference/idebugprimitivetypefield.md)|SP|Bir basit tür sabit listesi değeri temsil eden bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) arabirimi.|  
|[IDebugPropertyField](../../../extensibility/debugger/reference/idebugpropertyfield.md)|SP|Get veya ayarlanmış bir yönetilen kod sınıfının bir özelliği temsil eder.|  
|[IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)|SP|Sembollere ve türlere sağlayan bir sembol sağlayıcısını temsil eder.|  
|[IDebugSymbolProviderDirect](../../../extensibility/debugger/reference/idebugsymbolproviderdirect.md)|SP|Doğrudan erişimli bir sembol sağlayıcısı meta verileri ve çekirdek sembol arabirimleri temsil eder.|  
|[IDebugTypeFieldBuilder](../../../extensibility/debugger/reference/idebugtypefieldbuilder.md)|SP|Türünü temsil eden bir alan oluşturma özelliği temsil eder.|  
|[IDebugTypeFieldBuilder2](../../../extensibility/debugger/reference/idebugtypefieldbuilder2.md)|SP|Genişletir **IDebugTypeFieldBuilder** dizi türleri oluşturabilmek için.|  
|[IEnumDebugAddresses](../../../extensibility/debugger/reference/ienumdebugaddresses.md)|SP|Bir koleksiyonunu temsil eder [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) nesneleri.|  
|[IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md)|SP|Bir koleksiyonunu temsil eder [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md) nesneleri.|  
|[IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)|SP|Bir koleksiyonunu temsil eder [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) nesneleri.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [API Başvurusu](../../../extensibility/debugger/reference/api-reference-visual-studio-debugging.md)