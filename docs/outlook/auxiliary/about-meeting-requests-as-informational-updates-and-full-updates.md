---
title: Sobre solicitações de reunião como atualizações informativas e atualizações completas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Uma solicitação de reunião é um email com IPM. Schedule.Meeting.Request como classe da mensagem. Por padrão, um participante recebe uma solicitação de reunião e responde a ela diretamente.
ms.openlocfilehash: 8e7ab7a85d3f9f7c0a67245b8d8ad27442f5c5e4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400128"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>Sobre solicitações de reunião como atualizações informativas e atualizações completas

Uma solicitação de reunião é um email com **IPM. Schedule.Meeting.Request** como classe da mensagem. Por padrão, um participante recebe uma solicitação de reunião e responde a ela diretamente. O Outlook dá suporte à configuração de representantes que podem responder a solicitações de reunião em nome do destinatário principal. De maneira programática, o Outlook configura a propriedade nomeada [PidLidMeetingType](https://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) de uma solicitação de reunião para identificar o status de atualização atual. 
  
## <a name="recipients-without-delegates"></a>Destinatários sem representantes

Quando o Outlook recebe uma nova solicitação de reunião, o Outlook configura a propriedade **PidLidMeetingType** da solicitação de reunião para **mtgRequest**. Qualquer atualização subsequente dessa reunião está em **mtgFullUpdate** (atualização completa) ou **mtgInfoUpdate** (atualização informativa), dependendo da causa da atualização, com a configuração do Outlook ** PidLidMeetingType** adequadamente. Uma atualização completa requer que um participante explicitamente responda à solicitação de reunião e uma atualização informativa não. 
  
## <a name="full-updates"></a>Atualizações completas

Há dois cenários que resultam em uma atualização completa:
  
- Quando um organizador muda data, hora, fuso horário ou recorrência de uma solicitação de reunião anterior, o organizador deve enviar uma atualização para os participantes. Essa atualização é uma atualização completa na qual um participante explicitamente deve responder para notificar ao organizador de participação, porque o Outlook ignora as respostas anterior.
    
- Se um participante não respondeu a uma solicitação inicial de reunião e receber uma atualização subsequente, a solicitação inicial de reunião fica desatualizada e a atualização se torna completa, independentemente da causa da atualização.
    
## <a name="informational-updates"></a>Atualizações informativas

Há quatro cenários em que o Outlook cria uma atualização informativa. Nesses cenários, responder à atualização informativa é opcional.
  
- Se um organizador mudar o local de uma solicitação anterior de reunião, ele deverá enviar uma atualização para os participantes. Se um participante já aceitou a solicitação inicial de reunião, ele receberá a atualização como uma atualização informativa.
    
- Se um organizador adicionar um participante à solicitação de reunião anterior, o organizador precisará enviar a solicitação de reunião para os participantes recém-adicionados e terá a opção de incluir os participantes existentes na atualização. O participante recém-adicionado receberá a solicitação de reunião como uma nova solicitação. Se o organizador optar por enviar uma atualização aos participantes existentes, os participantes receberão a atualização como uma atualização informativa.
    
- Se um organizador remover um participante de uma solicitação de reunião anterior, ele deverá enviar uma atualização para o participante que foi removido da solicitação de reunião e terá uma opção para incluir os participantes existentes na atualização. Os participantes receberão a atualização como uma atualização informativa.
    
- Se um organizador altera o assunto ou corpo de uma solicitação de reunião anterior, o organizador tem a opção de enviar uma atualização aos participantes ou salvar as alterações na cópia do organizador de solicitação de reunião. Se o organizador optar por enviar uma atualização, os participantes receberão a atualização como uma atualização informativa.
    
## <a name="recipients-set-up-with-delegates"></a>Configurar com representantes de destinatários

Destinatários que optam por configurar representantes podem ter representantes para responder às solicitações de reunião que não são marcadas como particular. Por padrão, a entidade de segurança recebe apenas uma cópia da solicitação de reunião ou uma cópia de uma atualização para uma solicitação de reunião anterior, e os representantes sempre recebem a solicitação de reunião original ou a atualização completa ou informativa original. Nessa configuração padrão, a entidade de segurança sempre recebe solicitações de reunião delegadas e atualizações; os representantes da entidade recebem solicitações de reunião como novas solicitações de reunião, atualizações completas ou atualizações informativas, conforme é descrito para os destinatários sem representantes na seção "Os destinatários sem representantes."
  
Por padrão, as entidades podem escolher responder a solicitações de reunião não particulares e atualizações, mesmo que os representantes estejam configurados para fazer isso em nome delas. No entanto, como alternativa, os administradores podem configurar uma política para impedir que os destinatários da entidade respondam.
  

