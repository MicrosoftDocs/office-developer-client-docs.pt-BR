---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Representa uma instância de um provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409955"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="be1e3-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be1e3-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="be1e3-104">Representa uma instância de um provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="be1e3-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="be1e3-105">Members</span><span class="sxs-lookup"><span data-stu-id="be1e3-105">Members</span></span>

<span data-ttu-id="be1e3-106">A tabela a seguir mostra os membros que estão disponíveis na interface **ISocialProvider.**</span><span class="sxs-lookup"><span data-stu-id="be1e3-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="be1e3-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="be1e3-107">**Name**</span></span>|<span data-ttu-id="be1e3-108">**Tipo de membro**</span><span class="sxs-lookup"><span data-stu-id="be1e3-108">**Member type**</span></span>|<span data-ttu-id="be1e3-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="be1e3-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be1e3-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="be1e3-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="be1e3-111">Propriedade</span><span class="sxs-lookup"><span data-stu-id="be1e3-111">Property</span></span>  <br/> |<span data-ttu-id="be1e3-112">Retorna uma matriz de cadeias de caracteres que especificam URLs de site para o provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="be1e3-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="be1e3-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="be1e3-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="be1e3-114">Method</span><span class="sxs-lookup"><span data-stu-id="be1e3-114">Method</span></span>  <br/> |<span data-ttu-id="be1e3-115">Obtém uma interface [ISocialSession](isocialsessioniunknown.md) configurada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="be1e3-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="be1e3-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="be1e3-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="be1e3-117">Method</span><span class="sxs-lookup"><span data-stu-id="be1e3-117">Method</span></span>  <br/> |<span data-ttu-id="be1e3-118">Obtém uma cadeia de caracteres que descreve os recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="be1e3-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="be1e3-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="be1e3-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="be1e3-120">Method</span><span class="sxs-lookup"><span data-stu-id="be1e3-120">Method</span></span>  <br/> |<span data-ttu-id="be1e3-121">Obtém uma interface [ISocialSession.](isocialsessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="be1e3-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="be1e3-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="be1e3-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="be1e3-123">Method</span><span class="sxs-lookup"><span data-stu-id="be1e3-123">Method</span></span>  <br/> |<span data-ttu-id="be1e3-124">No momento, não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="be1e3-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="be1e3-125">Load</span><span class="sxs-lookup"><span data-stu-id="be1e3-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="be1e3-126">Method</span><span class="sxs-lookup"><span data-stu-id="be1e3-126">Method</span></span>  <br/> |<span data-ttu-id="be1e3-127">Inicializa o provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="be1e3-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="be1e3-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="be1e3-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="be1e3-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="be1e3-129">Property</span></span>  <br/> |<span data-ttu-id="be1e3-130">Retorna um GUID que representa um identificador exclusivo para a rede social.</span><span class="sxs-lookup"><span data-stu-id="be1e3-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="be1e3-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="be1e3-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="be1e3-132">Propriedade</span><span class="sxs-lookup"><span data-stu-id="be1e3-132">Property</span></span>  <br/> |<span data-ttu-id="be1e3-133">Retorna uma matriz de bytes que representa o ícone da rede social.</span><span class="sxs-lookup"><span data-stu-id="be1e3-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="be1e3-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="be1e3-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="be1e3-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="be1e3-135">Property</span></span>  <br/> |<span data-ttu-id="be1e3-136">Retorna uma cadeia de caracteres que representa o nome da rede social.</span><span class="sxs-lookup"><span data-stu-id="be1e3-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="be1e3-137">Versão</span><span class="sxs-lookup"><span data-stu-id="be1e3-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="be1e3-138">Propriedade</span><span class="sxs-lookup"><span data-stu-id="be1e3-138">Property</span></span>  <br/> |<span data-ttu-id="be1e3-139">Retorna uma cadeia de caracteres que representa o número de versão do provedor para essa rede social.</span><span class="sxs-lookup"><span data-stu-id="be1e3-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be1e3-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="be1e3-140">Remarks</span></span>

<span data-ttu-id="be1e3-141">Um provedor OSC deve implementar essa interface para se comunicar com o OSC.</span><span class="sxs-lookup"><span data-stu-id="be1e3-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be1e3-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="be1e3-142">See also</span></span>

- [<span data-ttu-id="be1e3-143">Interfaces do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="be1e3-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

