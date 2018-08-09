---
title: Elemento VisioDocument ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: O elemento raiz de um documento do Microsoft Visio.
ms.openlocfilehash: 5a325b78ec64708246f0c8a6f5396c2ce1569121
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773279"
---
# <a name="visiodocument-element-visio-xml"></a>Elemento VisioDocument ('Visio XML')

O elemento raiz de um documento do Microsoft Visio.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

Nenhum.
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Cores](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Colors_Type](colors_type-complextypevisio-xml.md) <br/> |Contém a tabela de cores do documento.  <br/> |
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contém os elementos que especificam as configurações do documento.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Especifica a estrutura do **ShapeSheet** de um documento.  <br/> |
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.  <br/> |
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Contém uma coleção de elementos de **FaceName** .  <br/> |
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Contém os elementos de cabeçalho e rodapé de um documento.  <br/> |
|[PublishSettings](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[PublishSettings_Type](publishsettings_type-complextypevisio-xml.md) <br/> |Especifica o conjunto de páginas que estão visíveis e está definida de recordsets são atualizáveis em um desenho de desenho.  <br/> |
|[Folhas de estilo](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Contém uma coleção de elementos de folha de estilos do documento.  <br/> |
   
### <a name="attributes"></a>Atributos

Nenhum.
  

