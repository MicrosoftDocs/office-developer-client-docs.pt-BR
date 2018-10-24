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
ms.openlocfilehash: dbc56b7334d3966696641a84f23a64ce3802e3e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595269"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="f023a-103">Visão geral do provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="f023a-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="f023a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f023a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f023a-105">Um provedor de transporte é uma biblioteca de vínculo dinâmico (DLL) que atua como um intermediário entre um ou mais sistemas de mensagens subjacentes e o subsistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f023a-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="f023a-106">Um sistema de mensagens é algum mecanismo específico pelo qual as mensagens são enviadas e recebidas.</span><span class="sxs-lookup"><span data-stu-id="f023a-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="f023a-107">Alguns exemplos de sistemas de mensagens são:</span><span class="sxs-lookup"><span data-stu-id="f023a-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="f023a-108">Um sistema de arquivos de rede compartilhado que o provedor de transporte grava as mensagens diretamente.</span><span class="sxs-lookup"><span data-stu-id="f023a-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="f023a-109">Uma interface de rede TCP/IP que o provedor de transporte usa para se conectar a um servidor de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f023a-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="f023a-110">Um serviço online que os usuários se conectam ao.</span><span class="sxs-lookup"><span data-stu-id="f023a-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="f023a-111">Um baseado em host mensagens ou office automation sistema.</span><span class="sxs-lookup"><span data-stu-id="f023a-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="f023a-112">Um conjunto de chamadas de procedimento remoto para um servidor de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f023a-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="f023a-113">Qualquer coisa que pode ser usado para transferir dados de um computador para outro.</span><span class="sxs-lookup"><span data-stu-id="f023a-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="f023a-114">Um provedor de transporte DLL deve estar de acordo com a interface especificada por MAPI.</span><span class="sxs-lookup"><span data-stu-id="f023a-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="f023a-115">Como um desenvolvedor de provedor de transporte, você implementará essa interface em termos de funcionalidade presente no sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f023a-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  

