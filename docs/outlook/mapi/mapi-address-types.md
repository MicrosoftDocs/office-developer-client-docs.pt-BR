---
title: Tipos de endereço MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 20eb429b2574f67e8b28ae96eeb96f42840123d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767804"
---
# <a name="mapi-address-types"></a><span data-ttu-id="831ef-103">Tipos de endereço MAPI</span><span class="sxs-lookup"><span data-stu-id="831ef-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="831ef-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="831ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="831ef-105">Cada usuário de mensagens é associado um tipo de endereço, uma cadeia de caracteres que descreve o formato do endereço do usuário que está armazenado na propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="831ef-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="831ef-106">Tipos de endereço são mapeados para formatos de endereço.</span><span class="sxs-lookup"><span data-stu-id="831ef-106">Address types map to address formats.</span></span> <span data-ttu-id="831ef-107">Ou seja, examinando o tipo de endereço do destinatário, aplicativos cliente podem determinar como formatar um endereço apropriado para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="831ef-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="831ef-108">Por exemplo, o `SMTP` tipo de endereço Especifica o endereço de Internet padrão:</span><span class="sxs-lookup"><span data-stu-id="831ef-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="831ef-109">E, o `EX` tipo de endereço Especifica um endereço de servidor do Exchange.</span><span class="sxs-lookup"><span data-stu-id="831ef-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="831ef-110">Todas as entradas do catálogo de endereços devem ter um tipo de endereço válido.</span><span class="sxs-lookup"><span data-stu-id="831ef-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="831ef-111">Os clientes precisam de seus usuários especificar um tipo de endereço ao criar um tipo de destinatário personalizado sem suporte pelo provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="831ef-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="831ef-112">Para as entradas que oferecem suporte a eles, provedores de catálogo de endereços são necessárias para fornecer tipos de endereço válido.</span><span class="sxs-lookup"><span data-stu-id="831ef-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="831ef-113">MAPI define o tipo de apenas um endereço: MAPIPDL, o que significa de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="831ef-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="831ef-114">Para obter uma lista dos tipos de endereço suportado por todos os provedores de transporte da sessão, os aplicativos cliente chamam o método de **IMAPISession::EnumAdrTypes** .</span><span class="sxs-lookup"><span data-stu-id="831ef-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="831ef-115">Para obter mais informações, consulte [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="831ef-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

