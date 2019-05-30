---
title: Elemento DataConnection (DataConnections_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Resume a comunicação entre um ou mais objetos DataRecordset e uma fonte de dados não XML.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538400"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a>Elemento DataConnection (DataConnections_Type complexType) (XML do Visio)

Resume a comunicação entre um ou mais objetos **DataRecordset** e uma fonte de dados não XML. 
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |connections.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Contém os elementos **DataConnection** para o documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd:boolean  <br/> |opcional  <br/> |O valor padrão é false. Consulte Comentários para obter mais informações.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|Comando  <br/> |xsd:string  <br/> |opcional  <br/> |A cadeia de caracteres de comando usada para consultar a fonte de dados.  <br/> |Valores do tipo xsd:string.  <br/> |
|ConnectionString  <br/> |xsd:string  <br/> |opcional  <br/> |A cadeia de conexão que define os parâmetros necessários para se conectar a uma fonte de dados.  <br/> |Valores do tipo xsd:string.  <br/> |
|FileName  <br/> |xsd:string  <br/> |obrigatório  <br/> |O nome do arquivo de conexão. Consulte Comentários para obter mais informações.  <br/> |Valores do tipo xsd:string.  <br/> |
|FriendlyName  <br/> |xsd:string  <br/> |opcional  <br/> |Um nome fornecido pelo usuário para a conexão de dados.  <br/> |Valores do tipo xsd:string.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |O ID atribuído pelo Visio para uma determinada conexão, exclusivo no documento.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Timeout  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |O tempo de espera em minutos ao tentar estabelecer uma conexão antes de encerrar a tentativa.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

