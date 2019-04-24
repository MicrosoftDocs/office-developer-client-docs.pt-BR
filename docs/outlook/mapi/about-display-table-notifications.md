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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326408"
---
# <a name="about-display-table-notifications"></a>Sobre a exibição de notificações de tabela

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As notificações em uma tabela de exibição são enviadas pelo provedor de serviços responsável pela criação da tabela de exibição para MAPI. O MAPI registra para essas notificações chamando o método imApitable [:: Advise](imapitable-advise.md) da tabela de exibição e especificando o evento de tabela modificada. 
  
Como em todas as notificações de tabela, as notificações de tabela de exibição incluem uma estrutura [TABLE_NOTIFICATION](table_notification.md) . Somente os membros **ulTableEvent** e **propIndex** dessa estrutura são significativos; os outros membros são ignorados. O membro **ulTableEvent** é definido como TABLE_ROW_MODIFIED e o membro **propIndex** é definido como o valor da coluna **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) na linha correspondente. O MAPI responde à notificação chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps para a propriedade exibida no controle e exibindo o novo valor. 
  
As notificações de tabela de exibição podem ser usadas por um provedor de serviços para coordenar alterações em controles relacionados na caixa de diálogo. Por exemplo, se a implementação da interface de propriedade precisa atualizar um ou mais campos na caixa de diálogo, talvez em resposta a outro controle que tenha definido o sinalizador DT_SET_IMMEDIATE em sua propriedade **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) — Ele pode gerar uma notificação de exibição de tabela. Uma notificação de tabela de exibição pode alertar a implementação de interface de propriedade que o valor de um ou mais controles precisa ser relido devido a uma alteração que está sendo feita ou a um evento externo que ocorre. 
  
Um provedor de serviços pode emitir notificações de tabela de exibição por:
  
- Chamar [ITableData:: HrNotify](itabledata-hrnotify.md), se a tabela de exibição foi criada com um objeto Table Data.
    
    - Ou
    
- Usando seu próprio código, se a tabela de exibição foi criada com a implementação **** IMAPITable do provedor. 
    
MAPI responde a exibir notificações de tabela quando necessário, relendo o valor de um controle da implementação da interface de propriedade. A tabela a seguir descreve os detalhes em torno de como o MAPI lida com notificações para tipos específicos de controles.
  
|**Control**|**Ação MAPI**|
|:-----|:-----|
|Botão  <br/> |Chama [IMAPIProp:: OpenProperty](imapiprop-openproperty.md)para recuperar o objeto de controle por meio da propriedade representada pelo membro **UlPRControl** da estrutura [DTBLBUTTON](dtblbutton.md) se a chamada tiver falhado anteriormente. Chama o IMAPIControl do objeto de controle [:: GetState](imapicontrol-getstate.md) para determinar se o botão deve ser habilitado e habilita ou desabilita o botão adequadamente.  <br/> |
|Caixa de seleção  <br/> |Relê o valor para o membro **ulPRPropertyName** .  <br/> |
|Caixa de combinação  <br/> |Reabre a tabela associada ao membro **ulPRTableName** da estrutura [DTBLCOMBOBOX](dtblcombobox.md) . Relê todas as linhas, incluindo o valor do membro **ulPRPropertyName**.  <br/> |
|Caixa de listagem suspensa  <br/> |Reabre a tabela associada ao membro **ulPRTableName** da estrutura [DTBLDDLBX](dtblddlbx.md) e relê todas as linhas. Chama [IMAPIProp::](imapiprop-getprops.md) GetProps para recuperar os valores das propriedades armazenadas nos membros **ulPRDisplayProperty** e **ulPRSetProperty** .  <br/> |
|Editar  <br/> |Relê a propriedade e reexibe.  <br/> |
|Caixa de grupo  <br/> |Ignora a notificação.  <br/> |
|Rótulo  <br/> |Ignora a notificação.  <br/> |
|Caixa de listagem de seleção múltipla  <br/> |Se uma das colunas for um identificador de entrada, atualizará a caixa de listagem. O objeto correspondente não é fechado ou recarregado.  <br/> |
|Caixa de listagem de seleção única  <br/> |Lê a propriedade Set, tentando identificá-la.  <br/> |
|Caixa de listagem de vários valores  <br/> |Relê a propriedade e preenche novamente a caixa de listagem.  <br/> |
|Página com guias  <br/> |Não há notificações para este controle; Tudo é estático.  <br/> |
|Botão de opção  <br/> |Relê a propriedade que está associada ao botão e é armazenada no membro **ulPropTag** da estrutura [DTBLRADIOBUTTON](dtblradiobutton.md) e faz a seleção apropriada com os controles.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

