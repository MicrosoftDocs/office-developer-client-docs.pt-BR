---
title: Propriedades mapeáveis do gateway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6f1a399cac2adbae66dabf9383540bb089424d17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430473"
---
# <a name="gateway-mappable-properties"></a><span data-ttu-id="e9438-103">Propriedades mapeáveis do gateway</span><span class="sxs-lookup"><span data-stu-id="e9438-103">Gateway mappable properties</span></span>

<span data-ttu-id="e9438-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9438-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9438-105">Propriedades mapeadas pelo gateway são propriedades que podem exigir tradução quando enviadas de um domínio de mensagens para outro.</span><span class="sxs-lookup"><span data-stu-id="e9438-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="e9438-106">As propriedades mapeadas pelo gateway MAPI permitem que as mensagens incluam informações que exijam um gateway para garantir que o sistema de mensagens de destino o use adequadamente.</span><span class="sxs-lookup"><span data-stu-id="e9438-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="e9438-107">Embora os desenvolvedores de gateway não precisem fornecer esse recurso de conversão, eles devem considerar as propriedades de mapeáveis de gateway como uma oportunidade de melhorar o tratamento do conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e9438-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="e9438-108">MAPI especifica cinco tipos de propriedades do gateway-mapeáveis:</span><span class="sxs-lookup"><span data-stu-id="e9438-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="e9438-109">Nome diferenciado (DN)</span><span class="sxs-lookup"><span data-stu-id="e9438-109">Display name</span></span>
    
- <span data-ttu-id="e9438-110">Nome para exibição</span><span class="sxs-lookup"><span data-stu-id="e9438-110">Email address</span></span>
    
- <span data-ttu-id="e9438-111">Tipo de email</span><span class="sxs-lookup"><span data-stu-id="e9438-111">Email type</span></span>
    
- <span data-ttu-id="e9438-112">Identificador de entrada</span><span class="sxs-lookup"><span data-stu-id="e9438-112">Entry identifier</span></span>
    
- <span data-ttu-id="e9438-113">Chave de pesquisa</span><span class="sxs-lookup"><span data-stu-id="e9438-113">Search key</span></span>
    
<span data-ttu-id="e9438-114">Este é o conjunto de propriedades de endereçamento que estão associadas a destinatários, remetentes, destinatários de relatórios e remetentes e destinatários delegados.</span><span class="sxs-lookup"><span data-stu-id="e9438-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="e9438-115">Para ajudar seu cliente a definir essas propriedades para que um gateway as manipule especialmente, MAPI especifica uma Convenção de nomenclatura usando propriedades nomeadas e conjuntos de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e9438-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="e9438-116">Cinco conjuntos de propriedades existem para reter propriedades nomeadas, as propriedades de endereçamento que exigem mapeamento.</span><span class="sxs-lookup"><span data-stu-id="e9438-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="e9438-117">Há um conjunto de propriedades para cada tipo de propriedade mapeável.</span><span class="sxs-lookup"><span data-stu-id="e9438-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="e9438-118">Os conjuntos de propriedades que armazenarão essas propriedades de endereçamento nomeadas são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="e9438-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="e9438-119">**Conjunto de propriedades**</span><span class="sxs-lookup"><span data-stu-id="e9438-119">**Property set**</span></span>|<span data-ttu-id="e9438-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e9438-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e9438-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="e9438-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="e9438-122">Contém propriedades de cadeia de caracteres usadas como nomes de exibição.</span><span class="sxs-lookup"><span data-stu-id="e9438-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="e9438-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="e9438-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="e9438-124">Contém propriedades de cadeia de caracteres usadas como endereços de email.</span><span class="sxs-lookup"><span data-stu-id="e9438-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="e9438-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="e9438-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="e9438-126">Contém propriedades de cadeia de caracteres usadas como tipos de endereço de email.</span><span class="sxs-lookup"><span data-stu-id="e9438-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="e9438-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e9438-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="e9438-128">Contém propriedades binárias usadas como identificadores de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="e9438-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="e9438-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="e9438-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="e9438-130">Contém propriedades binárias usadas como chaves de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e9438-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

