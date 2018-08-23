---
title: Indicadores de progresso MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8fc39c6d7da0970ee15cdd9dd67bfeef0997d7d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582865"
---
# <a name="mapi-progress-indicators"></a>Indicadores de progresso MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Muitas das operações que podem ser executadas para clientes podem levar muito tempo para ser concluída. Para informar aos clientes sobre o progresso de uma operação demorada, você pode mostrar um indicador que exibe graficamente a terminar parte de uma operação em qualquer ponto do início da operação para sua conclusão. O indicador de progresso mostra uma porcentagem do total a operação seja concluída.
  
Os seguintes métodos suportam operações demoradas e a exibição de um indicador de progresso:
  
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)e [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md) e [IMAPIProp::CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)e [IMAPISupport::CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::DeleteAttach](imessage-deleteattach.md).
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md).
    
Para exibir um indicador de progresso, MAPI define um objeto de andamento. Objetos de progresso implementar o [IMAPIProgress: IUnknown](imapiprogressiunknown.md) interface, uma interface que inclui métodos para estabelecer o intervalo do indicador e criando a exibição. MAPI fornece uma implementação de objeto de progresso como alguns clientes. Você deve usar a implementação de um cliente, se esta for fornecida, como um parâmetro de entrada para o método executar a operação. Se o cliente passa NULL em vez de um ponteiro para um objeto de andamento, use a implementação de MAPI chamando o método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) . 
  
## <a name="see-also"></a>Confira também



[Provedores de serviços MAPI](mapi-service-providers.md)

