---
title: Sunucu Gezgini kullanarak SharePoint bağlantılarına gözatma | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.SharePointExplorer.SharePointConnection
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, browsing SharePoint sites
- SharePoint development in Visual Studio, SharePoint Connections
- SharePoint Connections [SharePoint development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: c9f64e2cebf267e9be1773b37a5827c876961a0d
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56609533"
---
# <a name="browse-sharepoint-connections-by-using-server-explorer"></a>Sunucu Gezgini kullanarak SharePoint bağlantılarına göz atın
  Yerel SharePoint bağlantıları gözatabilirsiniz **Sunucu Gezgini**. Bu tekniği kullanarak, bir SharePoint sitesi bileşenleriyle sisteminizde gidebilirsiniz. SharePoint site bileşenlerini liste tanımları ve içerik türleri gibi görünen adlı bir düğüm **SharePoint bağlantıları** ağaç görünümünde **Sunucu Gezgini**. Görüntülenecek **Sunucu Gezgini**, menü çubuğunda, **görünümü** > **Sunucu Gezgini**. SharePoint site bileşenlerini görüntülenmesinin yanı sıra öğeleri kaldırma, özelliklerini görüntülemek veya kısayol menüsünden komutlarını kullanarak ağaç görünümü yenileyin.

> [!IMPORTANT]
>  Bir SharePoint sitesi göz atmak için SharePoint site koleksiyonu yöneticisi olmalı ve Visual Studio yerel bilgisayarın yönetici olarak çalıştırıyor olmalısınız. Site Aksi takdirde, görünür **Sunucu Gezgini**, ancak kendi düğüm genişletilemiyor. Site koleksiyonu yöneticisi olup olmadığını doğrulamak için bir web tarayıcısında, açık sitesini açın **Site eylemleri** menüsünde seçin **Site izinleri**ve ardından **izinleri: Ekip sitesi** sayfasında **Site koleksiyonu yöneticileri** komutunu **Yönet** Şeritteki grubu. Bir site koleksiyonu yöneticisi olduğunuz adınızı metin kutusunda görüntülenir. Varsa **Site koleksiyonu yöneticileri** komut grubu Yönet Şerit üzerindeki görünmüyorsa, site koleksiyonu için Yönetici değilseniz ve site yöneticisinden uygun izinleri almak.

## <a name="server-explorer-nodes"></a>Sunucu Gezgini düğümü
 Her bir SharePoint sitesi bileşeninin bir düğüm tarafından temsil edilen **Sunucu Gezgini** ağaç görünümü altında **SharePoint bağlantıları**. Örneğin, görüntüleyen bir tartışma türünü temsil eden bir tartışma olarak adlandırılan bir içerik türü varsayılan SharePoint sitelerinde yer **tartışmaları** SharePoint sitesinin sayfası. Tartışma içerik türü, çeşitli alanları içerir. Bu alanları görüntülemek için **Sunucu Gezgini**, genişletme **içerik türü** düğümünü ve ardından **tartışma** düğümü. Altında bu var. gövdesi ve tartışma konu başlığı gibi birkaç alan düğümü

## <a name="node-shortcut-menu-commands"></a>Düğümün kısayol menü komutları
 Her düğüm, düğüme sağ veya bunu seçerek ve ardından erişim bir kısayol menüsünde vardır **Shift**+**F10** anahtarları. Düğüm komutları aşağıdakileri içerebilir:

|Komut adı|Açıklama|
|------------------|-----------------|
|Yenile|Ağaç görünümünde düğümünde görüntülenen son tarihten oluşmuş olabilecek değişiklikleri yansıtacak şekilde güncelleştirir.|
|Sil|Seçili düğüm ağacı görünümden kaldırır. **Not:**  Bu komut yalnızca altında listelenen SharePoint bağlantıları etkin **SharePoint bağlantıları** düğümü.|
|Özellikler|Seçili konumda kullanılabilir özelliklerini görüntüler **özellikleri** penceresi. Tüm salt okunur özelliklerini olduğunu ve her düğüm ile ilişkili özellikler.|
|Bağlantı Ekle|Gözatmak istediğiniz bir SharePoint sitesi belirtmenizi sağlar. Kullanılabilir **SharePoint bağlantıları** düğümü ve alt site düğümleri.|
|Tarayıcıda görüntüle|Seçili listedeki Web tarayıcınızda görüntülenir. Bu komut, bazı listelerinde altında kullanılabilir **listeler** bulunan düğüm **listeler ve kitaplıklardaki**.|

## <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[Nasıl yapılır: SharePoint bağlantıları Ekle Kaldır](../sharepoint/how-to-add-or-remove-sharepoint-connections.md)|Yeni bir SharePoint sitesine eklemek için gereken adımları açıklar **SharePoint bağlantıları** düğümünde **Sunucu Gezgini**.|

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint çözümleri geliştirme](../sharepoint/developing-sharepoint-solutions.md)
