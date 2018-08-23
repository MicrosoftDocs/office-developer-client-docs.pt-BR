---
title: Vis�o geral da programa��o MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: bd9cdd9119f94e1f7684be34e1b4ef6fb40ab2bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576502"
---
# <a name="mapi-programming-overview"></a><span data-ttu-id="6f229-103">Vis�o geral da programa��o MAPI</span><span class="sxs-lookup"><span data-stu-id="6f229-103">MAPI Programming Overview</span></span>

  
  
<span data-ttu-id="6f229-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f229-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f229-105">Esta referência Microsoft Outlook Messaging API (MAPI) foi elaborada para C e com uma variedade de desenvolvedores do C++ precisa e experiência com mensagens.</span><span class="sxs-lookup"><span data-stu-id="6f229-105">This Microsoft Outlook Messaging API (MAPI) Reference is written for C and C++ developers with a variety of needs and experience with messaging.</span></span> <span data-ttu-id="6f229-106">Para os desenvolvedores que desejam usar MAPI para incrementar seus aplicativos que têm recursos de mensagens, nenhum conhecimento de pré-requisito específico é necessário.</span><span class="sxs-lookup"><span data-stu-id="6f229-106">For those developers who want to use MAPI to augment their applications that have messaging features, no specific prerequisite knowledge is required.</span></span> <span data-ttu-id="6f229-107">Você precisa de um plano de fundo em mensagens e o modelo COM (Component Object) usar MAPI para criar aplicativos de larga escala do grupo de trabalho ou drivers de serviços do sistema de mensagens especializados.</span><span class="sxs-lookup"><span data-stu-id="6f229-107">You need a background in messaging and the Component Object Model (COM) to use MAPI to create full-scale workgroup applications or drivers for specialized messaging system services.</span></span>
  
<span data-ttu-id="6f229-108">Antes de iniciar o trabalho de desenvolvimento, você deve considerar as seguintes informações sobre como usar o MAPI, o processo de logon e como perfis e serviços de mensagem sejam criados e configurados.</span><span class="sxs-lookup"><span data-stu-id="6f229-108">Before starting development work, you should consider the following information about how to use MAPI, the logon process, and how profiles and message services are created and configured.</span></span>
  
<span data-ttu-id="6f229-109">O programa Interface MAPI (Messaging Application) é um amplo conjunto de funções que os desenvolvedores podem usar para criar aplicativos habilitados para email.</span><span class="sxs-lookup"><span data-stu-id="6f229-109">The Messaging Application Program Interface (MAPI) is an extensive set of functions that developers can use to create mail-enabled applications.</span></span> <span data-ttu-id="6f229-110">A biblioteca de função completa é conhecida como MAPI.</span><span class="sxs-lookup"><span data-stu-id="6f229-110">The full function library is known as MAPI.</span></span> <span data-ttu-id="6f229-111">MAPI permite controle total sobre o sistema de mensagens no computador cliente, criação e gerenciamento de mensagens, gerenciamento da caixa de correio do cliente, provedores de serviços e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6f229-111">MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6f229-112">MAPI estendido é o mesmo MAPI e simplesmente é conhecido como MAPI na documentação de MAPI.</span><span class="sxs-lookup"><span data-stu-id="6f229-112">Extended MAPI is the same as MAPI, and is simply referred to as MAPI in the MAPI documentation.</span></span> 
  
 <span data-ttu-id="6f229-113">**MAPI simples**</span><span class="sxs-lookup"><span data-stu-id="6f229-113">**Simple MAPI**</span></span>
  
<span data-ttu-id="6f229-114">MAPI simples fornece um conjunto de funções que permite que você adicione um nível básico de funcionalidade aos aplicativos do Microsoft baseado no Windows de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6f229-114">Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6f229-115">A função de MAPI simples MAPISendMail é compatível com o Microsoft Outlook 2013 e o Microsoft Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="6f229-115">The Simple MAPI function MAPISendMail is supported by Microsoft Outlook 2013 and Microsoft Outlook 2010.</span></span> <span data-ttu-id="6f229-116">Outras funções de MAPI simples foram preteridas no Windows.</span><span class="sxs-lookup"><span data-stu-id="6f229-116">Other Simple MAPI functions have been deprecated in Windows.</span></span> 
  

