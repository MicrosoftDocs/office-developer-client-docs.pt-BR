---
title: Configuração da ordem de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339386"
---
# <a name="setting-transport-order"></a><span data-ttu-id="d3d9b-103">Configuração da ordem de transporte</span><span class="sxs-lookup"><span data-stu-id="d3d9b-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="d3d9b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3d9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3d9b-105">O spooler MAPI atribui responsabilidade para mensagens de saída com base nos tipos de endereço e identificadores que os provedores de transporte declaram que podem lidar.</span><span class="sxs-lookup"><span data-stu-id="d3d9b-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="d3d9b-106">Os provedores de transporte publicam uma lista de tipos de endereço e identificadores com suporte, armazenados em estruturas **MAPIUID** , quando MAPI chama o método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) , diretamente após o logon.</span><span class="sxs-lookup"><span data-stu-id="d3d9b-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="d3d9b-107">O tipo de endereço de um destinatário é armazenado em sua propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d3d9b-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d3d9b-108">O registro de um tipo de endereço indica a MAPI que o provedor de transporte pode entregar aos destinatários com a propriedade **PR_ADDRTYPE** definida para o tipo de endereço registrado.</span><span class="sxs-lookup"><span data-stu-id="d3d9b-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="d3d9b-109">Da mesma forma, registrar-se para um **MAPIUID** indica que o provedor de transporte pode entregar para destinatários representados por identificadores de entrada com o **MAPIUID**registrado.</span><span class="sxs-lookup"><span data-stu-id="d3d9b-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="d3d9b-110">A maioria dos provedores de transporte se registra para um ou mais tipos de endereço; alguns registros por **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="d3d9b-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="d3d9b-111">Os provedores de transporte que estão rigidamente acoplados a um provedor de catálogo de endereços e entendem seu formato de identificador de entrada podem se registrar para lidar com as mensagens por **MAPIUID**, melhorando o desempenho.</span><span class="sxs-lookup"><span data-stu-id="d3d9b-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="d3d9b-112">Esses provedores de transporte rigidamente acoplados podem extrair o endereço de email do destinatário e outras informações necessárias do identificador de entrada sem precisar abri-lo com uma chamada **IMAPISupport:: OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="d3d9b-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="d3d9b-113">O MAPI mantém um pedido de provedores de transporte, usado quando vários provedores de transporte foram registrados para o mesmo tipo de endereço ou **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="d3d9b-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="d3d9b-114">Você pode substituir esse pedido chamando [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) e passando uma lista ordenada dos **MAPIUID**s de todos os provedores de transporte ativos apontados pelo parâmetro _lpUIDList_ .:</span><span class="sxs-lookup"><span data-stu-id="d3d9b-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID**s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="d3d9b-115">Para recuperar uma lista de todos os tipos de endereço que podem ser tratados por um dos provedores de transporte ativos, chame [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="d3d9b-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="d3d9b-116">**EnumAdrTypes** retorna uma matriz de cadeias de caracteres que descreve os tipos de endereço suportados pelos provedores de transporte ativos na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="d3d9b-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

