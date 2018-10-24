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
ms.openlocfilehash: 195a82bfcc163ee01d2d42c71e79a8f5c9c620e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564630"
---
# <a name="form-states"></a>Estados de formulários

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Objetos de formulário podem estar em um dos cinco estados distintos, dependendo do que métodos tiverem sido chamados neles e se ocorreu algum erro na execução desses métodos. Os estados são descritos nos tópicos a seguir:
  
- [Estado não inicializado](uninitialized-state.md)
    
- [Estado normal](normal-state.md)
    
- [Estado de NoScribble](noscribble-state.md)
    
- [Estado de HandsOffAfterSave](handsoffaftersave-state.md)
    
- [Estado de HandsOffFromNormal](handsofffromnormal-state.md)
    
Os estados estão relacionadas principalmente até o status dos dados no objeto form. Os diferentes estados refletem se os dados precisam ser salvo, se o objeto de formulário deve permitir modificações aos dados, e que o ponto no processo de salvar os dados que o formulário está nesse. Sendo assim, o formulário Estados e transições entre elas têm mais a ver com a implementação do seu servidor de formulário do [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos que qualquer outra de interface. É muito útil para implementação adequada das interfaces de formulário de MAPI que seu servidor do formulário deve implementar o conhecimento desses estados. 
  
Os tópicos desta seção descrevem os diversos estados, juntamente com as ações permitidas que causam transições para outros estados. Qualquer transições não listadas nos tópicos não são permitidas. Se os objetos de formulário fizer não autorizadas transições entre estados, elas não serão se comportam das maneiras que os clientes de mensagens esperam e podem causar comportamento imprevisível do objeto de cliente ou formulário.
  
> [!NOTE]
> Algumas transições de estado dependem de informações nos estados anteriores. Seu servidor de formulário provavelmente terá de implementar um sinalizador em seus objetos de formulário para indicar se os valores das propriedades da mensagem foram alterados para facilitar posteriores alterações de estado. 
  
## <a name="see-also"></a>Confira também

- [Desenvolvimento de servidores de formulário MAPI](developing-mapi-form-servers.md)

