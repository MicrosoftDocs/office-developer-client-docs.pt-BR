---
title: Visão geral do provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356634"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="e1bf0-103">Visão geral do provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="e1bf0-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="e1bf0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1bf0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1bf0-105">Um provedor de transporte é uma biblioteca de vínculo dinâmico (DLL) que atua como um intermediário entre o subsistema MAPI e um ou mais sistemas de mensagens subjacentes.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="e1bf0-106">Um sistema de mensagens é um mecanismo específico pelo qual as mensagens são enviadas e recebidas.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="e1bf0-107">Alguns exemplos de sistemas de mensagens são:</span><span class="sxs-lookup"><span data-stu-id="e1bf0-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="e1bf0-108">Um sistema de arquivos de rede compartilhado no qual o provedor de transporte grava mensagens diretamente.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="e1bf0-109">Uma interface de rede TCP/IP que o provedor de transporte usa para se conectar a um servidor de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="e1bf0-110">Um serviço online ao qual os usuários se conectam.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="e1bf0-111">Um sistema de mensagens ou de automação do Office baseado em host.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="e1bf0-112">Um conjunto de chamadas de procedimento remoto para um servidor de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="e1bf0-113">Qualquer coisa que possa ser usada para transferir dados de um computador para outro.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="e1bf0-114">Uma DLL do provedor de transporte deve estar em conformidade com a interface especificada por MAPI.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="e1bf0-115">Como desenvolvedor de provedor de transporte, você implementará essa interface em termos da funcionalidade presente no sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  

