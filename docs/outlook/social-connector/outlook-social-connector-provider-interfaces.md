---
title: Interfaces do provedor do Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) é um recurso do Office compartilhado por aplicativos cliente do Office que se conecta ao social e redes de negócios para que os usuários podem permanecer em contato com pessoas em suas redes sem sair do Office.
ms.openlocfilehash: bc393f32e563bbbef70538ea00cd92cf7f96729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770948"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="acdec-103">Interfaces do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="acdec-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="acdec-104">Outlook Social Connector (OSC) é um recurso do Office compartilhado por aplicativos cliente do Office que se conecta ao social e redes de negócios para que os usuários podem permanecer em contato com pessoas em suas redes sem sair do Office.</span><span class="sxs-lookup"><span data-stu-id="acdec-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="acdec-105">Um provedor OSC é um modelo COM (Component Object) DLL que permite que o OSC acessar dados de redes sociais de forma independente das APIs de cada rede social.</span><span class="sxs-lookup"><span data-stu-id="acdec-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="acdec-106">A tabela a seguir lista as interfaces na extensibilidade do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="acdec-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="acdec-107">Um provedor OSC deve implementar quatro das interfaces de cinco para se comunicar com o OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)e [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="acdec-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="acdec-108">Se o provedor do OSC oferece suporte à sincronização de atividades, sob demanda ou cache de sincronização de híbrido de amigos, cache de credenciais de logon e o logon usando credenciais ou a capacidade de acompanhar uma pessoa, o provedor deve implementar [ISocialSession2 ](isocialsession2iunknown.md), bem como.</span><span class="sxs-lookup"><span data-stu-id="acdec-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="acdec-109">**Nome**</span><span class="sxs-lookup"><span data-stu-id="acdec-109">**Name**</span></span>|<span data-ttu-id="acdec-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="acdec-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acdec-111">ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="acdec-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="acdec-112">Representa uma pessoa na rede social.</span><span class="sxs-lookup"><span data-stu-id="acdec-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="acdec-113">ISocialProfile</span><span class="sxs-lookup"><span data-stu-id="acdec-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="acdec-114">Representa o usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="acdec-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="acdec-115">ISocialProvider</span><span class="sxs-lookup"><span data-stu-id="acdec-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="acdec-116">Representa uma instância de um provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="acdec-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="acdec-117">ISocialSession</span><span class="sxs-lookup"><span data-stu-id="acdec-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="acdec-118">Representa uma conexão a um site de rede social.</span><span class="sxs-lookup"><span data-stu-id="acdec-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="acdec-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="acdec-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="acdec-120">Suporte à sincronização de atividades, adicionando amigos, sincronização sob demanda ou híbrida de amigos ou fazer logon na rede social usando credenciais armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="acdec-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   

