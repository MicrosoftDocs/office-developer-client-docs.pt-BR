---
title: Manipular erros de propriedade nomeados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f6c12973a3ee2f9842e74f6f01b94553659dc1ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583306"
---
# <a name="handling-named-property-errors"></a><span data-ttu-id="90e36-103">Manipular erros de propriedade nomeados</span><span class="sxs-lookup"><span data-stu-id="90e36-103">Handling named property errors</span></span>
  
<span data-ttu-id="90e36-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90e36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90e36-p101">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop.</span><span class="sxs-lookup"><span data-stu-id="90e36-p101">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop.</span></span> 
  
<span data-ttu-id="90e36-107">Quando uma chamada como resultado sucesso parcial, como quando a solicita��o � para nomes que mapeiam aos identificadores espec�ficos e um ou mais nomes n�o for encontrado, **GetNamesFromIDs** retorna MAPI_W_ERRORS_RETURNED e coloca PT_ERROR no tipo de propriedade para a propriedade ausente na matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="90e36-107">When a call results in partial success, such as when the request is for names that map to specific identifiers and one or more names cannot be found, **GetNamesFromIDs** returns MAPI_W_ERRORS_RETURNED and places PT_ERROR in the property type for the missing property in the property tag array.</span></span> 
  
<span data-ttu-id="90e36-p102">Em alguns casos, um cliente faz uma chamada para **GetNamesFromIDs** que resulte em nenhuma propriedades sendo retornadas, como quando n�o h� nenhuma propriedade em um conjunto de propriedades especificado, ou quando todas as propriedades nomeadas s�o de um tipo exclu�do com os sinalizadores. Os clientes podem esperar provedores de servi�os:</span><span class="sxs-lookup"><span data-stu-id="90e36-p102">Sometimes a client makes a call to **GetNamesFromIDs** that results in no properties being returned, such as when there are no properties in a specified property set, or when all named properties are of a type excluded by the flags. Clients can expect service providers to:</span></span> 
  
- <span data-ttu-id="90e36-110">Retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="90e36-110">Return S_OK.</span></span>
    
- <span data-ttu-id="90e36-111">Defina o conte�do do ponteiro de matriz a propriedade tag para uma matriz de marca de propriedade alocadas recentemente com sua lista de membros **cValues** definida como zero.</span><span class="sxs-lookup"><span data-stu-id="90e36-111">Set the contents of the property tag array pointer to a newly allocated property tag array with its **cValues** member set to zero.</span></span> 
    
- <span data-ttu-id="90e36-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span><span class="sxs-lookup"><span data-stu-id="90e36-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span></span> 
    
- <span data-ttu-id="90e36-113">Defina o conte�do da contagem de estruturas de **MAPINAMEID** como zero.</span><span class="sxs-lookup"><span data-stu-id="90e36-113">Set the contents of the count of **MAPINAMEID** structures to zero.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="90e36-114">Ver tamb�m</span><span class="sxs-lookup"><span data-stu-id="90e36-114">See also</span></span>

- [<span data-ttu-id="90e36-115">MAPI denominada propriedades</span><span class="sxs-lookup"><span data-stu-id="90e36-115">MAPI Named Properties</span></span>](mapi-named-properties.md)

