---
title: Elemento RefreshConflict (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indica uma linha no conjunto de registros de dados vinculada a uma forma que está em conflito após a atualização dos registros de dados.
ms.openlocfilehash: 2da6f98cf7b047564331aaf5a4167e392927a155
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397398"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a>Elemento RefreshConflict (DataRecordSet_Type complexType) ('Visio XML')

Indica uma linha no conjunto de registros de dados vinculada a uma forma que está em conflito após a atualização dos registros de dados.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Recordsets.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Armazena, formata, atualiza e expõe os dados consultados de um banco de dados no Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |ID da página da forma envolvida no conflito.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|RowID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |A identificação da linha original da linha agora está em conflito após a atualização dos dados era.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Identificação da forma  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Identificação da forma envolvida no conflito da forma.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

