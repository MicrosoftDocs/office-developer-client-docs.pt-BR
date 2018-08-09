---
title: Elemento DocumentSheet (VisioDocument_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Especifica uma estrutura DocumentSheet.
ms.openlocfilehash: 50332759ff3bbe94887371d48c4a2e729243fb32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771767"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a>Elemento DocumentSheet (VisioDocument_Type complexType) ('Visio XML')

Especifica uma estrutura DocumentSheet.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |O elemento raiz de um documento do Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Célula](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma célula em um DocumentSheet.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Descreve como se o nome tiver sido personalizado pelo usuário.  <br/> |Valores do tipo xsd:Boolean.  <br/> |
|IsCustomNameU  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Descreve como se o nome universal foi personalizado pelo usuário.  <br/> |Valores do tipo xsd:Boolean.  <br/> |
|Nome  <br/> |XSD: String  <br/> |opcional  <br/> |Especifica o nome de dependente de idioma do DocumentSheet.  <br/> |Valores do tipo xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |opcional  <br/> |Especifica o nome de independente de idioma do DocumentSheet.  <br/> |Valores do tipo xsd: String.  <br/> |
|UniqueID  <br/> |XSD: String  <br/> |opcional  <br/> |Cadeia de caracteres opcional. Um GUID (identificador global exclusivo) que identifica a forma.  <br/> |Valores do tipo xsd: String.  <br/> |
   

