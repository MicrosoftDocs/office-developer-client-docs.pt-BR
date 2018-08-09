---
title: Sobre solicitações de reunião como atualizações informativas e atualizações completas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Uma solicitação de reunião é um email que tenha IPM. Schedule.Meeting.Request como a classe de mensagem. Por padrão, um participante receber uma solicitação de reunião responde a ele diretamente.
ms.openlocfilehash: 3565b2af03ef79d70fc9f2817c64a788f031c416
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765791"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>Sobre solicitações de reunião como atualizações informativas e atualizações completas

Uma solicitação de reunião é um email que tenha **IPM. Schedule.Meeting.Request** como a classe de mensagem. Por padrão, um participante receber uma solicitação de reunião responde a ele diretamente. O Outlook suporta configurar representantes que podem responder às solicitações de reunião em nome do destinatário principal. Programaticamente, Outlook define a propriedade nomeada [PidLidMeetingType](http://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) de uma solicitação de reunião para identificar o status atual da atualização. 
  
## <a name="recipients-without-delegates"></a>Destinatários sem representantes

Quando o Outlook recebe uma nova solicitação de reunião, conjuntos de Outlook item da propriedade **PidLidMeetingType** da solicitação de reunião a **mtgRequest**. Qualquer atualização subsequente essa reunião é **mtgFullUpdate** (uma atualização completa) ou **mtgInfoUpdate** (uma atualização informativa), dependendo da causa da atualização, com o Outlook definindo **PidLidMeetingType** adequadamente. Uma atualização completa exige um participante à explicitamente responder à solicitação de reunião e não uma atualização informativa. 
  
## <a name="full-updates"></a>Atualizações completas

Há dois cenários que resultam em uma atualização completa:
  
- Quando um organizador altera a data, hora, fusos horários ou recorrência de uma solicitação de reunião anteriores, o organizador deve enviar uma atualização para todos os participantes. Essa atualização é uma atualização completa para o qual um participante explicitamente deve responder para notificar o organizador de presença, pois o Outlook ignora quaisquer respostas anteriores.
    
- Se um participante não respondeu a uma solicitação de reunião inicial e recebe uma atualização subsequente, a solicitação de reunião inicial fica desatualizada e a atualização é uma atualização completa, independentemente da causa da atualização.
    
## <a name="informational-updates"></a>Atualizações informativas

Existem quatro cenários nos quais o Outlook gera uma atualização informativa. Nesses cenários, responder a atualização informativos é opcional.
  
- Se um organizador altera o local de uma solicitação de reunião anteriores, o organizador deve enviar uma atualização para todos os participantes. Se um participante já aceita a solicitação de reunião inicial, o participante recebe a atualização como uma atualização informativa.
    
- Se um organizador adiciona um participante a uma solicitação de reunião anteriores, o organizador deve enviar a solicitação de reunião ao participante recém-adicionado e tem a opção para incluir participantes existentes na atualização. O nome do participante recém-adicionado recebe a solicitação de reunião como uma nova solicitação. Se o organizador optar por enviar uma atualização aos participantes existentes, os participantes recebem a atualização como uma atualização informativa.
    
- Se um organizador remove um participante de uma solicitação de reunião anteriores, o organizador deve enviar uma atualização para o participante que foi removido da solicitação de reunião e tem uma opção para incluir participantes existentes na atualização. Os participantes recebem a atualização como uma atualização informativa.
    
- Se um organizador mudar o assunto ou corpo de uma solicitação de reunião anteriores, o organizador tem a opção para enviar uma atualização para os participantes ou apenas salvar as alterações para a cópia do organizador da solicitação de reunião. Se o organizador optar por enviar uma atualização, os participantes recebem a atualização como uma atualização informativa.
    
## <a name="recipients-set-up-with-delegates"></a>Configurar destinatários com delegados

Destinatários que optar por configurar seus representantes podem ter representantes responder às solicitações de reunião que não são marcadas como particulares. Por padrão, a entidade recebe apenas uma cópia de uma solicitação de reunião ou uma cópia de uma atualização para uma solicitação de reunião anteriores e os representantes sempre recebem a solicitação de reunião original ou atualização completa ou informativa original. Nesta configuração padrão, a entidade sempre recebe solicitações de reunião delegada e atualizações; os representantes da entidade de segurança recebem solicitações de reunião como novas solicitações de reunião, atualizações completas ou informativas atualizações, conforme descrito para destinatários sem representantes na seção "Destinatários sem representantes".
  
Por padrão, o entidades podem optar por responder às solicitações de reunião não-particular e atualizações, mesmo que os delegados forem configurados para fazer isso em nome deles. No entanto, como alternativa, os administradores podem definir uma política para impedir que os destinatários principais respondendo.
  

