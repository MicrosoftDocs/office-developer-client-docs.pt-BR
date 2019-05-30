---
title: Elemento ProtectMasters (DocumentSettings_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Especifica se o usuário é impedido de criar, editar ou excluir formas mestras. O usuário ainda pode criar novas formas a partir de uma forma mestra, independentemente dessa configuração.
ms.openlocfilehash: 34ace8c873b133f44ea7bd7c9c2e4127a103a760
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540690"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a>Elemento ProtectMasters (DocumentSettings_Type complexType) (XML do Visio)

Especifica se o usuário é impedido de criar, editar ou excluir formas mestras. O usuário ainda pode criar novas formas a partir de uma forma mestra, independentemente dessa configuração. 
  
O intervalo de valores possíveis para esse elemento é ' 0 ' ou ' 1 '. Um valor de ' 0 ' indica que os usuários podem criar, editar ou excluir formas mestras. Um valor de ' 1 ' indica que os usuários não podem criar, editar ou excluir formas mestras.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contém elementos que especificam configurações de documentos.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

Nenhum
  

