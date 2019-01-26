---
title: VSPerfReport | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- command-line tools, VSPerfReporttool
- performance tools, VSPerfReport tool
- profiling tools,VSPerfReport
- VSPerfReport tool
- command line, tools
- instrumentation, VSPerfReporttool
ms.assetid: dbfd8d91-4430-4b82-81b9-97ac61412a6c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 56dbbded2f141ab2e4be02c81f4e40fd6f523809
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55020808"
---
# <a name="vsperfreport"></a>VSPerfReport
VSPerfReport komut satırı aracını kullanarak raporları oluşturmak için kullanılan [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma veri dosyaları profil oluşturma araçları. Varsayılan rapor biçimi bir. *csv* dosya.  
  
 VSPerfReport aşağıdaki sözdizimini kullanır:  
  
```cmd  
VSPerfReport [/U] vspfilename [/options]  
```  
  
 Unutmayın `filename` geçerli olmalıdır. *Vsp* veya. *vsps* dosya.  
  
 VSPerfReport komut satırı aracını da karşılaştırmak için kullanılır. *vsp* veya. *vsps* dosyaları. Fark ("fark") rapor oluşturmak için aşağıdaki sözdizimini kullanın:  
  
```cmd  
VSPerfReport [/U] /diff vspfilename1 vspfilename2 [/options]  
```  
  
 `vspfilename1 and vspfilename2` geçerli olmalıdır. *vsp* veya. *vsps* dosyaları.  
  
## <a name="symbol-files"></a>Simge dosyaları  
 İşlev adları ve satır numaraları gibi sembol bilgilerini görüntülemek için VSPerfReport sembol erişim gerektirir (. Profili oluşturulan bileşenleri ve Windows sembol dosyalarını PDB) dosyaları. Daha fazla bilgi için [nasıl yapılır: Komut satırından sembol dosyası konumlarını belirtme](../profiling/how-to-specify-symbol-file-locations-from-the-command-line.md).  
  
## <a name="general-report-options"></a>Genel rapor seçenekleri  
 Aşağıdaki tabloda genel raporun biçimlendirme seçenekleri ve raporlanacak verileri seçme seçeneklerini açıklar.  
  
|Seçenekler|Açıklama|  
|-------------|-----------------|  
|**U**|Rapor çıktısı ve yeniden yönlendirilmiş konsol Çıkışı Unicode olarak yazılır. İlk seçenek belirtilmelidir.|  
|**Özet:**[*türleri*]|Bir veya daha fazla rapor türlerini oluşturur.<br /><br /> -   `All` -Tüm rapor türleri oluşturuldu.<br />-   `CallerCallee` -İşlevler arası üst/alt ilişkilerini.<br />-   `Function` -çağrılan işlevlerin.<br />-   `CallTree` -çağrılan işlevlerin hiyerarşisini.<br />-   `Counter` -tüm işaretleri birlikte Windows performans sayacı değerlerini.<br />-   `Ip` -profili yönergeleri.<br />-   `Life` -(ayırma verilerinin toplandığını olduğunda kullanılabilir.) ayrılmış nesnelerin ömrü<br />-   `Line` Kaynak kod satırı profil verileri.<br />-   `Header` -rapor dosyasının başlık bilgilerini içerir.<br />-   `Mark` tüm işaretleri.<br />-   `Module` -profili modüller.<br />-   `Process` -profili işlemler.<br />-   `Thread` -iş parçacığı profili.<br />-   `Type` -türler ayrılmış.<br />-   `Contention` -Kaynak çakışmaları.<br />-   `RuleWarnings` -Performans kural sorunlarını<br />-   `ETW` -tüm olay izleme için Windows (ETW) olayları, profil oluşturma çalışmasında toplanan. .Etl veri dosyası özgün konumuna veya .vsp veya .vsps dosyasını içeren dizini olmalıdır.|  
|**Xml**|XML formatında çıkış rapor.|  
|**CallTrace**|İşlev girişi ve çıkış yapar ve ETW olayları işaretleri listesini oluşturur.|  
|**ClearPackedSymbols**|Daha önce katıştırılmış sembolleri bir profil oluşturucu veri dosyasından kaldırır. İkinci PackSymbols çalıştırmadan önce şu komutu çalıştırın. zaman.|  
|**SymbolPath:** `path`|Bir veya daha fazla arama yollarını ya da profil oluşturucu veri dosyası için sembolleri içeren sembol sunucuları belirtir.|  
|**DebugSymPath**|Simgeler ve bulunan olup olmadığı için Aranan konumları listeler. Bu seçenek, sembol çözümleme sorunlarını gidermek kullanışlıdır.|  
|**PackSymbols**|Kaydeder simgeleri profil oluşturma veri (.vsp) dosyasına kadar bu sembol (. *pdb*) dosyaları, analiz için gerekli değildir.|  
|**Çıkış:** *yolu*&#124;*dosya adı*|Oluşturulan rapor dosyaları için alternatif bir konum belirtir. Varsayılan olarak, raporlar, geçerli dizinde oluşturulur.|  
|**SummaryFile**|Analiz edin ve analiz edilmiş bilgileri bir .vsps Özet dosyasına kaydet.|  
|**PrintMarks**|Adları ve tüm zaman damgaları içinde belirtilen rapor dosyasını görüntüleyin.|  
|**?**|Kullanım bilgilerini görüntüler.|  
|**NoLogo**|Rapor çalıştırırken sürüm bilgileri gizler.|  
|**UserRulesDirectory**|[Henüz uygulanmadı] directory içeren kullanıcı tanımlı performans kuralları belirtir.|  
  
## <a name="filter-options"></a>Filtre Seçenekleri  
 Aşağıdaki tabloda kullanılabilir verileri filtrelemek için seçenekleri açıklar.  
  
|Seçenekler|Açıklama|  
|-------------|-----------------|  
|**JustMyCode**[**:**[`caller`] [,`callee`]]|Yalnızca kullanıcı uygulama işlev çağrılarını Göster; Sistem çağrıları gizleyin.<br /><br /> -Parametre - tüm sistem işlevlerini gizleyin.<br />-   `caller` -Uygulama işlevlerini çağıran sistem fonksiyonların bir seviyesini göster.<br />-   `callee` -Kullanıcı uygulama işlevleri tarafından çağrılan sistem fonksiyonların bir seviyesini göster.|  
|**StartTime:**[*değer*]|Yalnızca (milisaniye cinsinden.) değerden sonra toplanan verileri göster|  
|**EndTime:**[*değer*]|Yalnızca (milisaniye cinsinden.) değerden önce toplanan verileri göster|  
|**FilterFile:** `VSPFFile`|Visual Studio performans raporu penceresinden oluşturulan bir filtre dosyasının konumunu belirtir.|  
|**MsFilter:**[*starttime, süresi*]|Yalnızca verileri göstermek `starttime` uzunluğuna kadar `duration` (milisaniye cinsinden.)|  
|**İşlem:**[*PID*]|Yalnızca belirtilen işlemden verileri göster.|  
|**İş parçacığı:**[*ThreadID*]|Yalnızca belirtilen iş parçacığından verileri göster.|  
|**İş parçacığı:**[*ThreadID, ProcessId*]|Yalnızca belirtilen işlemle ilişkili belirtilen iş parçacığından verileri göster.|  
  
## <a name="difference-report-options"></a>Fark rapor seçenekleri  
 Aşağıdaki tabloda, rapor dosyalarını karşılaştırma seçeneklerini açıklar.  
  
|Seçenekler|Açıklama|  
|-------------|-----------------|  
|**Fark**  `vspfile1 vspfile2`|İki rapor dosyalarını karşılaştırma (. *Vsp* veya. *vsps*) dosyaları. Özet Seçenekleri fark seçeneğini kullanarak göz ardı edilir.|  
|**Fark:**[*değer*]|Bu eşik değerinin iki değer arasındaki farkı göz ardı edilir. Ayrıca bu eşiğin altında yeni veriler gösterilmeyecek.|  
|**DiffTable:**[*tablename*]|Dosyayı karşılaştırmak için belirli tabloyu kullanın. İşlevler tablosu varsayılandır.|  
|**DiffColumn:**[*columnname*]|Bu özel sütun karşılaştırma değerleri kullanın. Özel örnekler Yüzde sütunu varsayılandır.|  
|**QueryDiffTables**|Geçerli tablolar ve sütunlar için sağlanan iki rapor dosyaları listeler.|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Performans raporu görünümleri](../profiling/performance-report-views.md)