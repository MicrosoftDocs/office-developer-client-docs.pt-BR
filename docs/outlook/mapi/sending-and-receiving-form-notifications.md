---
title: Enviar e receber notificações de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431852"
---
# <a name="sending-and-receiving-form-notifications"></a>Enviar e receber notificações de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As notificações de formulário são usadas em MAPI para facilitar a comunicação do formulário para o seu visualizador, bem como do seu visualizador para o formulário.
  
Os formulários enviam notificações para o seu visualizador quando ocorre um dos seguintes eventos:
  
- O formulário é fechado.
    
- Uma nova mensagem é carregada no formulário.
    
- Uma operação de salvamento foi concluída.
    
- Uma mensagem é enviada.
    
Cada um desses tipos de eventos corresponde a um método específico no [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), uma das interfaces que seu visualizador de formulários deve implementar. Quando ocorre um evento, o formulário chama o método **IMAPIViewAdviseSink** correspondente no coletor de aviso do visualizador. Por exemplo, quando uma nova mensagem chega que o seu visualizador deve incluir em sua exibição, o formulário chama o método [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) . 
  
Implemente seu coletor de aviso de exibição de uma maneira que faz sentido para o seu visualizador; Não há implementação padrão. Por exemplo, no **OnNewMessage** , você pode atualizar o modo de exibição da tabela de conteúdo da pasta atual para incluir a mensagem recém-criada. Em [IMAPIViewAdviseSink::](imapiviewadvisesink-onsubmitted.md)onsent, o método que é chamado quando você recebe um evento de mensagem enviado, você pode copiar a mensagem enviada para uma pasta Itens enviados.
  
Os formulários recebem uma notificação do seu visualizador quando ocorre uma alteração que afeta o formulário e quando você está carregando uma nova mensagem. Para notificar um formulário, chame um dos métodos de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::](imapiformadvisesink-onchange.md) OnChange ou [IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md). Chamar **** OnChange para comunicar o status. Por exemplo, se o formulário estiver exibindo o último item em uma pasta quando uma nova mensagem chegar, **** chame OnChange com o sinalizador VCSTATUS_NEXT definido para informar ao formulário que agora há um próximo item. 
  
Chamar **OnActivateNext** para alertar o formulário para a chegada de uma nova mensagem que pode ou não ser exibida. Passe a classe de mensagem da mensagem para **OnActivateNext**. 
  
As notificações de um objeto de formulário para o aplicativo cliente são manipuladas pela interface do **IMAPIViewAdviseSink** do aplicativo cliente. Para obter mais informações, consulte [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).
  

