---
title: VSCT XML Şeması koşullu öznitelikleri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, conditional attributes
- conditional attributes (VSCT XML schema)
ms.assetid: 754d4f32-319b-44c9-915f-f7c60e53222e
caps.latest.revision: 6
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 6294ee8027b61840149096561efc91b8a4a3c3ec
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62422169"
---
# <a name="vsct-xml-schema-conditional-attributes"></a>VSCT XML Şeması Koşullu Öznitelikleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Tüm öğeleri ve listeleri için koşullu öznitelikler uygulanabilir. Mantıksal işleçler ve sembol genişletme ifadeler true veya false olarak değerlendirin. TRUE ise sonuçta elde edilen çıktıda ilişkili liste veya öğe dahildir.  
  
 Belirteç genişletmeleri diğer belirteç genişletmeleri veya sabitler karşı test edilebilir. ' % S'işlevi Defined() değere sahip olsa bile belirli bir adı tanımlı olup olmadığını test etmek için kullanılır.  
  
 Koşul özniteliği bir listesine uygulandığında, koşul listesindeki her alt öğenin uygulanır. Bir alt öğesi bir koşul özniteliğine içeriyorsa, onun koşulu bir AND işlemi tarafından üst ifade ile birleştirilir.  
  
 Değerler 1, '1' ve 'true' true ' değerlendirilir ve 0, '0' ve 'false' false ' değerlendirilir.  
  
## <a name="operators"></a>İşleçler  
 Koşullu ifadeler değerlendirmek için aşağıdaki işleçleri kullanılabilir.  
  
|İşleç|Tanım|  
|--------------|----------------|  
|(,)|Gruplandırma|  
|!|Mantıksal değil|  
|\<, >, \<=, >=, ==, !=|İlişkisel ve eşitlik|  
|and|Boole değeri|  
|veya|Boole değeri|  
  
## <a name="examples"></a>Örnekler  
  
```  
<Menu Condition="Defined(DEBUG)" …  
</Menu>  
  
<Menu Condition="%(SKU_MODE) = 'Demo'" …  
</Menu>  
  
<Menus Condition="Defined(DEBUG)">  
    <Menu …  
    </Menu>  
</Menus>  
  
<Menus Condition="Defined(DEMO_SKU)">  
    <Menus Condition="!Defined(DEBUG)">  
        <Menu …  
        </Menu>  
    </Menus>  
  
    <Menu …  
    </Menu>  
</Menus>  
  
<Menus Condition="(Defined(DEMO_SKU) or Defined(SAMPLE_SKU))   
and !Defined(DEBUG)">  
    <Menu …  
    </Menu>  
</Menus>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
