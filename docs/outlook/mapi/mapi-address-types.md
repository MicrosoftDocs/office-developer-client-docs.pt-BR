---
title: Tipos de endereço MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b0ff4ecff7a6e834f1e017adc11244657896db03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405433"
---
# <a name="mapi-address-types"></a><span data-ttu-id="610d7-103">Tipos de endereço MAPI</span><span class="sxs-lookup"><span data-stu-id="610d7-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="610d7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="610d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="610d7-105">Cada usuário de mensagens é associado a um tipo de endereço, uma cadeia de caracteres que descreve o formato do endereço do usuário que é armazenado na propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="610d7-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="610d7-106">Os tipos de endereço mapeiam para formatos de endereço.</span><span class="sxs-lookup"><span data-stu-id="610d7-106">Address types map to address formats.</span></span> <span data-ttu-id="610d7-107">Ou seja, observando o tipo de endereço de um destinatário, os aplicativos clientes podem determinar como formatar um endereço apropriado para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="610d7-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="610d7-108">Por exemplo, o `SMTP` tipo de endereço especifica o endereço de Internet padrão:</span><span class="sxs-lookup"><span data-stu-id="610d7-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="610d7-109">E o tipo `EX` de endereço especifica um endereço do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="610d7-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="610d7-110">Todas as entradas do catálogo de endereços devem ter um tipo de endereço válido.</span><span class="sxs-lookup"><span data-stu-id="610d7-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="610d7-111">Os clientes exigem que seus usuários especifiquem um tipo de endereço ao criar um tipo de destinatário personalizado sem suporte pelo provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="610d7-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="610d7-112">Para as entradas que eles dão suporte, os provedores de catálogo de endereços são necessários para fornecer tipos de endereço válidos.</span><span class="sxs-lookup"><span data-stu-id="610d7-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="610d7-113">MAPI define apenas um tipo de endereço: MAPIPDL, que significa lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="610d7-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="610d7-114">Para obter uma lista dos tipos de endereço suportados por todos os provedores de transporte na sessão, os aplicativos cliente chamam o método **IMAPISession:: EnumAdrTypes** .</span><span class="sxs-lookup"><span data-stu-id="610d7-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="610d7-115">Para obter mais informações, consulte [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="610d7-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

