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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429163"
---
# <a name="form-states"></a>Estados de formulários

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os objetos de formulário podem estar em um dos cinco estados distintos, dependendo de quais métodos foram chamados neles e se algum erro ocorreu ao executar esses métodos. Os estados são descritos nos seguintes tópicos:
  
- [Estado não reinicializado](uninitialized-state.md)
    
- [Estado Normal](normal-state.md)
    
- [Estado NoScribble](noscribble-state.md)
    
- [Estado HandsOffAfterSave](handsoffaftersave-state.md)
    
- [Estado HandsOffFromNormal](handsofffromnormal-state.md)
    
Os estados se relacionam principalmente com o status dos dados no objeto form. Os diferentes estados refletem se os dados precisam ser salvos, se o objeto de formulário deve permitir modificações nos dados e em que ponto no processo de salvar os dados em que o formulário está. Dessa forma, os estados do formulário e as transições entre eles têm mais a ver com a implementação de [IPersistMessage :](ipersistmessageiunknown.md) métodos de interface IUnknown do que com qualquer outro servidor de formulário. O conhecimento desses estados é muito útil para a implementação adequada das interfaces de formulário MAPI que seu servidor de formulário deve implementar. 
  
Os tópicos desta seção descrevem os vários estados, juntamente com as ações permitidas que causam transições para outros estados. As transições não listadas nos tópicos não são permitidas. Se seus objetos de formulário fizerem transições não permitidos entre os estados, eles não se comportarão da maneira que os clientes de mensagens esperam e podem causar um comportamento imprevisível de objeto de cliente ou formulário.
  
> [!NOTE]
> Algumas transições de estado dependem de informações de estados anteriores. Seu servidor de formulário provavelmente terá que implementar um sinalizador em seus objetos de formulário para indicar se os valores das propriedades da mensagem foram alterados para facilitar alterações de estado posteriores. 
  
## <a name="see-also"></a>Confira também

- [Desenvolvendo servidores de formulário MAPI](developing-mapi-form-servers.md)

