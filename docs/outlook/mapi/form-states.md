---
title: Estados de formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327514"
---
# <a name="form-states"></a>Estados de formulários

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os objetos Form podem estar em um dos cinco Estados distintos, dependendo de quais métodos foram chamados neles e se algum erro ocorreu na execução desses métodos. Os Estados são descritos nos seguintes tópicos:
  
- [Estado não inicializado](uninitialized-state.md)
    
- [Estado normal](normal-state.md)
    
- [Estado noRabisco](noscribble-state.md)
    
- [Estado HandsOffAfterSave](handsoffaftersave-state.md)
    
- [Estado HandsOffFromNormal](handsofffromnormal-state.md)
    
Os Estados se relacionam principalmente com o status dos dados no objeto Form. Os diferentes Estados refletem se os dados precisam ser salvos, se o objeto Form deve permitir modificações nos dados e o ponto no processo de salvar os dados em que o formulário está. Assim, os Estados e as transições de formulário entre eles têm mais a fazer com a implementação do seu servidor de formulário de métodos de interface [IPersistMessage: IUnknown](ipersistmessageiunknown.md) do que outros. O conhecimento desses Estados é muito útil para a implementação adequada das interfaces de formulário MAPI que seu servidor de formulários deve implementar. 
  
Os tópicos desta seção descrevem os vários Estados, juntamente com as ações permitidas que causam transições para outros Estados. As transições não listadas nos tópicos não são permitidas. Se os objetos de formulário fizerem transições não permitidas entre Estados, elas não se comportarão de maneiras que os clientes de mensagens esperam e possam causar comportamento de cliente ou de formulário imprevisível.
  
> [!NOTE]
> Algumas transições de estado dependem das informações de Estados anteriores. O servidor de formulário provavelmente terá que implementar um sinalizador em seus objetos Form para indicar se os valores das propriedades da mensagem foram alterados para facilitar as alterações de estado posteriores. 
  
## <a name="see-also"></a>Confira também

- [Desenvolver servidores de formulário MAPI](developing-mapi-form-servers.md)

