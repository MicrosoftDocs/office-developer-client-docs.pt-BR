---
title: Visão geral da programação MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: d69d15f0f635c81bea30401b3a6d6e3ccf620112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408338"
---
# <a name="mapi-programming-overview"></a>Visão geral da programação MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Esta referência da API de mensagens do Microsoft Outlook (MAPI) é escrita para desenvolvedores C e C++ com uma variedade de necessidades e experiência com mensagens. Para os desenvolvedores que desejam usar o MAPI para ampliar seus aplicativos que têm recursos de mensagens, nenhum conhecimento específico de pré-requisito é necessário. Você precisa de um plano de fundo no sistema de mensagens e do COM (Component Object Model) para usar o MAPI para criar aplicativos ou drivers de grupo de trabalho de escala total para serviços especializados do sistema de mensagens.
  
Antes de iniciar o trabalho de desenvolvimento, considere as seguintes informações sobre como usar o MAPI, o processo de logon e como os perfis e os serviços de mensagens são criados e configurados.
  
O MAPI (Messaging Application Program interface) é um conjunto abrangente de funções que os desenvolvedores podem usar para criar aplicativos habilitados para email. A biblioteca de funções completa é conhecida como MAPI. O MAPI permite o controle completo sobre o sistema de mensagens no computador cliente, a criação e o gerenciamento de mensagens, o gerenciamento da caixa de correio do cliente, dos provedores de serviços e assim por diante.
  
> [!NOTE]
> MAPI estendido é o mesmo que MAPI e é simplesmente chamado de MAPI na documentação MAPI. 
  
 **Simple MAPI**
  
O Simple MAPI fornece um conjunto de funções que permite adicionar um nível básico de funcionalidade de mensagens a aplicativos baseados no Microsoft Windows.
  
> [!IMPORTANT]
> A função Simple MAPI MAPISendMail é suportada pelo Microsoft Outlook 2013 e pelo Microsoft Outlook 2010. Outras funções do Simple MAPI foram preteridas no Windows. 
  

