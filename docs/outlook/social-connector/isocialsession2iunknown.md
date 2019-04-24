---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: O suporta a adição de amigos, a sincronização por demanda ou híbrida de amigos, a sincronização sob demanda de atividades ou o logon na rede social usando credenciais armazenadas em cache.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345294"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="914c6-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="914c6-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="914c6-104">O suporta a adição de amigos, a sincronização por demanda ou híbrida de amigos, a sincronização sob demanda de atividades ou o logon na rede social usando credenciais armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="914c6-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="914c6-105">Members</span><span class="sxs-lookup"><span data-stu-id="914c6-105">Members</span></span>

<span data-ttu-id="914c6-106">A tabela a seguir mostra os membros que estão disponíveis na interface **ISocialSession2** .</span><span class="sxs-lookup"><span data-stu-id="914c6-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="914c6-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="914c6-107">**Name**</span></span>|<span data-ttu-id="914c6-108">**Tipo de membro**</span><span class="sxs-lookup"><span data-stu-id="914c6-108">**Member type**</span></span>|<span data-ttu-id="914c6-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="914c6-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="914c6-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="914c6-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="914c6-111">Método		</span><span class="sxs-lookup"><span data-stu-id="914c6-111">Method</span></span>  <br/> |<span data-ttu-id="914c6-112">Adiciona a pessoa identificada pelos __ parâmetros EmailAddresses e _DisplayName_ como um amigo para o usuário conectado na rede social.</span><span class="sxs-lookup"><span data-stu-id="914c6-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="914c6-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="914c6-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="914c6-114">Método		</span><span class="sxs-lookup"><span data-stu-id="914c6-114">Method</span></span>  <br/> |<span data-ttu-id="914c6-115">Obtém uma cadeia de caracteres que representa uma coleção de atividades dos usuários especificados pelo parâmetro _hashedAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="914c6-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="914c6-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="914c6-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="914c6-117">Método		</span><span class="sxs-lookup"><span data-stu-id="914c6-117">Method</span></span>  <br/> |<span data-ttu-id="914c6-118">Retorna uma cadeia de caracteres que contém uma coleção de detalhes de pessoa e imagem para os usuários especificados pelo parâmetro _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="914c6-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="914c6-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="914c6-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="914c6-120">Método		</span><span class="sxs-lookup"><span data-stu-id="914c6-120">Method</span></span>  <br/> |<span data-ttu-id="914c6-121">Faz logon no site de rede social usando credenciais armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="914c6-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="914c6-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="914c6-122">Remarks</span></span>

<span data-ttu-id="914c6-123">Um provedor do Outlook Social Connector (OSC) pode optar por implementar essa interface se o provedor oferecer suporte à sincronização por demanda ou híbrida de amigos, à sincronização sob demanda de atividades ou ao fazer logon na rede social usando credenciais armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="914c6-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="914c6-124">Se o provedor do OSC implementar o **ISocialSession2** e suportar as seguintes pessoas na rede social, o OSC chamaria [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) em vez de [ISocialSession:: FollowPerson](isocialsession-followperson.md)e o provedor deve implementar **ISocialSession2:: FollowPersonEx**também.</span><span class="sxs-lookup"><span data-stu-id="914c6-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="914c6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="914c6-125">See also</span></span>

- [<span data-ttu-id="914c6-126">Interfaces do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="914c6-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

