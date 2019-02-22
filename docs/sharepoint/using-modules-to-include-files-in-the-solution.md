---
title: Çözüme dosyaları dahil etmek için modül kullanma | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, deployment modules
- SharePoint development in Visual Studio, modules
- modules [SharePoint development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 569f1027163d5651d184254b4e6f57a02df2a39a
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56596191"
---
# <a name="use-modules-to-include-files-in-the-solution"></a>Çözüme dosyaları dahil etmek için modül kullanma
  Ne zaman dosyalarını yeni ana sayfalar gibi dosya türlerinin bakılmaksızın SharePoint sunucusuna dağıtmak isteyebilirsiniz zamanlar olabilir. Bunu yapmak için kullanabileceğiniz *modülleri* (ile karıştırılmamalıdır [!INCLUDE[vbprvb](../sharepoint/includes/vbprvb-md.md)] kod modülleri). Modüller, dosyaları bir SharePoint çözümünü kapsayıcılardır. Çözüm dağıtılırken, modül dosyalarında SharePoint sunucusundaki belirtilen klasöre kopyalanır.

## <a name="module-items-and-elements"></a>Modül öğeleri ve öğeleri
 Bir modülü oluşturmak için bir projeye seçim yaparak ekleme **Yeni Öğe Ekle** iletişim kutusu. Ardından, değiştirme, *Elements.xml* dosya sisteminde nerede ve SharePoint sunucusuna kopyalanması gereken dağıtmak istediğiniz dosyaların adını içerecek şekilde.

 İşte bir örnek *Elements.xml* dosya bir modül için:

```xml
<?xml version="1.0" encoding="utf-8"?>
<Elements xmlns="http://schemas.microsoft.com/sharepoint/">
    <Module Name="Module1">
        <File Path="Module1\Sample.txt" Url="Module1/Sample.txt" />
    </Module>
</Elements>

```

 Yeni oluşturulan modüller aşağıdaki varsayılan dosyaları içerir:

|Dosya Adı|Açıklama|
|---------------|-----------------|
|*Elements.XML*|Modül için tanım dosyasını.|
|*Örnek.txt*|Modüldeki bir dosyayı bir örnek olarak hizmet veren bir yer tutucu dosyası.|

 *Elements.xml* dosyası aşağıdaki öğeleri içerir:

|Öğe adı|Açıklama|
|------------------|-----------------|
|Öğeleri|Modülde tanımlanmış tüm öğeleri içerir.|
|Modül|Tek bir öznitelik modülü öğesinin *adı*, modülün adını şu biçimde belirtir `<Module Name="Module1">`.<br /><br /> Modülün adını değiştirirseniz unutmayın (veya kendi *klasör adı* özelliği), modül öğesi adı el ile güncelleştirmeniz gerekir.<br /><br /> Modül öğesinde bir alt dosya veya dosyalar için belirtirseniz [!INCLUDE[sharepointShort](../sharepoint/includes/sharepointshort-md.md)] (WSS) otomatik olarak oluşturur eşleşen bir dizin yapısı için.|
|Dosya|İki parametre dosyası öğesinin *yolu* ve *Url*.<br /><br /> -Path: SharePoint çözüm dosyasının konumunu ve adını. Biçimidir `Path="Module1\Sample.txt"`.<br /><br /> -Url: Dosyanın SharePoint sunucusuna dağıtılacağı konumu. Biçimidir `Url="Module1/Sample.txt"`.<br /><br /> -Type: Bir isteğe bağlı öznitelik iki ayarı vardır: *GhostableInLibrary* ve *Ghostable*. Biçimidir `Type="GhostableInLibrary"`. Belirtme *GhostableInLibrary* dosyası, bir SharePoint belge kitaplığına kitaplığına eklendiğinde, dosyayı eşlik edecek bir liste öğesi birlikte eklenecek anlamına gelir. Belirtme *Ghostable* için SharePoint belge kitaplığı dışında eklenmesi için dosyayı neden olur.|

 Dağıtmak istediğiniz her dosya için ayrı bir gerekli `<File>` öğenin girişte *Elements.xml*.

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Bir modül kullanarak dosyaları içerme](../sharepoint/how-to-include-files-by-using-a-module.md)
- [Nasıl Yapılır: Bir dosya sağlayın](http://go.microsoft.com/fwlink/?LinkID=144271)
- [SharePoint çözümleri geliştirme](../sharepoint/developing-sharepoint-solutions.md)
- [SharePoint için Web bölümleri oluşturma](../sharepoint/creating-web-parts-for-sharepoint.md)
- [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)
