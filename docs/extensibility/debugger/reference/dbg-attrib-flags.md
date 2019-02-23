---
title: DBG_ATTRIB_FLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DBG_ATTRIB_FLAGS
helpviewer_keywords:
- DBGPROP_ATTRIB_FLAGS enumerations
ms.assetid: 2f13e601-dadc-476e-a8ec-01c4515082e7
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 831d1326d88e70ffaba2cc0c242c55d7325be705
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56689336"
---
# <a name="dbgattribflags"></a>DBG_ATTRIB_FLAGS
Çeşitli özniteliklerini açıklayan bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) veya [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) arabirimi. Üyesi [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md) yapısı.

## <a name="syntax"></a>Sözdizimi

```cpp
#define DBG_ATTRIB_NONE                 0x0000000000000000,
#define DBG_ATTRIB_ALL                  0x00000000ffffffff,

// Attributes about the object itself

#define DBG_ATTRIB_OBJ_IS_EXPANDABLE    0x0000000000000001,
#define DBG_ATTRIB_OBJ_HAS_ID           0x0000000000000002,
#define DBG_ATTRIB_OBJ_CAN_HAVE_ID      0x0000000000000004,

// Attributes about the value of the object

#define DBG_ATTRIB_VALUE_READONLY       0x0000000000000010,
#define DBG_ATTRIB_VALUE_ERROR          0x0000000000000020,
#define DBG_ATTRIB_VALUE_SIDE_EFFECT    0x0000000000000040,
#define DBG_ATTRIB_OVERLOADED_CONTAINER 0x0000000000000080,
#define DBG_ATTRIB_VALUE_BOOLEAN        0x0000000000000100,
#define DBG_ATTRIB_VALUE_BOOLEAN_TRUE   0x0000000000000200,
#define DBG_ATTRIB_VALUE_INVALID        0x0000000000000400,
#define DBG_ATTRIB_VALUE_NAT            0x0000000000000800,
#define DBG_ATTRIB_VALUE_AUTOEXPANDED   0x0000000000001000,
#define DBG_ATTRIB_VALUE_TIMEOUT        0x0000000000002000,
#define DBG_ATTRIB_VALUE_RAW_STRING     0x0000000000004000,
#define DBG_ATTRIB_VALUE_CUSTOM_VIEWER  0x0000000000008000,

// Attributes about field access types for the object

#define DBG_ATTRIB_ACCESS_NONE          0x0000000000010000,
#define DBG_ATTRIB_ACCESS_PUBLIC        0x0000000000020000,
#define DBG_ATTRIB_ACCESS_PRIVATE       0x0000000000040000,
#define DBG_ATTRIB_ACCESS_PROTECTED     0x0000000000080000,
#define DBG_ATTRIB_ACCESS_FINAL         0x0000000000100000,
#define DBG_ATTRIB_ACCESS_ALL           0x00000000001f0000,

// Attributes for the storage types of the object

#define DBG_ATTRIB_STORAGE_NONE         0x0000000001000000,
#define DBG_ATTRIB_STORAGE_GLOBAL       0x0000000002000000,
#define DBG_ATTRIB_STORAGE_STATIC       0x0000000004000000,
#define DBG_ATTRIB_STORAGE_REGISTER     0x0000000008000000,
#define DBG_ATTRIB_STORAGE_ALL          0x000000000f000000,

// Attributes for the type modifiers on the object

#define DBG_ATTRIB_TYPE_NONE            0x0000000100000000,
#define DBG_ATTRIB_TYPE_VIRTUAL         0x0000000200000000,
#define DBG_ATTRIB_TYPE_CONSTANT        0x0000000400000000,
#define DBG_ATTRIB_TYPE_SYNCHRONIZED    0x0000000800000000,
#define DBG_ATTRIB_TYPE_VOLATILE        0x0000001000000000,
#define DBG_ATTRIB_TYPE_ALL             0x0000001f00000000,

// Attributes that describe the type of object

#define DBG_ATTRIB_DATA                 0x0000010000000000,
#define DBG_ATTRIB_METHOD               0x0000020000000000,
#define DBG_ATTRIB_PROPERTY             0x0000040000000000,
#define DBG_ATTRIB_CLASS                0x0000080000000000,
#define DBG_ATTRIB_BASECLASS            0x0000100000000000,
#define DBG_ATTRIB_INTERFACE            0x0000200000000000,
#define DBG_ATTRIB_INNERCLASS           0x0000400000000000,
#define DBG_ATTRIB_MOSTDERIVED          0x0000800000000000,
#define DBG_ATTRIB_CHILD_ALL            0x0000ff0000000000,

// Miscellaneous attributes

#define DBG_ATTRIB_MULTI_CUSTOM_VIEWERS 0x0001000000000000

typedef UINT64 DBG_ATTRIB_FLAGS;
```

```csharp
public const int DBG_ATTRIB_NONE                 = 0x0000000000000000,
public const int DBG_ATTRIB_ALL                  = 0x00000000ffffffff,

// Attributes about the object itself

public const int DBG_ATTRIB_OBJ_IS_EXPANDABLE    = 0x0000000000000001,
public const int DBG_ATTRIB_OBJ_HAS_ID           = 0x0000000000000002,
public const int DBG_ATTRIB_OBJ_CAN_HAVE_ID      = 0x0000000000000004,

// Attributes about the value of the object

public const int DBG_ATTRIB_VALUE_READONLY       = 0x0000000000000010,
public const int DBG_ATTRIB_VALUE_ERROR          = 0x0000000000000020,
public const int DBG_ATTRIB_VALUE_SIDE_EFFECT    = 0x0000000000000040,
public const int DBG_ATTRIB_OVERLOADED_CONTAINER = 0x0000000000000080,
public const int DBG_ATTRIB_VALUE_BOOLEAN        = 0x0000000000000100,
public const int DBG_ATTRIB_VALUE_BOOLEAN_TRUE   = 0x0000000000000200,
public const int DBG_ATTRIB_VALUE_INVALID        = 0x0000000000000400,
public const int DBG_ATTRIB_VALUE_NAT            = 0x0000000000000800,
public const int DBG_ATTRIB_VALUE_AUTOEXPANDED   = 0x0000000000001000,
public const int DBG_ATTRIB_VALUE_TIMEOUT        = 0x0000000000002000,
public const int DBG_ATTRIB_VALUE_RAW_STRING     = 0x0000000000004000,
public const int DBG_ATTRIB_VALUE_CUSTOM_VIEWER  = 0x0000000000008000,

// Attributes about field access types for the object

public const int DBG_ATTRIB_ACCESS_NONE          = 0x0000000000010000,
public const int DBG_ATTRIB_ACCESS_PUBLIC        = 0x0000000000020000,
public const int DBG_ATTRIB_ACCESS_PRIVATE       = 0x0000000000040000,
public const int DBG_ATTRIB_ACCESS_PROTECTED     = 0x0000000000080000,
public const int DBG_ATTRIB_ACCESS_FINAL         = 0x0000000000100000,
public const int DBG_ATTRIB_ACCESS_ALL           = 0x00000000001f0000,

// Attributes for the storage types of the object

public const int DBG_ATTRIB_STORAGE_NONE         = 0x0000000001000000,
public const int DBG_ATTRIB_STORAGE_GLOBAL       = 0x0000000002000000,
public const int DBG_ATTRIB_STORAGE_STATIC       = 0x0000000004000000,
public const int DBG_ATTRIB_STORAGE_REGISTER     = 0x0000000008000000,
public const int DBG_ATTRIB_STORAGE_ALL          = 0x000000000f000000,

// Attributes for the type modifiers on the object

public const int DBG_ATTRIB_TYPE_NONE            = 0x0000000100000000,
public const int DBG_ATTRIB_TYPE_VIRTUAL         = 0x0000000200000000,
public const int DBG_ATTRIB_TYPE_CONSTANT        = 0x0000000400000000,
public const int DBG_ATTRIB_TYPE_SYNCHRONIZED    = 0x0000000800000000,
public const int DBG_ATTRIB_TYPE_VOLATILE        = 0x0000001000000000,
public const int DBG_ATTRIB_TYPE_ALL             = 0x0000001f00000000,

// Attributes that describe the type of object

public const int DBG_ATTRIB_DATA                 = 0x0000010000000000,
public const int DBG_ATTRIB_METHOD               = 0x0000020000000000,
public const int DBG_ATTRIB_PROPERTY             = 0x0000040000000000,
public const int DBG_ATTRIB_CLASS                = 0x0000080000000000,
public const int DBG_ATTRIB_BASECLASS            = 0x0000100000000000,
public const int DBG_ATTRIB_INTERFACE            = 0x0000200000000000,
public const int DBG_ATTRIB_INNERCLASS           = 0x0000400000000000,
public const int DBG_ATTRIB_MOSTDERIVED          = 0x0000800000000000,
public const int DBG_ATTRIB_CHILD_ALL            = 0x0000ff0000000000,

// Miscellaneous attributes

public const int DBG_ATTRIB_MULTI_CUSTOM_VIEWERS = 0x0001000000000000
```

## <a name="members"></a>Üyeler
 DBG_ATTRIB_NONE öznitelikleri gösterir.

 DBG_ATTRIB_ALL tüm öznitelikleri gösterir.

 DBG_ATTRIB_OBJ_IS_EXPANDABLE başvuru veya özelliğin alt olduğunu gösterir.

 Bu nesne için bir kimlik oluşturuldu DBG_ATTRIB_OBJ_HAS_ID gösterir.

 Bu nesne için bir kimlik oluşturulabilir DBG_ATTRIB_OBJ_CAN_HAVE_ID gösterir.

 DBG_ATTRIB_VALUE_READONLY değerin salt okunur olduğunu gösterir.

 DBG_ATTRIB_VALUE_ERROR değeri bir hata olduğunu gösterir.

 Değerlendirme bir yan etkisi olan DBG_ATTRIB_VALUE_SIDE_EFFECT gösterir.

 DBG_ATTRIB_OVERLOADED_CONTAINER, bu özellik gerçekten aşırı kapsayıcısı olduğunu gösterir.

 DBG_ATTRIB_VALUE_BOOLEAN gösteren değer `DEBUG_PROPERTY_INFO::bstrValue` Boolean.

 DBG_ATTRIB_VALUE_BOOLEAN_TRUE gösteren değer `DEBUG_PROPERTY_INFO::bstrValue` Boolean ve `TRUE`.

 DBG_ATTRIB_VALUE_INVALID gösteren değer `DEBUG_PROPERTY_INFO::bstrValue` geçerli değil.

 DBG_ATTRIB_VALUE_NAT gösteren değer `DEBUG_PROPERTY_INFO::bstrValue` olan "*bir şey*" (NAT). NAT, ertelenmiş kurgusal özel durumları belirten bir kayıt bayrağı Intel 64-bit işlemciler açıklar.

 DBG_ATTRIB_VALUE_AUTOEXPANDED gösteren değer `DEBUG_PROPERTY_INFO::bstrValue` muhtemelen otomatik genişletilmiş olmuştur.

 DBG_ATTRIB_VALUE_TIMEOUT değerlendirme zaman aşımına uğradı gösterir.

 DBG_ATTRIB_VALUE_RAW_STRING gösteren değer `DEBUG_PROPERTY_INFO::bstrValue` işlenmemiş bir dize temsil edilir.

 Bu özellik en az bir özel Görüntüleyici ile ilişkili olan DBG_ATTRIB_VALUE_CUSTOM_VIEWER gösterir.

 DBG_ATTRIB_ACCESS_NONE ne sahip bir nesne belirtir `public`, `private`, ne de `protected` erişim yazın.

 DBG_ATTRIB_ACCESS_PUBLIC erişimine sahip bir nesne belirtir.

 DBG_ATTRIB_ACCESS_PRIVATE özel erişimi olan bir nesne belirtir.

 DBG_ATTRIB_ACCESS_PROTECTED Korumalı Erişim bir nesne belirtir.

 DBG_ATTRIB_ACCESS_FINAL son erişimi olan bir nesne belirtir.

 Erişim ayıklanacak DBG_ATTRIB_ACCESS_ALL maskesi öznitelikleri gelen `DBG_ATTRIB_FLAGS`.

 DBG_ATTRIB_STORAGE_NONE belirtilen depolama tür olduğunu gösterir.

 Genel depolama DBG_ATTRIB_STORAGE_GLOBAL gösterir.

 Statik depolama DBG_ATTRIB_STORAGE_STATIC gösterir.

 Kayıt defterinde depolama DBG_ATTRIB_STORAGE_REGISTER gösterir.

 Depolama ayıklanacak DBG_ATTRIB_STORAGE_ALL maskesi öznitelikleri gelen `DBG_ATTRIB_FLAGS`.

 DBG_ATTRIB_TYPE_NONE, herhangi bir tür değiştiricisi olduğunu gösterir.

 DBG_ATTRIB_TYPE_VIRTUAL nesne türü sanal olduğunu gösterir.

 DBG_ATTRIB_TYPE_CONSTANT nesne türü sabit olduğunu gösterir.

 Nesne türü eşitlenir DBG_ATTRIB_TYPE_SYNCHRONIZED gösterir.

 DBG_ATTRIB_TYPE_VOLATILE nesne türü geçici olduğunu gösterir.

 DBG_ATTRIB_TYPE_ALL türü ayıklamak için maske öznitelikleri gelen `DBG_ATTRIB_FLAGS`.

 DBG_ATTRIB_DATA, bu nesne bir veri alanı olduğunu gösterir.

 DBG_ATTRIB_METHOD, bu nesne bir yöntem olduğunu gösterir.

 DBG_ATTRIB_PROPERTY, bu nesnenin bir özellik olduğunu gösterir.

 DBG_ATTRIB_CLASS, bu nesne bir sınıf olduğunu gösterir.

 DBG_ATTRIB_BASECLASS, bu nesne bir temel sınıf olduğunu gösterir.

 DBG_ATTRIB_INTERFACE, bu nesne bir arabirim olduğunu gösterir.

 DBG_ATTRIB_INNERCLASS, bu nesne bir iç sınıf olduğunu gösterir.

 Bu nesne DBG_ATTRIB_MOSTDERIVED belirten '*en çok türetilen*'. Terim "*en çok türetilen*" gerçek nesnenin türünü ve kendi başvuru türünde değil anlamına gelir.

 DBG_ATTRIB_CHILD_ALL gösterir maskesi `DBG_ATTRIB_DATA` aracılığıyla `DBG_ATTRIB_MOSTDERIVED`.

 DBG_ATTRIB_MULTI_CUSTOM_VIEWERS kendisiyle ilişkilendirilmiş birden çok özel görüntüleyiciler nesneyi içeren gösterir.

## <a name="remarks"></a>Açıklamalar

> [!NOTE]
>  Bu numaralandırma değerleri için C# derlemesinde gerçekten tanımlanmamış. Bunun yerine, kaynak dosyanız için tanımları kopyalamanız gerekir.

 Bu bayraklar ayrıca bir nesne, örneğin, alt bağımsız değişkeni olarak geçirildiğinde filtrelemek için kullanılan [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md). Değerleri ile bit düzeyinde birleştirilebilir `OR`.

 `DBG_ATTRIB_VALUE_CUSTOM_VIEWER` Bayrağı için bir gösterimi olan [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] edinme [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) alanından arabirim [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) arabirimi ve çağrı [GetCustomViewerList](../../../extensibility/debugger/reference/idebugproperty3-getcustomviewerlist.md) özel görüntüleyiciler listesi.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)
- [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)
- [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md)
- [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md)