---
title: Enviar e receber notificações de formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7148383c92b59adb9d3783e079e7c5f28c038eac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588990"
---
# <a name="sending-and-receiving-form-notifications"></a>Enviar e receber notificações de formulários

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Notificações de formulário são usadas em MAPI para facilitar a comunicação tanto contra o formulário para o visualizador, bem como seu visualizador para o formulário.
  
Formulários enviar notificações para seu visualizador quando um dos seguintes eventos ocorrer:
  
- O formulário é fechado.
    
- Uma nova mensagem é carregada no formulário.
    
- Uma operação de salvamento for concluída.
    
- Uma mensagem é enviada.
    
Cada um desses tipos de eventos corresponde a um método específico no [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), uma das interfaces do visualizador seu formulário deve implementar. Quando ocorre um evento, as chamadas de formulário, o método **IMAPIViewAdviseSink** correspondente no seu visualizador do coletor de eventos de aviso. Por exemplo, quando uma nova mensagem é recebida que seu visualizador deve incluir no seu vídeo, o formulário chama seu método [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) . 
  
Implementar sua opinião avise o coletor de eventos de forma que faz sentido para sua viewer; Não há nenhuma implementação padrão. Por exemplo, em **OnNewMessage** , você pode atualizar o modo de exibição de tabela de conteúdo da pasta atual para incluir a mensagem que acabou de chegar. No [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), o método que é chamado quando você recebe um evento de mensagem enviada, você pode copiar a mensagem enviada para uma pasta de itens enviados.
  
Formulários recebem a notificação do seu visualizador quando ocorre uma alteração que afeta o formulário e quando você está carregando uma nova mensagem. Para notificar um formulário, ligue para um dos métodos de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) ou [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md). Chamada **OnChange** para se comunicar status. Por exemplo, se o formulário está exibindo o último item em uma pasta, quando uma nova mensagem é recebida, chame **OnChange** com o sinalizador VCSTATUS_NEXT definido para informar o formulário que, agora, há um próximo item. 
  
**OnActivateNext** para o formulário para a chegada de uma nova mensagem de alerta de chamada que ele pode ou não ser capazes de exibir. Passe a classe de mensagem da mensagem para **OnActivateNext**. 
  
Notificações por um objeto de formulário para o aplicativo cliente são tratadas pela interface de **IMAPIViewAdviseSink** do aplicativo cliente. Para obter mais informações, consulte [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).
  

