---
title: Configurando a ordem de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433595"
---
# <a name="setting-transport-order"></a><span data-ttu-id="2afac-103">Configurando a ordem de transporte</span><span class="sxs-lookup"><span data-stu-id="2afac-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="2afac-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2afac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2afac-105">O spooler MAPI atribui responsabilidade por mensagens de saída com base nos tipos de endereço e identificadores que os provedores de transporte declaram que podem manipular.</span><span class="sxs-lookup"><span data-stu-id="2afac-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="2afac-106">Os provedores de transporte publicam uma lista de tipos de endereços e identificadores com suporte — armazenados em estruturas **MAPIUID** — quando o MAPI chama seu método [IXPLogon::AddressTypes,](ixplogon-addresstypes.md) diretamente após o logon.</span><span class="sxs-lookup"><span data-stu-id="2afac-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="2afac-107">O tipo de endereço de um destinatário é armazenado **em sua PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="2afac-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="2afac-108">O registro de um tipo de endereço indica ao MAPI que o provedor de transporte pode entregar aos destinatários com a propriedade **PR_ADDRTYPE** definida como o tipo de endereço registrado.</span><span class="sxs-lookup"><span data-stu-id="2afac-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="2afac-109">Da mesma forma, registrar-se para um **MAPIUID** indica que o provedor de transporte pode entregar aos destinatários representados por identificadores de entrada com **MAPIUID registrado.**</span><span class="sxs-lookup"><span data-stu-id="2afac-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="2afac-110">A maioria dos provedores de transporte se registra para um ou mais tipos de endereços; alguns se registram **por MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="2afac-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="2afac-111">Os provedores de transporte que estão fortemente unidos a um provedor de agendamento de endereços e entendem seu formato de identificador de entrada podem se registrar para manipular mensagens por **MAPIUID,** melhorando assim o desempenho.</span><span class="sxs-lookup"><span data-stu-id="2afac-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="2afac-112">Esses provedores de transporte fortemente aparados podem extrair o endereço de email do destinatário e outras informações necessárias do identificador de entrada sem precisar abri-lo com uma chamada **IMAPISupport::OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="2afac-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="2afac-113">MAPI mantém uma ordem para provedores de transporte, usado quando vários provedores de transporte foram registrados para o mesmo tipo de endereço ou **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="2afac-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="2afac-114">Você pode substituir essa ordem chamando [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) e passando uma lista ordenada de **MAPIUID** s de todos os provedores de transporte ativos apontados pelo parâmetro _lpUIDList.:_</span><span class="sxs-lookup"><span data-stu-id="2afac-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID** s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="2afac-115">Para recuperar uma lista de todos os tipos de endereços que podem ser manipulados por um dos provedores de transporte ativos, chame [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="2afac-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="2afac-116">**EnumAdrTypes** retorna uma matriz de cadeias de caracteres que descreve os tipos de endereços suportados pelos provedores de transporte que estão ativos na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="2afac-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

