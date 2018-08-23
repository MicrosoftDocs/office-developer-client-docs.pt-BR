---
title: Configurar um pedido de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6e4c318678fdce7976140ff8f480ae638fd3ca4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593022"
---
# <a name="setting-transport-order"></a><span data-ttu-id="5325e-103">Configurar um pedido de transporte</span><span class="sxs-lookup"><span data-stu-id="5325e-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="5325e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5325e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5325e-105">O MAPI spooler atribui a responsabilidade para mensagens de saída com base nos tipos de endereço e identificadores que declara, podem lidar com provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="5325e-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="5325e-106">Provedores de transporte publicarem uma lista de tipos de endereço com suporte e os identificadores — armazenados nas estruturas **MAPIUID** — quando MAPI chama o método seus [IXPLogon::AddressTypes](ixplogon-addresstypes.md) , diretamente após o logon.</span><span class="sxs-lookup"><span data-stu-id="5325e-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="5325e-107">Tipo de endereço do destinatário é armazenado em sua propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5325e-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="5325e-108">Registrando para um tipo de endereço indica MAPI que o provedor de transporte que pode fornecer aos destinatários com sua propriedade **PR_ADDRTYPE** definida como o tipo de endereço registrado.</span><span class="sxs-lookup"><span data-stu-id="5325e-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="5325e-109">Da mesma forma, se registrar para uma **MAPIUID** indica que o provedor de transporte pode fornecer aos destinatários que são representados por identificadores de entrada com o registrados **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="5325e-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="5325e-110">A maioria dos provedores de transporte registrar para um ou mais tipos de endereço. poucos registro por **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="5325e-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="5325e-111">Provedores de transporte que estejam intimamente ligadas com um provedor de catálogo de endereços e entendem o seu formato de identificador de entrada podem se inscrever para lidar com as mensagens por **MAPIUID**, melhorando o desempenho.</span><span class="sxs-lookup"><span data-stu-id="5325e-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="5325e-112">Esses provedores de transporte de ligação estreita podem extrair o endereço de email do destinatário e outras informações necessárias do identificador de entrada sem precisar abri-lo com uma chamada **IMAPISupport::OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="5325e-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="5325e-113">MAPI mantém uma ordem para provedores de transporte, usada quando vários provedores de transporte tiverem registrado para o mesmo tipo de endereço ou **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="5325e-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="5325e-114">Você pode substituir essa ordem chamando [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) e passar uma lista ordenada do s **MAPIUID**de todos os provedores de transporte ativa apontado pelo parâmetro _lpUIDList_ .:</span><span class="sxs-lookup"><span data-stu-id="5325e-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID**s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="5325e-115">Para recuperar uma lista de todos os tipos de endereço que podem ser manipulados por um dos provedores de transporte ativa, chame [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="5325e-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="5325e-116">**EnumAdrTypes** retorna uma matriz de cadeias de caracteres que descreve os tipos de endereço suportados pelos provedores de transporte que estão ativos na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="5325e-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

