---
title: Elemento Master (Masters_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Contém elementos que definem um mestre para o documento.
ms.openlocfilehash: f6effa521b7c5ea69d41b6770ee2dbef61af097c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283962"
---
# <a name="master-element-masterstype-complextype-visio-xml"></a>Elemento Master (Masters_Type complexType) (' Visio XML ')

Contém elementos que definem um mestre para o documento.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Masters. xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Contém os elementos **mestres** do documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Especifica um ícone binário codificado de MIME (Multipurpose Internet Mail Extensions) (no formato. ico) para um elemento **Master** ou **MasterShortcut** em um documento.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contém elementos que definem a folha de página de um elemento **Page** ou **Master** .  <br/> |
|Formas  <br/> |Shapes_Type  <br/> |Contém uma coleção de elementos **Shape** .  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Especifica se o texto do mestre na janela de estêncil é alinhado à esquerda, à direita ou centralizado.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|BaseID  <br/> |xsd:string  <br/> |opcional  <br/> |Um GUID (identificador global exclusivo) que identifica o mestre nos documentos.  <br/> |Valores do tipo xsd:string.  <br/> |
|Oculto  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica se o mestre está oculto na interface do usuário.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |O tamanho do ícone do elemento.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica se o ícone é gerado automaticamente a partir do mestre.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |A identificação exclusiva do elemento no seu elemento pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|MatchByName  <br/> |xsd:boolean  <br/> |opcional  <br/> |Determina como o Microsoft Visio decide se um documento mestre já está presente quando uma instância de um mestre é descartada na página de desenho.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|Name  <br/> |xsd:string  <br/> |opcional  <br/> |O nome do elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |opcional  <br/> |O nome universal do elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Determina se um mestre se comporta como um padrão personalizado.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|Prompt  <br/> |xsd:string  <br/> |opcional  <br/> |A barra de status e o prompt da dica de ferramenta para o elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |opcional  <br/> |Um GUID que identifica o mestre no documento.  <br/> |Valores do tipo xsd:string.  <br/> |
   

