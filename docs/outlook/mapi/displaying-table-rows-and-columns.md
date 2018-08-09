---
title: Exibir linhas e colunas da tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ee60e64559a0b4163074ddb62ed72c4600c8e03d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766437"
---
# <a name="displaying-table-rows-and-columns"></a>Exibir linhas e colunas da tabela

  
  
**Aplica-se a**: Outlook 
  
 Uma página de propriedades pode ser usada por um provedor de catálogo de endereços para permitir que os usuários definam novos destinatários de email. 
  
A tabela de exibição correspondente contém quatro linhas, uma para cada controle. Os valores para as colunas que indicam a posição são os seguintes.
  
|**Control**|**XPOS**|**YPOS**|**DELTAX**|**DELTAY**|
|:-----|:-----|:-----|:-----|:-----|
|Rótulo de nome de exibição  <br/> |14  <br/> |18  <br/> |49  <br/> |8  <br/> |
|Caixa de edição de nome de exibição  <br/> |76  <br/> |16  <br/> |89  <br/> |12  <br/> |
|Etiqueta de endereço de email  <br/> |14  <br/> |42  <br/> |50  <br/> |8  <br/> |
|Caixa de edição de endereço de email  <br/> |76  <br/> |40  <br/> |89  <br/> |12  <br/> |
|Caixa de seleção  <br/> |14  <br/> |64  <br/> |90  <br/> |12  <br/> |
   
Esta tabela próxima sugere valores apropriados para o tipo do controle, sua propriedade **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) e bitmask dos sinalizadores, sua propriedade **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
  
|**Control**|**Tipo**|**Flags**|
|:-----|:-----|:-----|
|Rótulo de nome de exibição  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Caixa de edição de nome de exibição  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Etiqueta de endereço de email  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Caixa de edição de endereço de email  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Caixa de seleção  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
A tabela final lista todos os controles com o conteúdo da sua estrutura de controle associado. Observe que o valor para cada um dos controles label aparece na memória diretamente seguindo a estrutura.
  
|**Control**|**Estrutura**|
|:-----|:-----|
|Rótulo de nome de exibição  <br/> |{0, sizeof(DTBLLABEL)} "Nome de exibição:"  <br/> |
|Caixa de edição de nome de exibição  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}  <br/> |
|Etiqueta de endereço de email  <br/> |{0, sizeof(DTBLLABEL)} "Endereço de email:"  <br/> |
|Caixa de edição de endereço de email  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}  <br/> |
|Caixa de seleção  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> Os botões **Okey**, **Cancelar**e **Ajuda** não são incluídos na tabela de exibição. A interface do usuário pode adicionar contexto para uma caixa de diálogo adicionando controles não esteja na tabela de exibição. 
  
## <a name="see-also"></a>Confira também



[Implementação da tabela de exibição](display-table-implementation.md)

