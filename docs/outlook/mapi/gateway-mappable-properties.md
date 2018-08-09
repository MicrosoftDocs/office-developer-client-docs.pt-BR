---
title: Propriedades podem ser mapeadas de gateway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b637f4921165d70ddeda914b4299c35aabe8218f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766636"
---
# <a name="gateway-mappable-properties"></a><span data-ttu-id="5a41d-103">Propriedades podem ser mapeadas de gateway</span><span class="sxs-lookup"><span data-stu-id="5a41d-103">Gateway mappable properties</span></span>

<span data-ttu-id="5a41d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a41d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a41d-105">Propriedades podem ser mapeados Gateway são propriedades que podem exigir a conversão quando enviada de um domínio de mensagens para outro.</span><span class="sxs-lookup"><span data-stu-id="5a41d-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="5a41d-106">Propriedades podem ser mapeados gateway do MAPI habilitar as mensagens incluir informações que requer um gateway para garantir que o sistema de mensagens de destino utiliza adequadamente.</span><span class="sxs-lookup"><span data-stu-id="5a41d-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="5a41d-107">Embora os desenvolvedores de gateway não são necessários para fornecer esse recurso de conversão, eles devem considerar propriedades podem ser mapeados gateway como uma oportunidade para aperfeiçoar o tratamento do conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="5a41d-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="5a41d-108">MAPI Especifica cinco tipos de propriedades podem ser mapeados gateway:</span><span class="sxs-lookup"><span data-stu-id="5a41d-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="5a41d-109">Nome para exibição</span><span class="sxs-lookup"><span data-stu-id="5a41d-109">Display name</span></span>
    
- <span data-ttu-id="5a41d-110">Endereço de email</span><span class="sxs-lookup"><span data-stu-id="5a41d-110">Email address</span></span>
    
- <span data-ttu-id="5a41d-111">Tipo de email</span><span class="sxs-lookup"><span data-stu-id="5a41d-111">Email type</span></span>
    
- <span data-ttu-id="5a41d-112">Identificador de entrada</span><span class="sxs-lookup"><span data-stu-id="5a41d-112">Entry identifier</span></span>
    
- <span data-ttu-id="5a41d-113">Chave de pesquisa</span><span class="sxs-lookup"><span data-stu-id="5a41d-113">Search key</span></span>
    
<span data-ttu-id="5a41d-114">Este é o conjunto de propriedades que estão associadas a destinatários, remetentes confiáveis, destinatários de relatório e delegados remetentes e destinatários de endereçamento.</span><span class="sxs-lookup"><span data-stu-id="5a41d-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="5a41d-115">Para ajudar o seu cliente definir essas propriedades para que um gateway manipula especialmente, MAPI Especifica uma convenção de nomenclatura usando propriedades nomeadas e conjuntos de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5a41d-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="5a41d-116">Cinco conjuntos de propriedade existirem para armazenar propriedades nomeadas, as propriedades de endereçamento que exigem o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="5a41d-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="5a41d-117">Não há uma propriedade definida para cada tipo de propriedade podem ser mapeado.</span><span class="sxs-lookup"><span data-stu-id="5a41d-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="5a41d-118">Os conjuntos de propriedades que irá manter essas propriedades endereçamento nomeadas são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="5a41d-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="5a41d-119">**Conjunto de propriedades**</span><span class="sxs-lookup"><span data-stu-id="5a41d-119">**Property set**</span></span>|<span data-ttu-id="5a41d-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5a41d-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5a41d-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="5a41d-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="5a41d-122">Contém propriedades de cadeia de caracteres usadas como nomes de exibição.</span><span class="sxs-lookup"><span data-stu-id="5a41d-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="5a41d-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="5a41d-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="5a41d-124">Contém propriedades de cadeia de caracteres usadas como endereços de email.</span><span class="sxs-lookup"><span data-stu-id="5a41d-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="5a41d-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="5a41d-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="5a41d-126">Contém propriedades de cadeia de caracteres usadas como tipos de endereço de email.</span><span class="sxs-lookup"><span data-stu-id="5a41d-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="5a41d-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5a41d-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="5a41d-128">Contém propriedades binárias usadas como identificadores de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="5a41d-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="5a41d-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="5a41d-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="5a41d-130">Contém propriedades binárias usadas como chaves de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5a41d-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

