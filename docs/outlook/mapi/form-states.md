---
title: Estados de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 969aca6fd37f237a607df36cc58f249828449e27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766618"
---
# <a name="form-states"></a>Estados de formulário

**Aplica-se a**: Outlook 
  
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

