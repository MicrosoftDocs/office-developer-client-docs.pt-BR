---
title: Suporte a propriedades nomeadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 983cbaf4d3523bf1e5370e5ad3119ab8c1490f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770540"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="0cdb0-103">Suporte a propriedades nomeadas</span><span class="sxs-lookup"><span data-stu-id="0cdb0-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="0cdb0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0cdb0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0cdb0-105">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties.</span><span class="sxs-lookup"><span data-stu-id="0cdb0-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="0cdb0-106">Suporte a propriedades nomeadas é necessário para:</span><span class="sxs-lookup"><span data-stu-id="0cdb0-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="0cdb0-107">Provedores de catálogo de endereços que permitem entradas de outros provedores a serem copiados para seus contêineres.</span><span class="sxs-lookup"><span data-stu-id="0cdb0-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="0cdb0-108">Provedores que podem ser usados para criar tipos de mensagem arbitrário de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0cdb0-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="0cdb0-109">Propriedade nomeada suporte é opcional para todos os outros provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="0cdb0-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="0cdb0-110">Provedores de serviço que oferecem suporte a propriedades nomeadas devem implementar o mapeamento de nome-para-identifier os métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="0cdb0-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="0cdb0-111">Clientes chamadas **GetNamesFromIDs** para recuperar os nomes correspondentes para um ou mais identificadores de propriedade no intervalo 0x8000 failover e **GetIDsFromNames** criar ou recuperar os identificadores para um ou mais nomes.</span><span class="sxs-lookup"><span data-stu-id="0cdb0-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="0cdb0-112">Provedores de serviços que não oferecem suporte a propriedades nomeadas devem:</span><span class="sxs-lookup"><span data-stu-id="0cdb0-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="0cdb0-113">Transferir chamadas para [IMAPIProp::SetProps](imapiprop-setprops.md) para definir propriedades com identificadores de 0x8000 ou maior, retornando MAPI_E_UNEXPECTED_ID na matriz [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="0cdb0-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="0cdb0-114">Retorne MAPI_E_NO_SUPPORT dos métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="0cdb0-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    

