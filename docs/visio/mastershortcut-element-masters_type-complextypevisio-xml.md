---
title: Elemento MasterShortcut (Masters_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Especifica um atalho mestre definido no documento.
ms.openlocfilehash: 03196c6fc1f3424c61bcce406dc050f2d5a73365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341731"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>Elemento MasterShortcut (Masters_Type complexType) (' Visio XML ')

Especifica um atalho mestre definido no documento.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Master #. xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[Ícone](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Especifica um ícone binário codificado de MIME (Multipurpose Internet Mail Extensions) (no formato. ico) para um elemento **Master** ou **MasterShortcut** em um documento.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Especifica se o texto do elemento na janela de estêncil é alinhado à esquerda, à direita ou centralizado.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |O tamanho do ícone do elemento.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |A identificação exclusiva do elemento no seu elemento pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Nome  <br/> |xsd:string  <br/> |opcional  <br/> |O nome do elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |opcional  <br/> |O nome universal do elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Determina se um mestre se comporta como um padrão personalizado.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|Prompt  <br/> |xsd:string  <br/> |opcional  <br/> |A barra de status e o prompt da dica de ferramenta para o elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|ShortcutHelp  <br/> |xsd:string  <br/> |opcional  <br/> |Uma cadeia de caracteres de ajuda para o elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|ShortcutURL  <br/> |xsd:string  <br/> |opcional  <br/> |Uma URL para um elemento **MasterShortcut** .  <br/> |Valores do tipo xsd:string.  <br/> |
   

