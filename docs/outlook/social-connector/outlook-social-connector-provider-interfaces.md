---
title: Interfaces do provedor do Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: 'O Outlook Social Connector (OCS) é um recurso do Office compartilhado pelos aplicativos cliente do Office que se conecta a redes empresariais e sociais para que usuários possam se manter em contato com as pessoas das suas redes sem sair do Office. '
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422807"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="b0b2e-103">Interfaces do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="b0b2e-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="b0b2e-104">O Outlook Social Connector (OCS) é um recurso do Office compartilhado pelos aplicativos cliente do Office que se conecta a redes empresariais e sociais para que usuários possam se manter em contato com as pessoas das suas redes sem sair do Office. </span><span class="sxs-lookup"><span data-stu-id="b0b2e-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="b0b2e-105">Um provedor de OSC é um Component Object Model (COM) DLL que permite o OSC acessar dados de redes sociais de forma independente das APIs de cada rede social.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="b0b2e-106">A tabela a seguir lista as interfaces na extensibilidade do provedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="b0b2e-107">Um provedor de OSC deve implementar quatro das cinco interfaces para se comunicar com o OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md) e [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="b0b2e-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="b0b2e-108">Se o provedor de OSC oferecer suporte a atividades de sincronização, sob demanda ou sincronização híbrida de amigos, armazenar credenciais de logon em cache e fazer logon usando credenciais em cache, ou a capacidade de seguir uma pessoa, o provedor deve também implementar [ISocialSession2](isocialsession2iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="b0b2e-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="b0b2e-109">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b0b2e-109">**Name**</span></span>|<span data-ttu-id="b0b2e-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b0b2e-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0b2e-111">ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="b0b2e-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="b0b2e-112">Representa uma pessoa nas redes sociais.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="b0b2e-113">ISocialProfile</span><span class="sxs-lookup"><span data-stu-id="b0b2e-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="b0b2e-114">Representa o usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="b0b2e-115">ISocialProvider</span><span class="sxs-lookup"><span data-stu-id="b0b2e-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="b0b2e-116">Representa uma instância de um provedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="b0b2e-117">ISocialSession</span><span class="sxs-lookup"><span data-stu-id="b0b2e-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="b0b2e-118">Representa uma conexão a um site de rede social.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="b0b2e-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="b0b2e-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="b0b2e-120">Oferece suporte a atividades de sincronização, adicionar amigos, sob demanda ou sincronização híbrida de amigos, ou fazer logon nas redes sociais usando credenciais em cache.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   

