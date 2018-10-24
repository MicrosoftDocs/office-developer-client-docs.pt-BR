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
ms.openlocfilehash: 9ee41469914e52295af219428f26854662c9e2f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582242"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="62cf5-103">Suporte a propriedades nomeadas</span><span class="sxs-lookup"><span data-stu-id="62cf5-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="62cf5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62cf5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62cf5-105">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties.</span><span class="sxs-lookup"><span data-stu-id="62cf5-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="62cf5-106">Suporte a propriedades nomeadas é necessário para:</span><span class="sxs-lookup"><span data-stu-id="62cf5-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="62cf5-107">Provedores de catálogo de endereços que permitem entradas de outros provedores a serem copiados para seus contêineres.</span><span class="sxs-lookup"><span data-stu-id="62cf5-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="62cf5-108">Provedores que podem ser usados para criar tipos de mensagem arbitrário de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="62cf5-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="62cf5-109">Propriedade nomeada suporte é opcional para todos os outros provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="62cf5-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="62cf5-110">Provedores de serviço que oferecem suporte a propriedades nomeadas devem implementar o mapeamento de nome-para-identifier os métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="62cf5-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="62cf5-111">Clientes chamadas **GetNamesFromIDs** para recuperar os nomes correspondentes para um ou mais identificadores de propriedade no intervalo 0x8000 failover e **GetIDsFromNames** criar ou recuperar os identificadores para um ou mais nomes.</span><span class="sxs-lookup"><span data-stu-id="62cf5-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="62cf5-112">Provedores de serviços que não oferecem suporte a propriedades nomeadas devem:</span><span class="sxs-lookup"><span data-stu-id="62cf5-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="62cf5-113">Transferir chamadas para [IMAPIProp::SetProps](imapiprop-setprops.md) para definir propriedades com identificadores de 0x8000 ou maior, retornando MAPI_E_UNEXPECTED_ID na matriz [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="62cf5-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="62cf5-114">Retorne MAPI_E_NO_SUPPORT dos métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="62cf5-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    

