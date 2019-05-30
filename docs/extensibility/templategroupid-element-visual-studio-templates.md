---
title: Templategroupıd öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#TemplateGroupID
helpviewer_keywords:
- TemplateGroupID element [Visual Studio Templates]
- <TemplateGroupID> element [Visual Studio Templates]
ms.assetid: bce7b49a-90bc-4691-aff3-a87e209f6d83
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4b4e0ccae38b79cf8efb4b7b426fb65ae909c5d5
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66316600"
---
# <a name="templategroupid-element-visual-studio-templates"></a>TemplateGroupID Öğesi (Visual Studio Şablonları)
Ne tür bir proje öğesi şablonları kategoride görüneceğini belirtir. Bu öğe önemlidir [ShowByDefault (Visual Studio şablonları)](../extensibility/showbydefault-visual-studio-templates.md) ayarlanır `false`. Zaman [ShowByDefault (Visual Studio şablonları)](../extensibility/showbydefault-visual-studio-templates.md) ayarlanır `true`, sonra tüm proje türünde bir öğe şablonu kullanılabilir.

 \<VSTemplate > \<TemplateData > \<Templategroupıd >

## <a name="syntax"></a>Sözdizimi

```
<TemplateGroupID> ... </TemplateGroupID>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler
 Yok.

### <a name="child-elements"></a>Alt Öğeler
 Yok.

### <a name="parent-elements"></a>Üst Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Şablonu kategorilere ayırır ve nasıl görüntülendiğini tanımlar **yeni proje** veya **Yeni Öğe Ekle** iletişim kutusu.|

## <a name="text-value"></a>Metin Değeri
 Bir metin değeri gereklidir.

 Metin, öğe şablonları bir kategori için bir tanımlayıcı belirtir.

## <a name="remarks"></a>Açıklamalar
 `TemplateGroupID` bir öğedir.

 Değerini `TemplateGroupID` öğesi, proje sistemi kaydı ile birlikte kullanılır (hkey_local_machıne\software\microsoft\visualstudio\\ *\<sürüm numarası >* \Projects\\) görünen filtre şablonlarına **Yeni Öğe Ekle** iletişim kutusu.

|Visual C++ değeri|Açıklama|
|------------------------|-------------|
|VC yerel|Yerel projeleri için kullanılır. Ayrıca bir proje türü belirlenemiyorsa varsayılan.|
|VC yönetilen|Kullanılan yönetilen için (/ clr) projeleri|
|VC-Windows|Windows Platformu (yerel/yönetilen/deposu) hedefleyen tüm projeler için kullanılan|
|WinRT yerel UAP|Windows 10 mağazası projeleri için kullanılır|
|CodeSharing yerel|Paylaşılan öğe projeleri için kullanılır|
|WinRT-Native-6.3|Windows 8.1 Store projeler için kullanılan|
|WinRT-Native-Phone-6.3|Windows Phone 8.1 projeleri için kullanılır|
|WinRT yerel|Windows 8.0 Store projeler için kullanılan|
|VC-Android|Android projeleri için kullanılır|

## <a name="see-also"></a>Ayrıca Bkz.
- [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)
- [Proje ve Öğe Şablonları Oluşturma](../ide/creating-project-and-item-templates.md)