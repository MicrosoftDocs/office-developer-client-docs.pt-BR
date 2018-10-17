---
title: Elemento Connect (Connects_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399316"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a>Elemento Connect (Connects_Type complexType) ('Visio XML')

Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd:string  <br/> |opcional  <br/> |A célula da qual uma conexão se origina.  <br/> |Valores do tipo xsd:string.  <br/> |
|FromPart  <br/> |xsd:int  <br/> |opcional  <br/> |A parte de uma forma da qual uma conexão se origina.  <br/> |Valores do tipo xsd:int.  <br/> |
|FromSheet  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |A ID da forma a partir da qual uma ou mais conexões se originam.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ToCell  <br/> |xsd:string  <br/> |opcional  <br/> |A célula à qual uma conexão é feita.  <br/> |Valores do tipo xsd:string.  <br/> |
|ToPart  <br/> |xsd:int  <br/> |opcional  <br/> |A parte de uma forma à qual uma conexão é feita.  <br/> |Valores do tipo xsd:Int.  <br/> |
|ToSheet  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |A ID da forma à qual uma ou mais conexões foram feitas.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

