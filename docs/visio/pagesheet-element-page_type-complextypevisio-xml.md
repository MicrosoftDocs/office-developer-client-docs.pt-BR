---
title: Elemento PageSheet (Page_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Especifica as propriedades da página de desenho associado à página de desenho.
ms.openlocfilehash: 8b60795c02717e4b752c09af19fa932f87924d1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395130"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a>Elemento PageSheet (Page_Type complexType) ('Visio XML')

Especifica as propriedades da página de desenho associado à página de desenho.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Pages.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Contém os elementos que definem uma página do documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Especifica a ID da folha de estilos a partir dos quais herdam a formatação de preenchimento. Ela deve ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Especifica a ID da folha de estilos a partir dos quais herdam a formatação de linha. Ela deve ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Especifica a ID da folha de estilos a partir dos quais herdam a formatação de texto. Ela deve ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |XSD: String  <br/> |opcional  <br/> |A ID exclusiva do elemento dentro de seu elemento pai.  <br/> |Valores do tipo xsd: String.  <br/> |
   

