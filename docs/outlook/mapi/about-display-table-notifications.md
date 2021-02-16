---
title: Sobre a exibição de notificações de tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 41e6a2c8b6856bf072972325e7e08aabe3e17446
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430011"
---
# <a name="about-display-table-notifications"></a>Sobre a exibição de notificações de tabela

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As notificações em uma tabela de exibição são enviadas pelo provedor de serviços responsável pela criação da tabela de exibição para MAPI. MAPI registers for these notifications by calling a display table's [IMAPITable::Advise](imapitable-advise.md) method and specifying the table modified event. 
  
Assim como em todas as notificações de tabela, as notificações de tabela de exibição [incluem TABLE_NOTIFICATION](table_notification.md) estrutura. Somente os **membros ulTableEvent** e **propIndex** dessa estrutura são significativos; os outros membros são ignorados. O **membro ulTableEvent** é definido como TABLE_ROW_MODIFIED e o membro **propIndex** é definido como o valor da coluna **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) na linha correspondente. MAPI responds to the notification by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the property displayed in the control and by displaying the new value. 
  
As notificações da tabela de exibição podem ser usadas por um provedor de serviços para coordenar as alterações nos controles relacionados na caixa de diálogo. Por exemplo, se a implementação da interface de propriedade precisar atualizar um ou mais campos na caixa de diálogo — talvez em resposta a outro controle que tenha definido o sinalizador DT_SET_IMMEDIATE em sua propriedade **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) — ele poderá gerar uma notificação de tabela de exibição. Uma notificação da tabela de exibição pode alertar a implementação da interface de propriedade de que o valor de um ou mais controles precisa ser relido devido a uma alteração ou um evento externo ocorrendo. 
  
Um provedor de serviços pode emitir notificações de tabela de exibição:
  
- Chamar [ITableData::HrNotify](itabledata-hrnotify.md), se a tabela de exibição foi criada com um objeto de dados de tabela.
    
    - Ou -
    
- Usando seu próprio código, se a tabela de exibição foi criada com a implementação **IMAPITable do** provedor. 
    
MAPI responds to display table notifications when necessary by rereading a control's value from the property interface implementation. A tabela a seguir descreve os detalhes em torno de como o MAPI lida com notificações para tipos específicos de controles.
  
|**Control**|**Ação MAPI**|
|:-----|:-----|
|Botão  <br/> |Chama [IMAPIProp::OpenProperty](imapiprop-openproperty.md)para recuperar o objeto de controle por meio da propriedade representada pelo membro **ulPRControl** da estrutura [DTBLBUTTON](dtblbutton.md) se a chamada tiver falhado anteriormente. Chama o [IMAPIControl::GetState](imapicontrol-getstate.md) do objeto de controle para determinar se o botão deve ser habilitado e habilita ou desabilita o botão de acordo.  <br/> |
|Caixa de seleção  <br/> |Releia o valor do **membro ulPRPropertyName.**  <br/> |
|Caixa de combinação  <br/> |Reabre a tabela associada ao **membro ulPRTableName** da [estrutura DTBLCOMBOBOX.](dtblcombobox.md) Releia todas as linhas, incluindo o valor do **membro ulPRPropertyName.**  <br/> |
|Caixa de listagem drop-down  <br/> |Reabre a tabela associada ao **membro ulPRTableName** da estrutura [DTBLDDLBX](dtblddlbx.md) e releia todas as linhas. Chama [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar os valores das propriedades armazenadas nos **membros ulPRDisplayProperty** e **ulPRSetProperty.**  <br/> |
|Editar  <br/> |Releia a propriedade e as redisplays.  <br/> |
|Caixa de grupo  <br/> |Ignora a notificação.  <br/> |
|Rótulo  <br/> |Ignora a notificação.  <br/> |
|Caixa de listagem de seleção múltipla  <br/> |Se uma das colunas for um identificador de entrada, atualiza a caixa de listagem. O objeto correspondente não é fechado ou recarregado.  <br/> |
|Caixa de listagem de seleção única  <br/> |Lê a propriedade set, tentando identificá-la.  <br/> |
|Caixa de listagem de vários valores  <br/> |Rereads the property and repopulates the list box.  <br/> |
|Página com guias  <br/> |Não há notificações para esse controle; tudo é estático.  <br/> |
|Botão de rádio  <br/> |Rereads the property that is associated with the button and is stored in the **ulPropTag** member of the [DTBLRADIOBUTTON](dtblradiobutton.md) structure and makes the appropriate selection with the controls.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

