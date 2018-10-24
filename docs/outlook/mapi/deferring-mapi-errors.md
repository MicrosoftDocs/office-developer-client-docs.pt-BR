---
title: Adiar erros MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93ae6d54-41cd-433c-8124-eb07d71baa57
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3d2a46be04f235ba55aa5f2feef222ea7372b211
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569859"
---
# <a name="deferring-mapi-errors"></a><span data-ttu-id="46624-103">Adiar erros MAPI</span><span class="sxs-lookup"><span data-stu-id="46624-103">Deferring MAPI Errors</span></span>

  
  
<span data-ttu-id="46624-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46624-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46624-p101">Alguns m�todos de interface aceitam o sinalizador MAPI_DEFERRED_ERRORS como um par�metro de entrada. Quando esse sinalizador estiver definido, o m�todo n�o precisa retornar imediatamente com um valor; ele pode permitir que o chamador sabe o resultado da chamada em algum momento posterior.</span><span class="sxs-lookup"><span data-stu-id="46624-p101">Some interface methods accept the MAPI_DEFERRED_ERRORS flag as an input parameter. When this flag is set, the method does not have to return immediately with a value; it can let the caller know the result of the call at some later time.</span></span>
  
<span data-ttu-id="46624-p102">Adiar erros ajuda a provedores de servi�os em sua implementa��o dos m�todos complexas, tornando mais r�pido de processamento. Em vez de muitas solicita��es de manipula��o e retornar um valor para cada um, adiar erros permite que as chamadas para ser inclu�do no provedor de servi�o. Processando v�rias solicita��es de uma s� vez recorta no tr�fego de rede, melhorando o desempenho. Adiar erros � especialmente �til nas chamadas para excluir ou propriedades de c�pia, que podem ser muito demoradas opera��es.</span><span class="sxs-lookup"><span data-stu-id="46624-p102">Deferring errors helps service providers in their implementation of complex methods, making processing faster. Rather than handling many requests and returning a value for each, deferring errors allows the calls to be bundled within the service provider. Processing many requests at once cuts down on network traffic, thereby improving performance. Deferring errors is especially useful in calls to delete or copy properties, which can be very time-consuming operations.</span></span> 
  
<span data-ttu-id="46624-p103">Quando um cliente faz uma chamada sem definindo o sinalizador MAPI_DEFERRED_ERRORS que s� pode ser administrado de uma maneira adiada, provedores de servi�os podem adiar ou erros independentemente ou retornar MAPI_E_TOO_COMPLEX. A maioria dos clientes deve adiar erros como uma estrat�gia prefer�vel para falhando a chamada.</span><span class="sxs-lookup"><span data-stu-id="46624-p103">When a client makes a call without setting the MAPI_DEFERRED_ERRORS flag that can only be handled in a deferred manner, service providers can either defer the errors regardless or return MAPI_E_TOO_COMPLEX. Most clients should defer errors as a preferable strategy to failing the call.</span></span> 
  
<span data-ttu-id="46624-p104">Definindo o MAPI_DEFERRED_ERRORS sinalizador altera o tratamento de implementa��o em que as informa��es retornadas podem ser entregues a qualquer momento, em vez de cada vez planejada de erros de um cliente. � poss�vel que um erro a ser retornado quando for muito tarde fazer nada sobre ele ou depois de dados sobre a solicita��o original n�o est�o mais dispon�veis. Por exemplo, se um cliente chama **IMsgStore::OpenEntry** para abrir uma pasta exclu�da com MAPI_DEFERRED_ERRORS definido, o cliente n�o vai saber do problema at� que for feita uma chamada de **IMAPIProp::GetProps** para recuperar uma das propriedades da pasta. **GetProps** retornar� E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="46624-p104">Setting the MAPI_DEFERRED_ERRORS flag changes a client's error handling implementation in that the returned information can be delivered at any time rather than at a planned time. It is possible for an error to be returned when it is too late to do anything about it or after data about the original request is no longer available. For example, if a client calls **IMsgStore::OpenEntry** to open a deleted folder with MAPI_DEFERRED_ERRORS set, the client will not know of the problem until an **IMAPIProp::GetProps** call is made to retrieve one of the folder's properties. **GetProps** will then return MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46624-117">Ver tamb�m</span><span class="sxs-lookup"><span data-stu-id="46624-117">See also</span></span>



[<span data-ttu-id="46624-118">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="46624-118">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="46624-119">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="46624-119">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)

