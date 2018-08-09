---
title: Elemento mestre (Masters_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Contém os elementos que definem um mestre para o documento.
ms.openlocfilehash: 51c5f0ad8bee5000e981fcfd4d15e2e49f2bda3b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772321"
---
# <a name="master-element-masterstype-complextype-visio-xml"></a>Elemento mestre (Masters_Type complexType) ('Visio XML')

Contém os elementos que definem um mestre para o documento.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Masters.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Contém os elementos de **mestre** para o documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Especifica que uma MIME (Multipurpose Internet Mail Extensions) codificada ícone binário (no formato. ico) para um elemento de **mestre** ou **MasterShortcut** em um documento.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contém os elementos que definem a folha da página para um elemento de **página** ou **mestre** .  <br/> |
|Shapes  <br/> |Shapes_Type  <br/> |Contém uma coleção de elementos de **forma** .  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> |Especifica se o texto do mestre na janela de estêncil é alinhado à esquerda, direita, ou center.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|BaseID  <br/> |XSD: String  <br/> |opcional  <br/> |Um GUID (identificador global exclusivo) que identifica o mestre em documentos.  <br/> |Valores do tipo xsd: String.  <br/> |
|Oculto  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Especifica se o mestre está oculto na interface do usuário.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IconSize  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> |O tamanho do ícone do elemento.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Especifica se o ícone é gerado automaticamente a partir do próprio mestre.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |A ID exclusiva do elemento dentro de seu elemento pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|MatchByName  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Determina como o Microsoft Visio decide que se um mestre de documento já esteja presente quando uma instância de um mestre é quedo na página de desenho.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|Nome  <br/> |XSD: String  <br/> |opcional  <br/> |O nome do elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |opcional  <br/> |O nome universal do elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|PatternFlags  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> |Determina se um mestre se comporta como um padrão personalizado.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|Prompt  <br/> |XSD: String  <br/> |opcional  <br/> |A barra de status e a ferramenta de dica de aviso para o elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|UniqueID  <br/> |XSD: String  <br/> |opcional  <br/> |Um GUID que identifica o mestre dentro do documento.  <br/> |Valores do tipo xsd: String.  <br/> |
   

