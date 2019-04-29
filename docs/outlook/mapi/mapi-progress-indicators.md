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
  
Muitas das operações que você realiza para os clientes podem levar muito tempo para serem concluídas. Para informar os clientes sobre o progresso de uma operação extensa, você pode mostrar um indicador que exibe graficamente a parte concluída de uma operação em um determinado ponto, desde o início da operação até sua conclusão. O indicador de progresso mostra uma porcentagem da operação total a ser concluída.
  
Os seguintes métodos suportam operações demoradas e a exibição de um indicador de progresso:
  
- [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md), [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D Eletemessages](imapifolder-deletemessages.md), [IMAPIFolder::D Eletefolder](imapifolder-deletefolder.md), [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md)e [IMAPIFolder:](imapifolder-setreadflags.md): SetReadFlags.
    
- [IMAPIProp:: CopyProps](imapiprop-copyprops.md) e [IMAPIProp:: CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md), [IMAPISupport::D ocopyto](imapisupport-docopyto.md), [IMAPISupport:: CopyFolder](imapisupport-copyfolder.md)e [IMAPISupport::](imapisupport-copymessages.md)CopyMessages.
    
- [IMessage::D eleteattach](imessage-deleteattach.md).
    
- [IABContainer:: CopyEntries](iabcontainer-copyentries.md).
    
Para exibir um indicador de progresso, o MAPI define um objeto Progress. Os objetos Progress implementam a interface [método imapiprogress: IUnknown](imapiprogressiunknown.md) , uma interface que inclui métodos para o estabelecimento do intervalo do indicador e a criação da exibição. O MAPI fornece uma implementação de objeto Progress como alguns clientes. Você deve usar a implementação de um cliente, se um for fornecido, como um parâmetro de entrada para o método executando a operação. Se o cliente passar NULL em vez de um ponteiro para um objeto Progress, use a implementação do MAPI chamando o método [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) . 
  
## <a name="see-also"></a>Confira também



[Provedores de serviço MAPI](mapi-service-providers.md)

