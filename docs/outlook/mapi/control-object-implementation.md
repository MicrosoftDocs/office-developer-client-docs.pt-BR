---
title: Implementação do objeto Control
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8304021565638f8a5893d0be8cd6a94ed62a8d95
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422604"
---
# <a name="control-object-implementation"></a>Implementação do objeto Control

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Objetos de controle, ou objetos que suportam o [IMAPIControl : interface IUnknown,](imapicontroliunknown.md) são implementados por provedores para adicionar funcionalidade a um botão que aparece em uma caixa de diálogo MAPI. Os objetos de controle só podem ser implementados para botões. 
  
 **IMAPIControl** tem três métodos: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)e [Activate](imapicontrol-activate.md). 
  
MAPI calls **GetState** to determine whether or not to disable the button. **GetState** é chamado nas seguintes situações: 
  
- Quando a caixa de diálogo na qual o botão aparece é exibida pela primeira vez.
    
- Quando uma notificação de tabela de exibição é emitida para o botão. 
    
De definir o conteúdo do parâmetro  _lpulState_ como MAPI_DISABLED se o usuário não puder interagir com o botão e MAPI_ENABLED se o usuário puder interagir. 
  
Quando o usuário clica no botão, MAPI chama **Activate**. **A** ativação executa a tarefa que foi associada ao botão. Essa tarefa pode ser qualquer coisa apropriada para seu provedor, como exibir uma caixa de diálogo ou atualizar uma propriedade. Se a tarefa não tiver êxito porque o usuário a cancelou, retorne MAPI_E_USER_CANCEL. Para outras causas de falha, retorne o valor de erro apropriado. 
  
Se a tarefa for bem-sucedida e estiver vinculada a uma alteração de propriedade que é refletida em outro controle na caixa de diálogo, chame [ITableData::HrNotify](itabledata-hrnotify.md). **HrNotify** é chamado para emitir uma notificação de tabela de exibição com a propriedade **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) alterada na estrutura [TABLE_NOTIFICATION](table_notification.md) exibição. Não coloque o novo valor de propriedade na estrutura; em vez disso, retorne-o [quando IMAPIProp::GetProps](imapiprop-getprops.md) for chamado. Embora normalmente uma notificação de tabela de exibição não possa ser usada para desabilitar ou habilitar um controle, ela pode ser usada com um botão. O MAPI atualizará o controle alterado para responder à notificação. 
  
MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL. Se **GetLastError** coloca informações de erro estendidas na estrutura [MAPIERROR](mapierror.md) que retorna no conteúdo do parâmetro  _lppMAPIError,_ MAPI exibe para o usuário. 
  
## <a name="see-also"></a>Confira também



[Provedores de Serviços MAPI](mapi-service-providers.md)

