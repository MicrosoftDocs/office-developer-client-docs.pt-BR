---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Suporta a adição de amigos, a sincronização sob demanda ou híbrida de amigos, a sincronização sob demanda de atividades, ou de fazer logon na rede social usando credenciais armazenadas em cache.
ms.openlocfilehash: b14804d35e54ebe9fe2a529fb2664f0a661653bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770868"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="69535-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69535-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="69535-104">Suporta a adição de amigos, a sincronização sob demanda ou híbrida de amigos, a sincronização sob demanda de atividades, ou de fazer logon na rede social usando credenciais armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="69535-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="69535-105">Members</span><span class="sxs-lookup"><span data-stu-id="69535-105">Members</span></span>

<span data-ttu-id="69535-106">A tabela a seguir mostra os membros que estão disponíveis na interface **ISocialSession2** .</span><span class="sxs-lookup"><span data-stu-id="69535-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="69535-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="69535-107">**Name**</span></span>|<span data-ttu-id="69535-108">**Tipo de membro**</span><span class="sxs-lookup"><span data-stu-id="69535-108">**Member type**</span></span>|<span data-ttu-id="69535-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="69535-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="69535-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="69535-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="69535-111">Método</span><span class="sxs-lookup"><span data-stu-id="69535-111">Method</span></span>  <br/> |<span data-ttu-id="69535-112">Adiciona a pessoa identificada pelos parâmetros _emailAddresses_ e _displayName_ como um amigo para o usuário de logon na rede social.</span><span class="sxs-lookup"><span data-stu-id="69535-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="69535-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="69535-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="69535-114">Método</span><span class="sxs-lookup"><span data-stu-id="69535-114">Method</span></span>  <br/> |<span data-ttu-id="69535-115">Obtém um string que representa uma coleção de atividades dos usuários especificados pelo parâmetro _hashedAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="69535-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="69535-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="69535-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="69535-117">Método</span><span class="sxs-lookup"><span data-stu-id="69535-117">Method</span></span>  <br/> |<span data-ttu-id="69535-118">Retorna uma string que contém uma coleção de detalhes de imagem e a pessoa para os usuários especificados pelo parâmetro _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="69535-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="69535-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="69535-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="69535-120">Método</span><span class="sxs-lookup"><span data-stu-id="69535-120">Method</span></span>  <br/> |<span data-ttu-id="69535-121">Logs para o site de rede social usando credenciais armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="69535-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69535-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="69535-122">Remarks</span></span>

<span data-ttu-id="69535-123">Um provedor do Outlook Social Connector (OSC) pode optar por implementar essa interface, se o provedor oferece suporte a sincronização sob demanda ou híbrida de amigos, sincronização sob demanda de atividades, ou de fazer logon na rede social usando credenciais armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="69535-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="69535-124">Se o provedor do OSC implementa **ISocialSession2** e dá suporte às seguintes pessoas na rede social, o OSC chamaria [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) em vez de [ISocialSession::FollowPerson](isocialsession-followperson.md)e o provedor deve implementar **ISocialSession2::FollowPersonEx**, também.</span><span class="sxs-lookup"><span data-stu-id="69535-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="69535-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="69535-125">See also</span></span>

- [<span data-ttu-id="69535-126">Interfaces do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="69535-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

