---
title: Implementação do objeto de controle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b4b225f7e048ef40a79c4b258629cb01b79368d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565827"
---
# <a name="control-object-implementation"></a>Implementação do objeto de controle

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Controlar objetos ou objetos que suportam o [IMAPIControl: IUnknown](imapicontroliunknown.md) interface, são implementadas pelos provedores para adicionar funcionalidades a um botão que aparece em uma caixa de diálogo MAPI. Objetos de controle só podem ser implementados para botões. 
  
 **IMAPIControl** possui três métodos: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)e [Ativar](imapicontrol-activate.md). 
  
**GetState** para determinar se ou não desabilitar o botão de chamadas de MAPI. **GetState** é chamado nas seguintes situações: 
  
- Quando a caixa de diálogo na qual o botão aparece primeiro é exibida.
    
- Quando uma notificação de tabela de exibição é emitida para o botão. 
    
Defina o conteúdo do parâmetro _lpulState_ para MAPI_DISABLED se o usuário não pode interagir com o botão e MAPI_ENABLED se o usuário pode interagir. 
  
Quando o usuário clica no botão, **Ativar**chamadas MAPI. **Ativar** realiza a tarefa que tenha sido associada ao botão. Essa tarefa pode ser qualquer coisa apropriado para seu provedor, como exibir uma caixa de diálogo ou atualizar uma propriedade. Se a tarefa for bem sucedida porque o usuário cancelou a ele, retorne MAPI_E_USER_CANCEL. Para outras causas de falha, retorne o valor de erro apropriado. 
  
Se a tarefa for bem-sucedida e for vinculado a uma alteração de propriedade refletidos em outro controle, na caixa de diálogo, chame [ITableData::HrNotify](itabledata-hrnotify.md). **HrNotify** é chamado para emitir uma notificação de tabela de exibição com a propriedade de **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) da propriedade alterados na estrutura [TABLE_NOTIFICATION](table_notification.md) . Não coloque o novo valor da propriedade na estrutura; em vez disso, retorná-lo quando [IMAPIProp::GetProps](imapiprop-getprops.md) é chamado. Embora normalmente uma notificação de tabela de exibição não pode ser usada para desabilitar ou habilitar um controle, ele pode ser usado com um botão. MAPI atualizará o controle alterado para responder à notificação. 
  
MAPI chama o método do controle **GetLastError** quando **Ativar** retornará um erro que não seja MAPI_E_USER_CANCEL. Se **GetLastError** colocará informações de erro estendidas na estrutura [MAPIERROR](mapierror.md) que ele retorna o conteúdo do parâmetro _lppMAPIError_ , MAPI exibe para o usuário. 
  
## <a name="see-also"></a>Confira também



[Provedores de serviços MAPI](mapi-service-providers.md)

