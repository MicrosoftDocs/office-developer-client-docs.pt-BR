---
title: Exibindo linhas e colunas da tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f9f1cc0bebf3c90a5c12f2714e8ab7eea59104da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407113"
---
# <a name="displaying-table-rows-and-columns"></a>Exibindo linhas e colunas da tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Uma página de propriedades pode ser usada por um provedor de agendas para permitir que os usuários definam novos destinatários de email. 
  
A tabela de exibição correspondente contém quatro linhas, uma para cada controle. Os valores para as colunas que indicam a posição são os a seguir.
  
|**Control**|**XPOS**|**YPOS**|**DELTAX**|**DELTAY**|
|:-----|:-----|:-----|:-----|:-----|
|Rótulo de nome de exibição  <br/> |14   <br/> |18   <br/> |49  <br/> |8   <br/> |
|Caixa de edição de nome de exibição  <br/> |76  <br/> |16   <br/> |89  <br/> |12   <br/> |
|Rótulo de endereço de email  <br/> |14   <br/> |42  <br/> |50  <br/> |8   <br/> |
|Caixa de edição de endereço de email  <br/> |76  <br/> |40  <br/> |89  <br/> |12   <br/> |
|Caixa de seleção  <br/> |14   <br/> |64  <br/> |90  <br/> |12   <br/> |
   
Esta próxima tabela sugere os valores apropriados para o tipo do controle, sua propriedade **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) e bitmask de sinalizadores, sua **propriedade PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
  
|**Control**|**Tipo**|**Flags**|
|:-----|:-----|:-----|
|Rótulo de nome de exibição  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Caixa de edição de nome de exibição  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Rótulo de endereço de email  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Caixa de edição de endereço de email  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Caixa de seleção  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
A tabela final lista cada controle com o conteúdo de sua estrutura de controle associada. Observe que o valor de cada um dos controles de rótulo aparece na memória logo após a estrutura.
  
|**Control**|**Estrutura**|
|:-----|:-----|
|Rótulo de nome de exibição  <br/> |{sizeof(DTBLLABEL), 0} "Nome para exibição:"  <br/> |
|Caixa de edição de nome de exibição  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}  <br/> |
|Rótulo de endereço de email  <br/> |{sizeof(DTBLLABEL), 0} "Endereço de email:"  <br/> |
|Caixa de edição de endereço de email  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}  <br/> |
|Caixa de seleção  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> Os **botões OK**, **Cancelar** e **Ajuda** não estão incluídos na tabela de exibição. A interface do usuário pode adicionar contexto a uma caixa de diálogo adicionando controles que não estão na tabela de exibição. 
  
## <a name="see-also"></a>Confira também



[Implementação da tabela de exibição](display-table-implementation.md)

