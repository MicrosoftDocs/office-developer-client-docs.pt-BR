---
title: Conecte-se o elemento (Connects_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: "\n			Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.\n"
ms.openlocfilehash: 1bd3e1f006afe8d5bbb698e0b3a2179b74728315
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771582"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a>Conecte-se o elemento (Connects_Type complexType) ('Visio XML')


			Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.

  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |página # XML, master. XML de #  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |XSD: String  <br/> |opcional  <br/> |A célula do qual se origina uma conexão.  <br/> |Valores do tipo xsd: String.  <br/> |
|FromPart  <br/> |XSD:int  <br/> |opcional  <br/> |A parte de uma forma a partir do qual se origina uma conexão.  <br/> |Valores do tipo xsd:int.  <br/> |
|FromSheet  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |A identificação da forma da qual uma conexão ou conexões se originam.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ToCell  <br/> |XSD: String  <br/> |opcional  <br/> |A célula à qual uma conexão é feita.  <br/> |Valores do tipo xsd: String.  <br/> |
|ToPart  <br/> |XSD:int  <br/> |opcional  <br/> |A parte de uma forma ao qual uma conexão é feita.  <br/> |Valores do tipo xsd:Int.  <br/> |
|ToSheet  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |A identificação da forma à qual uma ou mais conexões são feitas.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

