---
title: Propriedade canônica PidTagControlType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7bdb02f72ba14a36c8a4c218cd5f0631e7145e6a
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734200"
---
# <a name="pidtagcontroltype-canonical-property"></a>Propriedade canônica PidTagControlType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor que indica um tipo de controle para um controle usado em uma caixa de diálogo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTROL_TYPE  <br/> |
|Identificador:  <br/> |0x3F02  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabela de exibição MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ter exatamente um dos seguintes valores:
    
DTCT_LABEL (0x00000000)
  
> Um rótulo da caixa de diálogo.
   
DTCT_EDIT (0x00000001)
  
> Uma caixa de texto de edição de caixa de diálogo.

DTCT_LBX (0x00000002)
  
> Uma caixa de listagem de diálogo.
    
DTCT_COMBOBOX (0x00000003)
  
> Uma caixa de combinação de diálogo.

DTCT_DDLBX (0x00000004)
  
> Uma caixa de listagem da caixa de diálogo.

DTCT_CHECKBOX (0x00000005)
  
> Uma caixa de seleção de diálogo.

DTCT_GROUPBOX (0x00000006)
  
> Uma caixa de diálogo de grupo.
  
DTCT_BUTTON (0x00000007)
  
> Um controle de botão de caixa de diálogo.
    
DTCT_PAGE (0x00000008)
  
> Uma página com guias de caixa de diálogo.
    
DTCT_RADIOBUTTON (0x00000009)
  
> Um botão de rádio da caixa de diálogo.
    
DTCT_MVLISTBOX (0x0000000B)
  
> Uma caixa de listagem de vários valores preenchida por uma propriedade de vários valores da cadeia de caracteres de tipo.
    
DTCT_MVDDLBX (0x0000000C)
  
> Uma caixa de listagem de valores múltiplos preenchida por uma propriedade de vários valores da cadeia de caracteres do tipo.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

