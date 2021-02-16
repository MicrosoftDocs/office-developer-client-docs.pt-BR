---
title: Enviando e recebendo notificações de formulário
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
# <a name="sending-and-receiving-form-notifications"></a>Enviando e recebendo notificações de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As notificações de formulário são usadas em MAPI para facilitar a comunicação entre o formulário e o visualizador, bem como do visualizador para o formulário.
  
Os formulários enviam notificações ao visualizador quando ocorre um dos seguintes eventos:
  
- O formulário está fechado.
    
- Uma nova mensagem é carregada no formulário.
    
- Uma operação de salvar é concluída.
    
- Uma mensagem é enviada.
    
Cada um desses tipos de evento corresponde a um método específico em [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), uma das interfaces que o visualizador de formulário deve implementar. When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink. Por exemplo, quando chega uma nova mensagem que o visualizador deve incluir na exibição, o formulário chama o método [IMAPIViewAdviseSink::OnNewMessage.](imapiviewadvisesink-onnewmessage.md) 
  
Implemente o sink de aconselhador de exibição de uma maneira que faça sentido para o visualizador; não há implementação padrão. Por exemplo, em **OnNewMessage,** você pode atualizar a exibição da tabela de conteúdo da pasta atual para incluir a mensagem recém-chegada. In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.
  
Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message. Para notificar um formulário, chame um dos métodos de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) ou [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md). Chame **OnChange** para comunicar o status. For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item. 
  
Chame **OnActivateNext** para alertar o formulário sobre a chegada de uma nova mensagem que ele pode ou não ser capaz de exibir. Passe a classe de mensagem da mensagem para **OnActivateNext**. 
  
As notificações por um objeto de formulário para o aplicativo cliente são manipuladas pela interface **IMAPIViewAdviseSink do** aplicativo cliente. Para obter mais informações, [consulte IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).
  

