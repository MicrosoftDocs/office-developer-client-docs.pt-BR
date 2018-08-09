---
title: Elemento de DataConnection (DataConnections_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Resume a comunicação entre um ou mais elementos de DataRecordset e uma fonte de dados não-XML.
ms.openlocfilehash: 74e15795e023517263d9b79e9f19557653e4e939
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771666"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a>Elemento de DataConnection (DataConnections_Type complexType) ('Visio XML')

Resume a comunicação entre um ou mais elementos de **DataRecordset** e uma fonte de dados não-XML. 
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Connections.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Conexões de dados](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Contém os elementos de **DataConnection** para o documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |XSD:Boolean  <br/> |opcional  <br/> |O valor padrão é false. Consulte Comentários para obter mais informações.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|Command  <br/> |XSD: String  <br/> |opcional  <br/> |A cadeia de caracteres de comando usada para consultar a fonte de dados.  <br/> |Valores do tipo xsd: String.  <br/> |
|ConnectionString  <br/> |XSD: String  <br/> |opcional  <br/> |A cadeia de caracteres de conexão que define os parâmetros necessários para se conectar a uma fonte de dados.  <br/> |Valores do tipo xsd: String.  <br/> |
|FileName  <br/> |XSD: String  <br/> |obrigatório  <br/> |O nome do arquivo de conexão. Consulte Comentários para obter mais informações.  <br/> |Valores do tipo xsd: String.  <br/> |
|FriendlyName  <br/> |XSD: String  <br/> |opcional  <br/> |Um nome de usuário fornecido para a conexão de dados.  <br/> |Valores do tipo xsd: String.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |O ID atribuído pelo Visio para uma determinada conexão, exclusivo dentro do documento.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Timeout  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |O tempo de espera em minutos durante a tentativa de estabelecer uma conexão antes de abortar a tentativa.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

