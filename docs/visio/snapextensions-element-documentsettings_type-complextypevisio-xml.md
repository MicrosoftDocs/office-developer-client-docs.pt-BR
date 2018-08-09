---
title: Elemento SnapExtensions (DocumentSettings_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Especifica se uma configuração de extensão de snap específico está habilitada ou desabilitada para a janela ativa.
ms.openlocfilehash: 4c00d8d45c1eb33f57f727779db91e358a83a969
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773008"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>Elemento SnapExtensions (DocumentSettings_Type complexType) ('Visio XML')

Especifica se uma configuração de extensão de snap específico está habilitada ou desabilitada para a janela ativa. 
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document  <br/> |
   
## <a name="definition"></a>Definição

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contém os elementos que especificam as configurações do documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

Nenhum.
  
## <a name="remarks"></a>Comentários

O valor do elemento **SnapExtensions** pode ser uma soma dos valores na tabela a seguir. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Ajustar a nada.  <br/> |
|1  <br/> |Ajustar à extensão da caixa de alinhamento.  <br/> |
|2  <br/> |Ajustar a extensão do eixo central.  <br/> |
|4  <br/> |Ajustar à extensão tangente da curva.  <br/> |
|8  <br/> |Ajustar a extensão de ponto de extremidade.  <br/> |
|16  <br/> |Ajustar a extensão do ponto médio.  <br/> |
|32  <br/> |Ajustar à extensão linear.  <br/> |
|64  <br/> |Ajustar à extensão da curva.  <br/> |
|128  <br/> |Ajustar à extensão perpendiculares do ponto de extremidade.  <br/> |
|256  <br/> |Ajustar à extensão perpendiculares do ponto médio.  <br/> |
|512  <br/> |Ajustar à extensão horizontal do ponto de extremidade.  <br/> |
|1024  <br/> |Ajustar à extensão vertical do ponto de extremidade.  <br/> |
|2048  <br/> |Ajustar a extensão de centro da elipse.  <br/> |
|4096  <br/> |Ajustar à extensão isométrica ângulos.  <br/> |
   

