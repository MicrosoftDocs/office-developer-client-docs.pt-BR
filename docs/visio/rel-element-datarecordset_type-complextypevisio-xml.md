---
title: Elemento Rel (DataRecordSet_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: Especifica uma relação com uma parte com o recordset associado e as informações de vinculação de dados.
ms.openlocfilehash: fa93a3cbc32b6929b159b958ef2a96eafacf204f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542860"
---
# <a name="rel-element-datarecordset_type-complextype-visio-xml"></a>Elemento Rel (DataRecordSet_Type complexType) (XML do Visio)

Especifica uma relação com uma parte com o recordset associado e as informações de vinculação de dados.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Especifica uma instância de um recordset e informações de vinculação de dados armazenadas no desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|r:id  <br/> |xsd:string  <br/> Consulte os comentários.  <br/> |obrigatório  <br/> |Especifica uma relação com uma parte.  <br/> |"rId#"  <br/> Consulte os comentários.  <br/> |
   
## <a name="remarks"></a>Comentários

O valor do atributo **r:id** deve ser um **tipo ST_RelationshipID** usuário. O **ST_RelationshipID** tipo é uma cadeia de caracteres que deve estar no formato 'rId#', onde o caractere final deve ser um número. O número deve ser exclusivo entre todos os elementos irmãos do **elemento Rel.** 
  
Para obter mais informações sobre o ST_RelationshipID, consulte a especificação [ISO/IEC 29500 Parte 1.](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)
  

