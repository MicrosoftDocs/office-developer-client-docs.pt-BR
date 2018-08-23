---
title: Tratamento de erros de propriedade MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23d68d8b-b0b6-4c32-8404-6acd23802db0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 82f37e2a6f6834c7a8553a3d9d364f7e657d81da
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579505"
---
# <a name="handling-mapi-property-errors"></a><span data-ttu-id="5afc6-103">Tratamento de erros de propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="5afc6-103">Handling MAPI property errors</span></span>

<span data-ttu-id="5afc6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5afc6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5afc6-105">Em vez de falha completa ou sucesso, os seguintes m�todos de **IMAPIProp** relatar �xito parcial:</span><span class="sxs-lookup"><span data-stu-id="5afc6-105">Instead of complete failure or success, the following **IMAPIProp** methods report partial success:</span></span> 
  
[<span data-ttu-id="5afc6-106">GetProps</span><span class="sxs-lookup"><span data-stu-id="5afc6-106">GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="5afc6-107">SetProps</span><span class="sxs-lookup"><span data-stu-id="5afc6-107">SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="5afc6-108">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="5afc6-108">DeleteProps</span></span>](imapiprop-deleteprops.md)
  
[<span data-ttu-id="5afc6-109">CopyTo</span><span class="sxs-lookup"><span data-stu-id="5afc6-109">CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="5afc6-110">CopyProps</span><span class="sxs-lookup"><span data-stu-id="5afc6-110">CopyProps</span></span>](imapiprop-copyprops.md)
  
<span data-ttu-id="5afc6-p101">**GetProps** relat�rios sucesso parcial quando ele pode recuperar pelo menos uma das propriedades solicitadas para um objeto. **GetProps** indica �xito parcial, retornando o aviso MAPI_W_ERRORS_RETURNED e colocando informa��es sobre as propriedades n�o est� dispon�veis da matriz de valores de propriedade apontado pelo par�metro **lppPropArray**. Entrada de uma propriedade n�o est� dispon�vel nessa matriz cont�m PT_ERROR para o tipo de propriedade no membro do **ulPropTag** e E_NOT_FOUND ou outro valor de erro apropriado para o membro **Value**. Por exemplo, se um cliente chama o m�todo de **GetProps** de uma pasta para recuperar tr�s propriedades e a terceira n�o estiver dispon�vel, o provedor de armazenamento de mensagem coloca PT_ERROR no terceiro tipo de propriedade da matriz de valores de propriedade e E_NOT_FOUND no valor da propriedade terceiro.</span><span class="sxs-lookup"><span data-stu-id="5afc6-p101">**GetProps** reports partial success when it can retrieve at least one of the requested properties for an object. **GetProps** indicates partial success by returning the warning MAPI_W_ERRORS_RETURNED and placing information about the unavailable properties in the property value array pointed to by the **lppPropArray** parameter. An unavailable property's entry in this array contains PT_ERROR for the property type in the **ulPropTag** member and MAPI_E_NOT_FOUND or another appropriate error value for the **Value** member. For example, if a client calls a folder's **GetProps** method to retrieve three properties and the third is unavailable, the message store provider places PT_ERROR in the third property type in the property value array and MAPI_E_NOT_FOUND in the third property value.</span></span> 
  
<span data-ttu-id="5afc6-p102">Outros m�todos **IMAPIProp** relatar �xito parcial de forma diferente. Esses m�todos relatar �xito parcial, retornando S_OK e colocando informa��es de erro em uma estrutura [SPropProblemArray](spropproblemarray.md) . Ao contr�rio de matriz de valores de propriedade em **GetProps** que cont�m dados independentemente se o m�todo teve �xito ou falha, a matriz de problema da propriedade nesses m�todos existe somente se h� erros e somente se o chamador registrou interesse em saber mais sobre os erros. Os chamadores devem especificar um ponteiro v�lido **SPropProblemArray** para registrar para obter informa��es de erro.</span><span class="sxs-lookup"><span data-stu-id="5afc6-p102">The other **IMAPIProp** methods report partial success differently. These methods report partial success by returning S_OK and placing error information in an [SPropProblemArray](spropproblemarray.md) structure. Unlike the property value array in **GetProps** that contains data regardless of whether the method succeeded or failed, the property problem array in these methods exists only if there are errors and only if the caller has registered interest in learning about the errors. Callers must specify a valid **SPropProblemArray** pointer to register for error information.</span></span> 
  
<span data-ttu-id="5afc6-p103">Quando um valor de erro � retornado de **SetProps**, **DeleteProps**, **CopyTo**ou **CopyProps**, isto indica falha em vez de sucesso parcial. A matriz de problema de propriedade, se estiver dispon�vel, n�o � v�lida. Os clientes n�o devem tentar acessar dados mantidos na estrutura nem deve tentar liberar a estrutura em si. A resposta apropriada � chamar [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="5afc6-p103">When an error value is returned from **SetProps**, **DeleteProps**, **CopyTo**, or **CopyProps**, this indicates failure instead of partial success. The property problem array, if available, is not valid. Clients should not try to access data held in the structure nor should they try to free the structure itself. The appropriate response is to call [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span> 
  
<span data-ttu-id="5afc6-p104">**GetLastError** � semelhante � fun��o do mesmo nome fornecido no SDK do Windows. Ambos fornecem que informa��es mais detalhadas sobre um erro que est� dispon�vel com o valor de retorno. Ambos retornarem informa��es sobre o erro anterior que tenha ocorrido. A diferen�a � que a fun��o de **GetLastError** Win32 relat�rios sobre um erro gerado pelo thread de chamada e o m�todo **IMAPIProp::GetLastError** relat�rios sobre um erro gerado pelo objeto atual. Ou seja, se um cliente chama **DeleteProps** em uma mensagem e MAPI_E_NO_ACCESS � retornado para indicar que a mensagem � somente leitura, **GetLastError** retorna dados fornecidos pela mensagem.</span><span class="sxs-lookup"><span data-stu-id="5afc6-p104">**GetLastError** is similar to the function of the same name provided in the Windows SDK. Both provide more detailed information about an error than is available with the return value. They both return information about the previous error that has occurred. The difference is that the Win32 **GetLastError** function reports on an error generated by the calling thread and the **IMAPIProp::GetLastError** method reports on an error generated by the current object. That is, if a client calls **DeleteProps** on a message and MAPI_E_NO_ACCESS is returned to indicate that the message is read-only, **GetLastError** returns data provided by the message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5afc6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5afc6-128">See also</span></span>

- [<span data-ttu-id="5afc6-129">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="5afc6-129">MAPI Property Overview</span></span>](mapi-property-overview.md)

