---
title: Desenvolver um provedor do catálogo de endereços MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 03f53dbfbe57db76ee8ceefda3f6938301f70da8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766400"
---
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="1c135-103">Desenvolver um provedor do catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="1c135-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="1c135-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c135-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c135-105">Um provedor de catálogo de endereços fornece informações de destinatário para aplicativos de cliente, para o repositório de mensagem e transporte provedores e MAPI.</span><span class="sxs-lookup"><span data-stu-id="1c135-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="1c135-106">Informações do destinatário são organizadas hierarquicamente em compartimentos de armazenamento conhecidos como contêineres.</span><span class="sxs-lookup"><span data-stu-id="1c135-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="1c135-107">Cada catálogo de endereços no perfil contribui um ou mais nível superior, ou pai, provedores de livro de contêineres ao catálogo de endereços MAPI, uma exibição integrada de informações de destinatário de todos os endereços em uma sessão.</span><span class="sxs-lookup"><span data-stu-id="1c135-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="1c135-108">É por meio do catálogo de endereços MAPI que os clientes e outros provedores de serviços obtém acesso aos dados de um provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1c135-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="1c135-109">MAPI constrói o catálogo de endereços integrada por:</span><span class="sxs-lookup"><span data-stu-id="1c135-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="1c135-110">Recuperando os contêineres de nível superior de cada provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1c135-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="1c135-111">Recuperando a tabela de hierarquia do cada contêiner.</span><span class="sxs-lookup"><span data-stu-id="1c135-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="1c135-112">Copiando cada tabela de hierarquia em uma tabela de hierarquia integrada.</span><span class="sxs-lookup"><span data-stu-id="1c135-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="1c135-113">É a tabela de hierarquia integrado que é exposta no cliente.</span><span class="sxs-lookup"><span data-stu-id="1c135-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="1c135-114">MAPI impõe poucos requisitos de escritores de provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1c135-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="1c135-115">A gama de recursos possíveis que você pode implementar como um gravador de catálogo de endereços é variados e flexíveis.</span><span class="sxs-lookup"><span data-stu-id="1c135-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="1c135-116">Por exemplo, seu provedor poderia ser limitados fornecendo um modo de exibição somente leitura de um determinado tipo de informação de destinatário ou implementar um conjunto completo de recursos, talvez permitindo que os clientes ou provedores para tornar as inclusões ou modificações nos dados de destinatário e para impor critérios de pesquisa para a definição de exibições personalizadas.</span><span class="sxs-lookup"><span data-stu-id="1c135-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="1c135-117">Dados do seu provedor podem residir localmente em um arquivo ou banco de dados ou em um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="1c135-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="1c135-118">Alguns provedores de catálogo de endereços devem trabalhar com um sistema de mensagens específico, firmemente combinado com um provedor de transporte, enquanto outros podem operar com qualquer sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1c135-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="1c135-119">MAPI define um tipo especial de provedor de catálogo de endereços chamado um catálogo de endereços pessoal ou PAB, que implementa um único contêiner modificável e pode conter informações copiadas de outros contêineres, bem como as informações que criou diretamente do destinatário.</span><span class="sxs-lookup"><span data-stu-id="1c135-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="1c135-120">Embora qualquer provedor de catálogo de endereços pode implementar um PAB e vários PABs podem ser adicionados a um perfil, apenas um desses provedores pode ser designado para operar como o PAB durante uma sessão de qualquer.</span><span class="sxs-lookup"><span data-stu-id="1c135-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

