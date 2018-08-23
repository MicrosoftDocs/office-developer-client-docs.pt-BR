---
title: Sobre notificações de tabela de exibição
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 487a5dbcdefe901b514083ee910972354574bd82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564455"
---
# <a name="about-display-table-notifications"></a>Sobre notificações de tabela de exibição

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Notificações em uma tabela de exibição são enviadas pelo provedor de serviços responsável por criar a tabela de exibição MAPI. MAPI registra para essas notificações chamando o método de [IMAPITable::Advise](imapitable-advise.md) uma exibição da tabela e especificando o evento modificada da tabela. 
  
Assim como acontece com todas as notificações de tabela exibir notificações de tabela incluem uma estrutura [TABLE_NOTIFICATION](table_notification.md) . Somente o **ulTableEvent** e os membros de **propIndex** desta estrutura são significativos; os outros membros são ignorados. O membro **ulTableEvent** é definido como TABLE_ROW_MODIFIED e o membro **propIndex** é definido como o valor da coluna **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) na linha correspondente. MAPI responde à notificação chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) para a propriedade exibida no controle e exibindo o novo valor. 
  
Notificações de tabela de exibição podem ser usadas por um provedor de serviços para coordenar mudanças para controles relacionados na caixa de diálogo. Por exemplo, se a implementação de interface de propriedade precisa atualizar um ou mais campos na caixa de diálogo — talvez em resposta a um outro controle que definiu o sinalizador DT_SET_IMMEDIATE em sua propriedade **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) — ele pode gerar uma notificação de tabela de exibição. Exibir uma notificação de tabela alertando a implementação de interface de propriedade que o valor de um ou mais controles precisa ser lidos novamente devido a uma alteração seja feita ou uma ocorrência do evento externo. 
  
Um provedor de serviços pode emitir notificações de tabela de exibição por:
  
- Chamando [ITableData::HrNotify](itabledata-hrnotify.md), se a tabela de exibição foi criada com um objeto de dados de tabela.
    
    - Ou -
    
- Usando seu próprio código, se a tabela de exibição foi criada com a implementação do provedor **IMAPITable** . 
    
MAPI responde para exibir as notificações de tabela quando necessário por releitura o valor de um controle a partir da implementação de interface de propriedade. A tabela a seguir descreve os detalhes ao redor como MAPI manipula notificações para tipos específicos de controles.
  
|**Control**|**Ação de MAPI**|
|:-----|:-----|
|Botão  <br/> |Chama [IMAPIProp::OpenProperty](imapiprop-openproperty.md)para recuperar o objeto de controle por meio da propriedade representado pelo membro **ulPRControl** da estrutura [DTBLBUTTON](dtblbutton.md) se a chamada teve falhou anteriormente. Chama [IMAPIControl::GetState](imapicontrol-getstate.md) para determinar se o botão deve ser habilitado e habilita ou desabilita o botão de acordo do objeto controle.  <br/> |
|Caixa de seleção  <br/> |Rereads o valor para o membro **ulPRPropertyName** .  <br/> |
|Caixa de combinação  <br/> |Reabre a tabela associada ao membro **ulPRTableName** da estrutura [DTBLCOMBOBOX](dtblcombobox.md) . Rereads todas as linhas, incluindo o valor para o membro **ulPRPropertyName**.  <br/> |
|Caixa de listagem drop-down  <br/> |Reabre a tabela associada ao membro **ulPRTableName** da estrutura [DTBLDDLBX](dtblddlbx.md) e rereads todas as linhas. Chama [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar os valores para as propriedades armazenadas em membros **ulPRSetProperty** e o **ulPRDisplayProperty** .  <br/> |
|EDIT  <br/> |Rereads a propriedade e exibe novamente.  <br/> |
|Caixa de grupo  <br/> |Ignora a notificação.  <br/> |
|Rótulo  <br/> |Ignora a notificação.  <br/> |
|Caixa de listagem de seleção vários  <br/> |Se uma das colunas é um identificador de entrada, atualiza a caixa de listagem. Objeto correspondente não está fechado ou recarregado.  <br/> |
|Caixa de listagem de seleção única  <br/> |Lê a propriedade set, tentando identificá-lo.  <br/> |
|Caixa de listagem com valores múltiplos  <br/> |Rereads a propriedade e preenche a caixa de listagem.  <br/> |
|Página com guias  <br/> |Não há nenhuma notificação para este controle; tudo é estático.  <br/> |
|Botão de opção  <br/> |Rereads a propriedade que está associado com o botão e é armazenada no membro **ulPropTag** da estrutura [DTBLRADIOBUTTON](dtblradiobutton.md) e faz com que a seleção apropriada com os controles.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

