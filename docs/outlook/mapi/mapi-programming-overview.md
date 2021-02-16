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
  
Esta Referência da API de Mensagens do Microsoft Outlook (MAPI) foi escrita para desenvolvedores C e C++ com uma variedade de necessidades e experiência com mensagens. Para os desenvolvedores que querem usar MAPI para aumentar seus aplicativos que têm recursos de mensagens, nenhum conhecimento de pré-requisito específico é necessário. Você precisa de um plano de fundo nas mensagens e no COM (Component Object Model) para usar o MAPI para criar aplicativos ou drivers de grupo de trabalho em escala completa para serviços especializados do sistema de mensagens.
  
Antes de iniciar o trabalho de desenvolvimento, você deve considerar as seguintes informações sobre como usar o MAPI, o processo de logon e como perfis e serviços de mensagens são criados e configurados.
  
O MAPI (Messaging Application Program Interface) é um amplo conjunto de funções que os desenvolvedores podem usar para criar aplicativos habilitados para email. A biblioteca de funções completa é conhecida como MAPI. MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.
  
> [!NOTE]
> MAPI estendido é o mesmo que MAPI e é simplesmente chamado de MAPI na documentação MAPI. 
  
 **Simple MAPI**
  
Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.
  
> [!IMPORTANT]
> A função MAPISendMail simples é suportada pelo Microsoft Outlook 2013 e Microsoft Outlook 2010. Outras funções MAPI simples foram preteridas no Windows. 
  

