---
title: Indicadores de progresso MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cdfb6898146583b7da9b043eadd3acc09edbf292
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410704"
---
# <a name="mapi-progress-indicators"></a>Indicadores de progresso MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Muitas das operações que você executa para os clientes podem levar muito tempo para ser concluídas. Para informar os clientes sobre o progresso de uma operação demorada, você pode mostrar um indicador que exibe graficamente a parte concluída de uma operação em qualquer ponto, desde o início da operação até sua conclusão. O indicador de progresso mostra uma porcentagem da operação total a ser concluída.
  
Os métodos a seguir suportam operações demoradas e a exibição de um indicador de progresso:
  
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::D eleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)e [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md) e [IMAPIProp::CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md), [IMAPISupport::D oCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)e [IMAPISupport::CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::D eleteAttach](imessage-deleteattach.md).
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md).
    
Para exibir um indicador de progresso, MAPI define um objeto de progresso. Os objetos de progresso implementam a interface [IMAPIProgress : IUnknown,](imapiprogressiunknown.md) uma interface que inclui métodos para estabelecer o intervalo do indicador e criar a exibição. O MAPI fornece uma implementação de objeto de progresso, assim como alguns clientes. Você deve usar a implementação de um cliente, se for fornecida, como um parâmetro de entrada para o método que executa a operação. Se o cliente passar NULL em vez de um ponteiro para um objeto de progresso, use a implementação de MAPI chamando o [método IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md) 
  
## <a name="see-also"></a>Confira também



[Provedores de Serviços MAPI](mapi-service-providers.md)

