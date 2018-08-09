---
title: Elemento DocumentSettings (VisioDocument_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: Contém os elementos que especificam as configurações do documento.
ms.openlocfilehash: 8cd10e43b95918ccd2ceaa75a47c9e93de2acc14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771748"
---
# <a name="documentsettings-element-visiodocumenttype-complextype-visio-xml"></a>Elemento DocumentSettings (VisioDocument_Type complexType) ('Visio XML')

Contém os elementos que especificam as configurações do documento.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
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
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |Uma MIME (Multipurpose Internet Mail Extensions) codificado arquivo de (VSU) de interface do usuário do Microsoft Visio que representa as barras de ferramentas personalizadas.  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Contém o nome do arquivo de (. VSU) da interface do usuário do Microsoft Visio que define os menus personalizados e aceleradores para um documento.  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Contém o nome do arquivo de (. VSU) da interface do usuário do Microsoft Visio que define as barras de ferramentas personalizadas e barras de status para um documento.  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Especifica se o recurso de grade dinâmica está habilitado para um documento ou janela.  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Especifica os objetos que formas coladas a quando a colagem está habilitada no documento.  <br/> |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Especifica se o usuário é impedido de exclusão ou a edição de páginas do plano de fundo.  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Especifica se o usuário é impedido de criar, editar ou excluir mestres. Independentemente dessa configuração, o usuário ainda pode criar instâncias de mestres.  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Especifica se o usuário é impedido de seleção de formas que têm sua elemento **LockSelect** definido como 1.  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Especifica se o usuário é impedido de criação ou edição de estilos.  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contém uma coleção de elementos de **SnapAngle** .  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Especifica se uma configuração de extensão de snap específico está habilitada ou desabilitada para a janela ativa.  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Especifica os objetos que as formas ajustadas ajustar quando está ativo na janela.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Especifica a ID de um elemento de **folha de estilos** .  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|DefaultGuideStyle  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Especifica a ID de um elemento de **folha de estilos** .  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|DefaultLineStyle  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Especifica a ID de um elemento de **folha de estilos** .  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|DefaultTextStyle  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Especifica a ID de um elemento de **folha de estilos** .  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|TopPage  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Especifica a identificação da página que deve ser exibida quando o documento é aberto pelo Microsoft Visio.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

