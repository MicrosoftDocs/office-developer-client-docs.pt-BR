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
# <a name="mapi-programming-overview"></a><span data-ttu-id="65186-103">Visão geral da programação MAPI</span><span class="sxs-lookup"><span data-stu-id="65186-103">MAPI Programming Overview</span></span>

  
  
<span data-ttu-id="65186-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65186-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65186-105">Esta referência da API de mensagens do Microsoft Outlook (MAPI) é escrita para desenvolvedores C e C++ com uma variedade de necessidades e experiência com mensagens.</span><span class="sxs-lookup"><span data-stu-id="65186-105">This Microsoft Outlook Messaging API (MAPI) Reference is written for C and C++ developers with a variety of needs and experience with messaging.</span></span> <span data-ttu-id="65186-106">Para os desenvolvedores que desejam usar o MAPI para ampliar seus aplicativos que têm recursos de mensagens, nenhum conhecimento específico de pré-requisito é necessário.</span><span class="sxs-lookup"><span data-stu-id="65186-106">For those developers who want to use MAPI to augment their applications that have messaging features, no specific prerequisite knowledge is required.</span></span> <span data-ttu-id="65186-107">Você precisa de um plano de fundo no sistema de mensagens e do COM (Component Object Model) para usar o MAPI para criar aplicativos ou drivers de grupo de trabalho de escala total para serviços especializados do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="65186-107">You need a background in messaging and the Component Object Model (COM) to use MAPI to create full-scale workgroup applications or drivers for specialized messaging system services.</span></span>
  
<span data-ttu-id="65186-108">Antes de iniciar o trabalho de desenvolvimento, considere as seguintes informações sobre como usar o MAPI, o processo de logon e como os perfis e os serviços de mensagens são criados e configurados.</span><span class="sxs-lookup"><span data-stu-id="65186-108">Before starting development work, you should consider the following information about how to use MAPI, the logon process, and how profiles and message services are created and configured.</span></span>
  
<span data-ttu-id="65186-109">O MAPI (Messaging Application Program interface) é um conjunto abrangente de funções que os desenvolvedores podem usar para criar aplicativos habilitados para email.</span><span class="sxs-lookup"><span data-stu-id="65186-109">The Messaging Application Program Interface (MAPI) is an extensive set of functions that developers can use to create mail-enabled applications.</span></span> <span data-ttu-id="65186-110">A biblioteca de funções completa é conhecida como MAPI.</span><span class="sxs-lookup"><span data-stu-id="65186-110">The full function library is known as MAPI.</span></span> <span data-ttu-id="65186-111">O MAPI permite o controle completo sobre o sistema de mensagens no computador cliente, a criação e o gerenciamento de mensagens, o gerenciamento da caixa de correio do cliente, dos provedores de serviços e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="65186-111">MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.</span></span>
  
> [!NOTE]
> <span data-ttu-id="65186-112">MAPI estendido é o mesmo que MAPI e é simplesmente chamado de MAPI na documentação MAPI.</span><span class="sxs-lookup"><span data-stu-id="65186-112">Extended MAPI is the same as MAPI, and is simply referred to as MAPI in the MAPI documentation.</span></span> 
  
 <span data-ttu-id="65186-113">**Simple MAPI**</span><span class="sxs-lookup"><span data-stu-id="65186-113">**Simple MAPI**</span></span>
  
<span data-ttu-id="65186-114">O Simple MAPI fornece um conjunto de funções que permite adicionar um nível básico de funcionalidade de mensagens a aplicativos baseados no Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="65186-114">Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="65186-115">A função Simple MAPI MAPISendMail é suportada pelo Microsoft Outlook 2013 e pelo Microsoft Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="65186-115">The Simple MAPI function MAPISendMail is supported by Microsoft Outlook 2013 and Microsoft Outlook 2010.</span></span> <span data-ttu-id="65186-116">Outras funções do Simple MAPI foram preteridas no Windows.</span><span class="sxs-lookup"><span data-stu-id="65186-116">Other Simple MAPI functions have been deprecated in Windows.</span></span> 
  

