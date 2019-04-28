---
title: Biçim tanımlayıcıları (C++) hata ayıklayıcısı | Microsoft Docs
ms.date: 3/11/2019
ms.topic: conceptual
f1_keywords:
- vs.debug
dev_langs:
- C++
helpviewer_keywords:
- QuickWatch dialog box, format specifiers in C++
- variables [debugger], watch variable symbols
- symbols, watch variable formatting
- QuickWatch dialog box, using format specifiers
- expressions [C++], format specifiers
- specifiers, watch variable format
- specifiers
- Watch window, format specifiers in C++
- watch variable symbols
- format specifiers, debugger
- debugger, format specifiers recognized by
ms.assetid: 0f6f3b7c-ce2c-4b4d-b14f-7589dbed5444
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 8e6be79bc38e9283493bf5b7428a21c17cf9d3e0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62896626"
---
# <a name="format-specifiers-for-c-in-the-visual-studio-debugger"></a>Visual Studio hata ayıklayıcısı C++ için biçim belirticileri
İçinde bir değer görüntülenir biçimini değiştirebilirsiniz **Watch**, **Otolar**, ve **Yereller** biçim belirticilerini kullanarak windows.

İçindeki Biçim belirticileri kullanabilirsiniz **hemen** penceresinde **komut** penceresi içinde [izleme noktaları](../debugger/using-breakpoints.md#BKMK_Print_to_the_Output_window_with_tracepoints)ve hatta kaynak pencerelerinde. Bu pencereler içinde bir ifade üzerinde duraklarsanız, sonuç görünür bir [DataTip](../debugger/view-data-values-in-data-tips-in-the-code-editor.md). DataTip görünen biçim belirticisini yansıtır.

> [!NOTE]
> Visual Studio yerel hata ayıklayıcı için yeni bir hata ayıklama motoru değiştiğinde, bazı yeni biçimli belirteçler eklendi eklenen ve bazı eskileri kaldırıldı. (Karışık özgün ve yönetilen) birlikte çalışabilirliği bunu yaptığınızda eski hata ayıklayıcı hala kullanılmaktadır, hata ayıklama C++/CLI.

## <a name="set-format-specifiers"></a>Biçim belirticileri kümesi
Aşağıdaki kod örneği kullanacağız:

```C++
int main() {
    int my_var1 = 0x0065;
    int my_var2 = 0x0066;
    int my_var3 = 0x0067;
}
```

Ekleme `my_var1` değişkenini **Watch** hata ayıklarken, pencere **hata ayıklama** > **Windows** > **izleyin**  >  **1 izleyin**. Ardından, değişkeni sağ tıklatın ve seçin **onaltılık gösterim**. Artık **Watch** penceresi 0x0065 değeri gösterir. Bu değer bir tamsayı yerine bir karakter olarak ifade edilen görmek için önce sağ tıklayın ve seçimini **onaltılık gösterim**. Ardından karakterin Biçim belirleyicisi ekleyin **c** içinde **adı** değişken adından sonra sütun. **Değer** sütun gösterdiğini **101 'e'**.

![WatchFormatCPlus1](../debugger/media/watchformatcplus1.png "WatchFormatCPlus1")

::: moniker range=">= vs-2019" 
Görüntüleyebilir ve değeri bir virgül (,) ekleyerek kullanılabilir biçim belirleyicilerinin bir listeden seçim **Watch** penceresi. 

![WatchFormatSpecDropdown](../debugger/media/vs-2019/format-specs-cpp.png "FormatSpecCpp")

::: moniker-end

## <a name="BKMK_Visual_Studio_2012_format_specifiers"></a> Biçim belirticileri
Aşağıdaki tablolarda, Visual Studio'da kullanabileceğiniz biçim belirteçlerini açıklar. Yeni hata ayıklayıcının ve birlikte çalışma C + ile hata ayıklama için değil, kalın belirleyicilerde desteklenen yalnızca +/ CLI.

::: moniker range=">= vs-2019" 

|Belirleyici|Biçimi|Özgün izleme değeri|Görüntülenen değer|
|---------------|------------|--------------------------|---------------------|
|d|Ondalık tamsayı|0x00000066|102|
|o|imzalanmamış sekizlik tamsayı|0x00000066|000000000146|
|x<br /><br /> **h**|Onaltılık tamsayı|102|0xcccccccc|
|X<br /><br /> **H**|Onaltılık tamsayı|102|0xCCCCCCCC|
|xb<br /><br /> **HB**|(baştaki 0 x) olmadan onaltılık tamsayı|102|cccccccc|
|Xb<br /><br /> **HB**|(baştaki 0 x) olmadan onaltılık tamsayı|102|CCCCCCCC|
|b|ikili işaretsiz tamsayı|25|0b00000000000000000000000000011001|
|bb|(olmadan, önde gelen 0b) ikili işaretsiz tamsayı|25|00000000000000000000000000011001|
|e|bilimsel gösterim|25000000|2.500000e + 07|
|G|Bilimsel veya kayan nokta, kısa|25000000|2.5e + 07|
|c|tek karakter|0x0065, c|101 'e'|
|s|const char * (tırnak işaretleriyle) dize|\<konumu > "hello world"|"hello world"|
|**sb**|const char * dizesini (tırnak işareti)|\<konumu > "hello world"|Merhaba Dünya|
|s8|UTF-8 dizesi|\<konumu > "Bu bir UTF-8 kahve cup â˜•"|"Bu bir UTF-8 kahve cup ☕"|
|**s8b**|UTF-8 dizesi (tırnak işareti)|\<konumu > "hello world"|Merhaba Dünya|
|Su|Unicode (UTF-16 kodlaması) dizesi (tırnak işaretleriyle)|\<Konum > L "Merhaba Dünya"|L "Merhaba Dünya"<br /><br /> "hello world" u|
|alt|Unicode (UTF-16 kodlaması) dizesi (tırnak işareti)|\<Konum > L "Merhaba Dünya"|Merhaba Dünya|
|bstr|BSTR ikili dosya dizesine (tırnak işaretleriyle)|\<Konum > L "Merhaba Dünya"|L "Merhaba Dünya"|
|env|Ortam bloğuna (çift null sonlandırılan dize)|\<Konum > L "=:: =::\\\\"|L "=:: =::\\\\\\0 = C: C =:\\\\windows\\\\system32\\0ALLUSERSPROFILE =...|
|**s32**|UTF-32 dizesiyle (tırnak işareti)|\<konumu > "hello world" U|U"hello world"|
|**s32b**|UTF-32 dize (tırnak işareti)|\<konumu > "hello world" U|Merhaba Dünya|
|**tr**|enum|Saturday(6)|Cumartesi|
|**hv**|İşaretçi türü - Denetlenmekte olan işaretçi değeri bir dizi yığın ayırma sonucunu örneğin olduğunu gösterir `new int[3]`.|\<Konum > {\<ilk üye >}|\<Konum > {\<ilk üye >, \<ikinci üye >,...}|
|**na**|Bir işaretçinin bir nesne için bellek adresi bastırır.|\<Konum >, {üye = değer...}|{üye = değer...}|
|**ND**|Türetilmiş sınıfları yok yalnızca temel sınıf bilgilerini görüntüler|`(Shape*) square` temel sınıf içerir ve türetilen sınıf bilgileri|Görüntüler, yalnızca sınıf bilgileri temel|
|İK|HRESULT veya Win32 hata kodu. Hata ayıklayıcının bunları otomatik olarak kodunu çözer gibi bu belirtici artık HRESULT'ları için gereklidir.|S_OK|S_OK|
|WC|Pencere sınıfı bayrağı|0x0010|WC_DEFAULTCHAR|
|WM|Windows ileti numaraları|16|WM_CLOSE KOMUTU|
|n|"Ham görünümü" öğesi Gizle|
|nvo|Yalnızca sayısal değerler için "Ham görünümünün" öğesini göster|
|!|herhangi bir veri türü görünümü özelleştirmelerini yok sayan, ham biçim|\<gösterim özelleştirilmiş >|4|

::: moniker-end

::: moniker range="vs-2017" 

|Belirleyici|Biçimi|Özgün izleme değeri|Görüntülenen değer|
|---------------|------------|--------------------------|---------------------|
|d|Ondalık tamsayı|0x00000066|102|
|o|imzalanmamış sekizlik tamsayı|0x00000066|000000000146|
|x<br /><br /> **h**|Onaltılık tamsayı|102|0xcccccccc|
|X<br /><br /> **H**|Onaltılık tamsayı|102|0xCCCCCCCC|
|c|tek karakter|0x0065, c|101 'e'|
|s|const char * (tırnak işaretleriyle) dize|\<konumu > "hello world"|"hello world"|
|**sb**|const char * dizesini (tırnak işareti)|\<konumu > "hello world"|Merhaba Dünya|
|s8|UTF-8 dizesi|\<konumu > "Bu bir UTF-8 kahve cup â˜•"|"Bu bir UTF-8 kahve cup ☕"|
|**s8b**|UTF-8 dizesi (tırnak işareti)|\<konumu > "hello world"|Merhaba Dünya|
|Su|Unicode (UTF-16 kodlaması) dizesi (tırnak işaretleriyle)|\<Konum > L "Merhaba Dünya"|L "Merhaba Dünya"<br /><br /> "hello world" u|
|alt|Unicode (UTF-16 kodlaması) dizesi (tırnak işareti)|\<Konum > L "Merhaba Dünya"|Merhaba Dünya|
|bstr|BSTR ikili dosya dizesine (tırnak işaretleriyle)|\<Konum > L "Merhaba Dünya"|L "Merhaba Dünya"|
|env|Ortam bloğuna (çift null sonlandırılan dize)|\<Konum > L "=:: =::\\\\"|L "=:: =::\\\\\\0 = C: C =:\\\\windows\\\\system32\\0ALLUSERSPROFILE =...|
|**s32**|UTF-32 dizesiyle (tırnak işareti)|\<konumu > "hello world" U|U"hello world"|
|**s32b**|UTF-32 dize (tırnak işareti)|\<konumu > "hello world" U|Merhaba Dünya|
|**tr**|enum|Saturday(6)|Cumartesi|
|**hv**|İşaretçi türü - Denetlenmekte olan işaretçi değeri bir dizi yığın ayırma sonucunu örneğin olduğunu gösterir `new int[3]`.|\<Konum > {\<ilk üye >}|\<Konum > {\<ilk üye >, \<ikinci üye >,...}|
|**na**|Bir işaretçinin bir nesne için bellek adresi bastırır.|\<Konum >, {üye = değer...}|{üye = değer...}|
|**ND**|Türetilmiş sınıfları yok yalnızca temel sınıf bilgilerini görüntüler|`(Shape*) square` temel sınıf içerir ve türetilen sınıf bilgileri|Görüntüler, yalnızca sınıf bilgileri temel|
|İK|HRESULT veya Win32 hata kodu. Hata ayıklayıcının bunları otomatik olarak kodunu çözer gibi bu belirtici artık HRESULT'ları için gereklidir.|S_OK|S_OK|
|WC|Pencere sınıfı bayrağı|0x0010|WC_DEFAULTCHAR|
|WM|Windows ileti numaraları|16|WM_CLOSE KOMUTU|
|!|herhangi bir veri türü görünümü özelleştirmelerini yok sayan, ham biçim|\<gösterim özelleştirilmiş >|4|

::: moniker-end

> [!NOTE]
> Zaman **hv** Biçim belirleyicisi varsa, hata ayıklayıcı arabellek uzunluğunu belirlemek ve söz konusu öğelerin sayısını görüntülemek çalışır. Her zaman bir dizinin tam arabellek boyutunu bulmak hata ayıklayıcının mümkün olmadığı için belirleyici Boyutlandır kullanması gereken `(pBuffer,[bufferSize])` mümkün olduğunda. **Hv** biçim belirticisi, arabellek boyutu kullanılabilir olmadığı durumlarda kullanışlıdır.

### <a name="BKMK_Size_specifiers_for_pointers_as_arrays_in_Visual_Studio_2012"></a> Diziler olarak işaretçiler için tanımlayıcılar boyutlandırın
Bir dizi olarak görüntülemek istediğiniz bir nesne işaretçiniz varsa, dizi öğelerinin sayısını belirtmek için bir tamsayı ya da bir ifade kullanabilirsiniz.

|Belirleyici|Biçimi|Özgün izleme değeri|Görüntülenen değer|
|---------------|------------|---------------------------|---------------------|
|n|Ondalık veya **onaltılık** tamsayı|pBuffer, [32]<br /><br /> pBuffer,**[0x20]**|Görüntüler `pBuffer` 32 öğe dizisi olarak.|
|**[exp]**|Bir tamsayı olarak değerlendirir. geçerli bir C++ ifadesi.|pBuffer, [bufferSize]|Bir dizisi olarak pBuffer görüntüler `bufferSize` öğeleri.|
|**expand(n)**|Geçerli bir tamsayı olarak değerlendirir bir C++ ifadesi|pBuffer, expand(2)|Üçüncü öğesine görüntüler  `pBuffer`|

## <a name="BKMK_Format_specifiers_for_interop_debugging_and_C___edit_and_continue"></a> Biçim belirleyiciler birlikte çalışma C + ile hata ayıklama için +/ CLI
Belirleyicilerde **kalın** yalnızca yerel ve C + hata ayıklama için destekleniyor +/ CLI kodu.

|Belirleyici|Biçimi|Özgün izleme değeri|Görüntülenen değer|
|---------------|------------|--------------------------|---------------------|
|**d**<br /><br />**i**|imzalanmış ondalık tamsayı|0xF000F065|-268373915|
|**u**|imzalanmamış ondalık tamsayı|0x0065|101|
|o|imzalanmamış sekizlik tamsayı|0xF065|0170145|
|x<br /><br />X|Onaltılık tamsayı|61541|0x0000f065|
|**m**<br /><br />**h**|uzun veya kısa önek: d, i, u, o, x, X|00406042|0x0c22|
|**f**|imzalanmış kayan nokta|(3./2.), f|1.500000|
|**e**|imzalanmış bilimsel gösterim|(3.0/2.0)|1.500000e+000|
|**g**|imzalanmış kayan nokta veya imzalanmış bilimsel gösterim<br/> hangisi daha kısaysa|(3.0/2.0)|1,5|
|c|tek karakter|\<Konum >|101 'e'|
|s|const char * (tırnak işaretleriyle)|\<Konum >|"hello world"|
|Su|const wchar_t*<br /><br /> const char16_t\* (tırnak işaretleriyle)|\<Konum >|L "Merhaba Dünya"|
|alt|const wchar_t*<br /><br /> const char16_t\*|\<Konum >|Merhaba Dünya|
|s8|const char * (tırnak işaretleriyle)|\<Konum >|"hello world"|
|İK|HRESULT veya Win32 hata kodu.<br/>Hata ayıklayıcının bunları otomatik olarak kodunu çözer gibi bu belirtici artık HRESULT'ları için gereklidir.|S_OK|S_OK|
|WC|Pencere sınıfı bayrağı|0x00000040,|WC_DEFAULTCHAR|
|WM|Windows ileti numaraları|0x0010|WM_CLOSE KOMUTU|
|!|herhangi bir veri türü görünümü özelleştirmelerini yok sayan, ham biçim|\<gösterim özelleştirilmiş >|4|

### <a name="BKMK_Format_specifiers_memory_locations_in_interop_debugging_and_C___edit_and_continue"></a> Biçim belirleyiciler bellek konumları'birlikte çalışma'C + ile hata ayıklama için +/ CLI
Aşağıdaki tablo, bellek konumları için kullanılan biçimlendirme simgeleri açıklar. Herhangi bir değer veya konumu değerlendiren bir ifade ile bellek konumu belirleyici kullanabilirsiniz.

|Sembol|Biçimi|Özgün izleme değeri|Görüntülenen değer|
|------------|------------|--------------------------|---------------------|
|**ma**|64 ASCII karakteri|0x0012ffac|0x0012ffac .4...0...".0W&.......1W&.0.:W..1...."..1.JO&.1.2.."..1...0y....1|
|**m**|ardından 16 ASCII karakter, onaltılık biçimde 16 bayt|0x0012ffac|0x0012ffac B3 34 CB 00 84 30 94 80 FF 22 8A 30 57 26 00 00 .4...0...".0W&..|
|**mb**|ardından 16 ASCII karakter, onaltılık biçimde 16 bayt|0x0012ffac|0x0012ffac B3 34 CB 00 84 30 94 80 FF 22 8A 30 57 26 00 00 .4...0...".0W&..|
|**mw**|8 sözcükler|0x0012ffac|0X0012FFAC 34B3 00CB 3084 8094 22FF 308A 2657 0000|
|**MD**|4 doublewords|0x0012ffac|0x0012ffac 00CB34B3 80943084 308A22FF 00002657|
|**mq**|2 quadwords|0x0012ffac|0x0012ffac 7ffdf00000000000 5f441a790012fdd4|
|**mu**|2-bayt karakter (Unicode)|0x0012ffac|0x0012ffac 8478 77f4 ffff ffff 0000 0000 0000 0000|

### <a name="BKMK_Size_specifier_for_pointers_as_arrays_in_interop_debugging_and_C___edit_and_continue"></a> Birlikte çalışma'C + ile hata ayıklama diziler olarak işaretçiler için belirleyici Boyutlandır +/ CLI
Bir dizi olarak görüntülemek istediğiniz bir nesne işaretçiniz varsa, dizi öğelerinin sayısını belirtmek için bir tamsayı kullanabilirsiniz.

|Belirleyici|Biçimi|İfade|Görüntülenen değer|
|---------------|------------|----------------|---------------------|
|n|Ondalık tamsayı|pBuffer[32]|Görüntüler `pBuffer` 32 öğe dizisi olarak.|