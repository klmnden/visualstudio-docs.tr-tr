---
title: Office programlarındaki ortak görevler
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office development in Visual Studio, getting started
- FAQs (frequently asked questions) [Office development in Visual Studio]
- Office development in Visual Studio, frequently asked questions
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 655cfbf885e9bd629d4417d007d4137db4521b6f
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54874009"
---
# <a name="common-tasks-in-office-programming"></a>Office programlarındaki ortak görevler
  Bu konu, aşağıdaki kategorileri Visual Studio kullanarak Office çözümleri programlama hakkında sık sorulan soruların yanıtlarını bulmanıza yardımcı olmak için tasarlanmıştır.  
  
-   [Kurulum ve genel görevleri](#projects).  
  
-   [Kullanıcı arabirimi özelleştirme görevleri](#ui).  
  
-   [Excel Otomasyon görevlerini](#excel).  
  
-   [Word otomasyon görevleri](#word).  
  
-   [Veri görevleri](#data).  
  
-   [Sunucu tarafı belge yönetim görevlerini](#server).  
  
-   [Güvenlik görevlerini](#security).  
  
-   [Dağıtım görevlerini](#deployment).  
  
##  <a name="projects"></a> Kurulum ve genel görevler  
  
-   [Nasıl yapılır: Visual Studio'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md).  
  
-   [Nasıl yapılır: Office çözümlerini yükseltme](https://msdn.microsoft.com/a269e539-b717-4680-a568-2152b070347e).  
  
-   [Nasıl yapılır: Office birincil birlikte çalışma derlemelerini yükleme](../vsto/how-to-install-office-primary-interop-assemblies.md).  
  
-   [Nasıl yapılır: Birincil birlikte çalışma derlemeleriyle Office uygulamalarını hedefleme](../vsto/how-to-target-office-applications-through-primary-interop-assemblies.md).  
  
-   [Nasıl yapılır: Office projelerinde olay işleyicileri oluşturma](../vsto/how-to-create-event-handlers-in-office-projects.md).  
  
-   [Nasıl yapılır: Kod çalıştırmadan Office çözümlerini açma](../vsto/how-to-open-office-solutions-without-running-code.md).  
  
-   [Nasıl yapılır: Bir Office çözümü için yapılandırma bilgilerini ayarlamanız](../vsto/how-to-set-up-configuration-information-for-an-office-solution.md).  
  
-   [Nasıl yapılır: Şeritte Geliştirici sekmesini gösterme](../vsto/how-to-show-the-developer-tab-on-the-ribbon.md).  
  
-   [Nasıl yapılır: Eklenti kullanıcı arayüzü hatalarını gösterme](../vsto/how-to-show-add-in-user-interface-errors.md).  
  
##  <a name="ui"></a> Kullanıcı arabirimi özelleştirme görevleri  
  
### <a name="controls-on-documents-and-worksheets"></a>Belgeler ve çalışma denetimlerini  
  
-   [Nasıl yapılır: Office belgelerine Windows Forms denetimleri ekleme](../vsto/how-to-add-windows-forms-controls-to-office-documents.md).  
  
-   [Nasıl yapılır: Çalışma sayfalarına NamedRange denetimleri ekleme](../vsto/how-to-add-namedrange-controls-to-worksheets.md).  
  
-   [Nasıl yapılır: Çalışma sayfalarına ListObject denetimleri ekleme](../vsto/how-to-add-listobject-controls-to-worksheets.md).  
  
-   [Nasıl yapılır: Office belgelerine Windows Forms denetimleri ekleme](../vsto/how-to-add-windows-forms-controls-to-office-documents.md).  
  
-   [Nasıl yapılır: İçerik ekleme denetimleri Word belgeleriyle](../vsto/how-to-add-content-controls-to-word-documents.md).  
  
-   [Nasıl yapılır: Word belgelerine yer işareti denetimi ekleme](../vsto/how-to-add-bookmark-controls-to-word-documents.md).  
  
### <a name="task-panes-in-document-level-customizations"></a>Belge düzeyi özelleştirmelerdeki görev bölmeleri  
  
-   [Nasıl yapılır: Eylemler bölmesi ekleme Word belgelerine veya Excel çalışma kitapları](../vsto/how-to-add-an-actions-pane-to-word-documents-or-excel-workbooks.md).  
  
### <a name="task-panes-in-vsto-add-ins"></a>VSTO eklentileri görev bölmeleri  
  
-   [Nasıl yapılır: Uygulamaya özel görev bölmesi ekleme](../vsto/how-to-add-a-custom-task-pane-to-an-application.md).  
  
### <a name="ribbon-customizations"></a>Şerit özelleştirmeleri  
  
-   [Nasıl yapılır: Şerit özelleştirmeye başlama](../vsto/how-to-get-started-customizing-the-ribbon.md).  
  
-   [Nasıl yapılır: Şeritteki sekmenin konumunu değiştirme](../vsto/how-to-change-the-position-of-a-tab-on-the-ribbon.md).  
  
-   [Nasıl yapılır: Yerleşik bir sekmeyi özelleştirme](../vsto/how-to-customize-a-built-in-tab.md).  
  
-   [Nasıl yapılır: Backstage görünümüne denetimler ekleme](../vsto/how-to-add-controls-to-the-backstage-view.md).  
  
-   [Nasıl yapılır: Bir Şerit Şerit Tasarımcısından Şerit XML dışarı](../vsto/how-to-export-a-ribbon-from-the-ribbon-designer-to-ribbon-xml.md).  
  
### <a name="outlook-form-regions"></a>Outlook form bölgeleri  
  
-   [Nasıl yapılır: Bir Outlook eklenti projesine form bölgesi ekleme](../vsto/how-to-add-a-form-region-to-an-outlook-add-in-project.md).  
  
-   [Nasıl yapılır: Outlook'un form bölgesini görüntülemesini engelleme](../vsto/how-to-prevent-outlook-from-displaying-a-form-region.md).  
  
### <a name="custom-menus"></a>Özel menü  
  
-   [Nasıl yapılır: Kısayol menülerine komut ekleme](../vsto/how-to-add-commands-to-shortcut-menus.md).  
  
##  <a name="excel"></a> Excel otomasyon görevleri  
  
-   [Nasıl yapılır: Program aracılığıyla çalışma sayfası hücresinde bir dizeyi görüntüleme](../vsto/how-to-programmatically-display-a-string-in-a-worksheet-cell.md).  
  
-   [Nasıl yapılır: Program aracılığıyla yeni çalışma kitaplarını](../vsto/how-to-programmatically-create-new-workbooks.md).  
  
-   [Nasıl yapılır: Program aracılığıyla çalışma kitaplarını açma](../vsto/how-to-programmatically-open-workbooks.md).  
  
-   [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kaydetme](../vsto/how-to-programmatically-save-workbooks.md).  
  
-   [Nasıl yapılır: Program aracılığıyla çalışma kitaplarını kapatma](../vsto/how-to-programmatically-close-workbooks.md).  
  
-   [Nasıl yapılır: Program aracılığıyla yeni çalışma kitaplarına ekleme](../vsto/how-to-programmatically-add-new-worksheets-to-workbooks.md).  
  
-   [Nasıl yapılır: Çalışma sayfalarını program aracılığıyla gizleme](../vsto/how-to-programmatically-hide-worksheets.md).  
  
-   [Nasıl yapılır: Program aracılığıyla kitaplarındaki taşıma](../vsto/how-to-programmatically-move-worksheets-within-workbooks.md).  
  
-   [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla koruma](../vsto/how-to-programmatically-protect-workbooks.md).  
  
-   [Nasıl yapılır: Koddaki çalışma sayfası aralıklarına program aracılığıyla bakma](../vsto/how-to-programmatically-refer-to-worksheet-ranges-in-code.md).  
  
-   [Nasıl yapılır: Program aracılığıyla çalışma kitaplarındaki aralıklara biçimler uygulama](../vsto/how-to-programmatically-apply-styles-to-ranges-in-workbooks.md).  
  
-   [Nasıl yapılır: Program aracılığıyla seçili hücreler içeren çalışma sayfalarındaki satırlarda biçimlendirmeyi değiştirme](../vsto/how-to-programmatically-change-formatting-in-worksheet-rows-containing-selected-cells.md).  
  
-   [Nasıl yapılır: Metin çalışma sayfası aralıklarında program aracılığıyla arama](../vsto/how-to-programmatically-search-for-text-in-worksheet-ranges.md).  
  
-   [Nasıl yapılır: Çalışma sayfalarını program aracılığıyla yazdırma](../vsto/how-to-programmatically-print-worksheets.md).  
  
-   [Nasıl yapılır: Program aracılığıyla Excel hesapları çalıştırma](../vsto/how-to-programmatically-run-excel-calculations-programmatically.md).  
  
-   [Nasıl yapılır: Çalışma sayfalarında verileri programlamayla sıralama](../vsto/how-to-programmatically-sort-data-in-worksheets.md).  
  
##  <a name="word"></a> Word otomasyon görevleri  
  
-   [Nasıl yapılır: Program aracılığıyla yeni belgeler oluşturma](../vsto/how-to-programmatically-create-new-documents.md).  
  
-   [Nasıl yapılır: Varolan belgeleri program aracılığıyla açma](../vsto/how-to-programmatically-open-existing-documents.md).  
  
-   [Nasıl yapılır: Program aracılığıyla belgeleri kaydetme](../vsto/how-to-programmatically-save-documents.md).  
  
-   [Nasıl yapılır: Program aracılığıyla belgeleri kapatma](../vsto/how-to-programmatically-close-documents.md).  
  
-   [Nasıl yapılır: Word belgelerine program aracılığıyla metin ekleme](../vsto/how-to-programmatically-insert-text-into-word-documents.md).  
  
-   [Nasıl yapılır: Program aracılığıyla tanımlama ve belgelerde aralıkları seçin](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md).  
  
-   [Nasıl yapılır: Word belgelerinde aralıkları'program aracılığıyla sıfırlama](../vsto/how-to-programmatically-reset-ranges-in-word-documents.md).  
  
-   [Nasıl yapılır: Belgelerde, belgelerde metin biçimlendirme](../vsto/how-to-programmatically-format-text-in-documents.md).  
  
-   [Nasıl yapılır: Word belgelerine XMLNode denetimleri ekleme](../vsto/how-to-add-xmlnode-controls-to-word-documents.md).  
  
-   [Nasıl yapılır: Yer işareti metnini program aracılığıyla güncelleştirme](../vsto/how-to-programmatically-update-bookmark-text.md).  
  
-   [Nasıl yapılır: Program aracılığıyla arama ve belgelerdeki metni değiştirme](../vsto/how-to-programmatically-search-for-and-replace-text-in-documents.md).  
  
-   [Nasıl yapılır: Program aracılığıyla belgeleri yazdırma](../vsto/how-to-programmatically-print-documents.md).  
  
-   [Nasıl yapılır: Program aracılığıyla Word tabloları oluşturma](../vsto/how-to-programmatically-create-word-tables.md).  
  
-   [Nasıl yapılır: Word tablolarına program aracılığıyla satır ve sütun ekleme](../vsto/how-to-programmatically-add-rows-and-columns-to-word-tables.md).  
  
-   [Nasıl yapılır: Program aracılığıyla karakter sayma sayısı](../vsto/how-to-programmatically-count-characters-in-documents.md).  
  
##  <a name="data"></a> Veri görevleri  
  
### <a name="data-bound-controls"></a>Verilere bağlı denetimler  
  
-   [Nasıl yapılır: Çalışma sayfalarını veritabanı verileriyle doldurma](../vsto/how-to-populate-worksheets-with-data-from-a-database.md).  
  
-   [Nasıl yapılır: Belgeleri veritabanı verileriyle doldurma](../vsto/how-to-populate-documents-with-data-from-a-database.md).  
  
-   [Nasıl yapılır: Belgeleri hizmet verileriyle doldurma](../vsto/how-to-populate-documents-with-data-from-services.md).  
  
-   [Nasıl yapılır: Belgeleri nesne verileriyle doldurma](../vsto/how-to-populate-documents-with-data-from-objects.md).  
  
-   [Nasıl yapılır: Belgeleri veritabanı verileriyle doldurma](../vsto/how-to-populate-documents-with-data-from-a-database.md).  
  
-   [Nasıl yapılır: Belgeleri hizmet verileriyle doldurma](../vsto/how-to-populate-documents-with-data-from-services.md).  
  
-   [Nasıl yapılır: Bir konak kontrolü verileriyle veri kaynağını güncelleme](../vsto/how-to-update-a-data-source-with-data-from-a-host-control.md).  
  
### <a name="cached-data-in-document-level-solutions"></a>Belge düzeyi çözümlerde önbelleğe alınmış verileri  
  
-   [Nasıl yapılır: Çevrimdışı veya sunucuda kullanmak için verileri önbelleğe](../vsto/how-to-cache-data-for-use-offline-or-on-a-server.md).  
  
-   [Nasıl yapılır: Bir Office belgesi bir veri kaynağını programlamayla önbelleğe alma](../vsto/how-to-programmatically-cache-a-data-source-in-an-office-document.md).  
  
-   [Nasıl yapılır: Bir parola korumalı belgede veriyi önbelleğe alma](../vsto/how-to-cache-data-in-a-password-protected-document.md).  
  
### <a name="custom-xml-data"></a>Özel XML verileri  
  
-   [Nasıl yapılır: Belge düzeyi özelleştirmelerine özel XML bölümleri ekleme](../vsto/how-to-add-custom-xml-parts-to-document-level-customizations.md).  
  
-   [Nasıl yapılır: VSTO eklentileri kullanarak belgelere özel XML bölümleri ekleme](../vsto/how-to-add-custom-xml-parts-to-documents-by-using-vsto-add-ins.md).  
  
##  <a name="server"></a> Sunucu tarafı belge yönetim görevleri  
  
-   [Nasıl yapılır: Belgelerden yönetilen kod uzantılarını kaldırma](../vsto/how-to-remove-managed-code-extensions-from-documents.md).  
  
-   [Nasıl yapılır: Belgelere yönetilen kod uzantıları ekleme](../vsto/how-to-attach-managed-code-extensions-to-documents.md).  
  
##  <a name="security"></a> Güvenlik görevleri  
  
-   [Nasıl yapılır: Office çözümlerini imzalama](../vsto/how-to-sign-office-solutions.md).  
  
##  <a name="deployment"></a> Dağıtım görevleri  
  
-   [Nasıl yapılır: ClickOnce kullanarak Office çözümü yayımlama](https://msdn.microsoft.com/2b6c247e-bc04-4ce4-bb64-c4e79bb3d5b8).  
  
-   [Nasıl yapılır: Belge düzeyinde Office çözümü ClickOnce kullanarak bir SharePoint sunucusuna yayımlama](https://msdn.microsoft.com/2408e809-fb78-42a1-9152-00afa1522e58).  
  
-   [Nasıl yapılır: ClickOnce Office çözüm yükleme](https://msdn.microsoft.com/14702f48-9161-4190-994c-78211fe18065).  
  
-   [Nasıl yapılır: Son kullanıcı bilgisayarlarında Office çözümlerinin çalışması için Önkoşulları Yükleme](https://msdn.microsoft.com/74dd2c52-838f-4abf-b2b4-4d7b0c2a0a98).  
  
-   [Nasıl yapılır: IIS Office çözümlerinin dağıtımı için hazırlama](https://msdn.microsoft.com/f62bce70-81d4-4f8b-86e6-2f2afec5d9b4).  
  
-   [Nasıl yapılır: Güncelleştirme dağıtılan Office çözümleri](https://msdn.microsoft.com/be96db53-b6ea-46ab-b8d9-b76b098b3b13).  
  
-   [Nasıl yapılır: Office çözümünü yükleme yolunu değiştirmek](https://msdn.microsoft.com/d0eaa07b-2d72-4902-899f-2f9fb165b8fd).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Başlama &#40;Visual Studio'da Office geliştirme&#41;](../vsto/getting-started-office-development-in-visual-studio.md)   
 [Office uygulaması ve proje türüne göre kullanılabilen özellikler](../vsto/features-available-by-office-application-and-project-type.md)   
 [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)  
