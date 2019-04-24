---
title: Suporte a propriedades nomeadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 27625e913f06e858295351ed62de840ae7789915
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349627"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="780e6-103">Suporte a propriedades nomeadas</span><span class="sxs-lookup"><span data-stu-id="780e6-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="780e6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="780e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="780e6-105">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties.</span><span class="sxs-lookup"><span data-stu-id="780e6-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="780e6-106">O suporte para propriedades nomeadas é necessário para:</span><span class="sxs-lookup"><span data-stu-id="780e6-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="780e6-107">Provedores de catálogo de endereços que permitem que entradas de outros provedores sejam copiadas em seus contêineres.</span><span class="sxs-lookup"><span data-stu-id="780e6-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="780e6-108">Provedores de repositórios de mensagens que podem ser usados para criar tipos de mensagem arbitrários.</span><span class="sxs-lookup"><span data-stu-id="780e6-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="780e6-109">O suporte à propriedade nomeada é opcional para todos os outros provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="780e6-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="780e6-110">Os provedores de serviços que dão suporte a propriedades nomeadas devem implementar o mapeamento de nome para identificador nos métodos [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="780e6-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="780e6-111">Os clientes chamam **GetNamesFromIDs** para recuperar os nomes correspondentes de um ou mais identificadores de propriedade no intervalo de mais de 0x8000 e o **GetIDsFromNames** para criar ou recuperar os identificadores de um ou mais nomes.</span><span class="sxs-lookup"><span data-stu-id="780e6-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="780e6-112">Os provedores de serviços que não dão suporte a propriedades nomeadas devem:</span><span class="sxs-lookup"><span data-stu-id="780e6-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="780e6-113">Falha em chamadas para [IMAPIProp::](imapiprop-setprops.md) SetProps para definir propriedades com identificadores de 0x8000 ou maior retornando MAPI_E_UNEXPECTED_ID na matriz [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="780e6-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="780e6-114">Retornar MAPI_E_NO_SUPPORT dos métodos [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="780e6-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    

