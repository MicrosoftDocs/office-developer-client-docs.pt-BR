---
title: Elemento MasterShortcut (Masters_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Especifica um atalho de mestre definido no documento.
ms.openlocfilehash: be3e7d207e58d8c249598a7e156356d4f9e61849
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772327"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>Elemento MasterShortcut (Masters_Type complexType) ('Visio XML')

Especifica um atalho de mestre definido no documento.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |. XML de # mestre  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Mestres](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Contém os elementos de **mestre** para o documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Ícone](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Especifica que uma MIME (Multipurpose Internet Mail Extensions) codificada ícone binário (no formato. ico) para um elemento de **mestre** ou **MasterShortcut** em um documento.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> |Especifica se o texto do elemento na janela de estêncil é alinhado à esquerda, direita, ou center.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|IconSize  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> |O tamanho do ícone do elemento.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|Id  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |A ID exclusiva do elemento dentro de seu elemento pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Nome  <br/> |XSD: String  <br/> |opcional  <br/> |O nome do elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |opcional  <br/> |O nome universal do elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|PatternFlags  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> |Determina se um mestre se comporta como um padrão personalizado.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|Prompt  <br/> |XSD: String  <br/> |opcional  <br/> |A barra de status e a ferramenta de dica de aviso para o elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|ShortcutHelp  <br/> |XSD: String  <br/> |opcional  <br/> |Uma cadeia de caracteres de ajuda para o elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|ShortcutURL  <br/> |XSD: String  <br/> |opcional  <br/> |Uma URL para um elemento **MasterShortcut** .  <br/> |Valores do tipo xsd: String.  <br/> |
   

