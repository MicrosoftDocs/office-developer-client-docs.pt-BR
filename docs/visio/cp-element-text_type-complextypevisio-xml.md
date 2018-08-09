---
title: elemento CP (Text_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Marca o início das propriedades de um caractere ou seja executado formatado de acordo com o elemento Char correspondente. A execução é definida para o final do texto ou até que a próxima marca.
ms.openlocfilehash: 16e5bb94afeb860220c6cb49a9b98e36e45d76cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771630"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a>elemento CP (Text_Type complexType) ('Visio XML')

Marca o início das propriedades de um caractere ou seja executado formatado de acordo com o elemento Char correspondente. A execução é definida para o final do texto ou até que a próxima marca.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[cp_Type](cp_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |página # XML, master. XML de #  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Contém o texto de uma forma.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |O índice do elemento de Char que representa essa propriedade executar.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

