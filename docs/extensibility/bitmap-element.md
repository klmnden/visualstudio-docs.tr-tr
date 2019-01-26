---
title: Bitmap öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, Bitmaps
- Bitmaps element (VSCT XML schema)
ms.assetid: edcd7891-f4e7-416d-809d-5e2eed9f17e4
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 687523f54d10a6a43e5db8d46ab391f53caf8c94
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54972241"
---
# <a name="bitmap-element"></a>Bitmap öğesi
Bir bit eşlem tanımlar. Bit eşlemin bir kaynaktan veya bir dosya yüklenir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<Bitmap guid="guidImages" href="images\MyImage.bmp" usedList="bmp1, bmp2, bmp3" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|GUID|Gerekli. GUID/ID komut tanımlayıcısı GUİD'si.<br /><br /> Guid özniteliği bir bit eşlem için herhangi bir VSPackage veya diğer komut grubuyla ilişkili değil.  Bit eşlem tanımına benzersiz olması ve başka bir amaçla kullanılmamalıdır.|  
|resID|Kimliği bir GUID/ID komut tanımlayıcısı. ResID veya href özniteliği gereklidir.<br /><br /> ResID özniteliği birleştirme komut tablosu sırasında yüklenecek olan bit eşlem Şerit belirleyen bir tamsayı kaynak kimliğidir.  Komut tablosu yüklenirken, kaynak kimliği tarafından belirtilen bit eşlemleri aynı modülünü kaynaktan yüklenir.|  
|usedList|ResID özniteliği mevcut ise gereklidir. Kullanılabilir görüntüler, bit eşlem şeridinde seçer.|  
|href|Bit eşlem yolu. ResID veya href özniteliği gereklidir.<br /><br /> Sonuçta elde edilen ikili dosyada gömülü belirtilen görüntü dosyasının yoluna aranır.  Komut tablosu birleştirme sırasında görüntünün kopyalanır ve ek kaynak araması ya da yük gereklidir.  Şerit'ndaki tüm görüntüler usedList öznitelik mevcut değilse kullanılabilir. **Not:**  Görüntüleri dahil çeşitli biçimlerden birinde sağlanabilir *.bmp*, *.png*, ve *.gif*.  Önceki derleyici sürümleri için kısmi saydam alfa bilgilerine sahip 32-bit bit eşlem resimleri desteklememektedir. Geçici çözüm bu sürümleri için kullanmaktır *.png* biçimi.|  
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|  
  
### <a name="child-elements"></a>Alt öğeleri  
 Yok.  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Bitmaps öğesi](../extensibility/bitmaps-element.md)|Bit eşlem öğeleri gruplandırır.|  
  
## <a name="example"></a>Örnek  
  
```  
<Bitmap guid="guidWidgetIcons" href="WidgetToolbarIcons_32.bmp" />  
<Bitmap guid="guidWidgetIcons2" resID="IDBMP_WIDGETICONS"  
  usedList="1, 2, 3, 4"/>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)