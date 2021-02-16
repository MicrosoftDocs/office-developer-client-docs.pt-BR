---
title: Desenvolvendo um provedor de lista de endereços MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1db3ce53a1da60d946e52a03369c10547676277f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409367"
---
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="5457e-103">Desenvolvendo um provedor de lista de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="5457e-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="5457e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5457e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5457e-105">Um provedor de agendas fornece informações de destinatário para aplicativos cliente, para provedores de transporte e armazenamento de mensagens e para MAPI.</span><span class="sxs-lookup"><span data-stu-id="5457e-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="5457e-106">As informações do destinatário são organizadas hierarquicamente em compartimentos de armazenamento conhecidos como contêineres.</span><span class="sxs-lookup"><span data-stu-id="5457e-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="5457e-107">Cada livro de endereços no perfil contribui com um ou mais contêineres de nível superior, ou pai, para o livro de endereços MAPI, uma exibição integrada das informações de destinatário de todos os provedores de livro de endereços em uma sessão.</span><span class="sxs-lookup"><span data-stu-id="5457e-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="5457e-108">É por meio do livro de endereços MAPI que os clientes e outros provedores de serviços têm acesso aos dados de um provedor de agendas.</span><span class="sxs-lookup"><span data-stu-id="5457e-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="5457e-109">MAPI builds the integrated address book by:</span><span class="sxs-lookup"><span data-stu-id="5457e-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="5457e-110">Recuperar os contêineres de nível superior de cada provedor de agendamento de endereços.</span><span class="sxs-lookup"><span data-stu-id="5457e-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="5457e-111">Recuperação da tabela de hierarquias de cada contêiner.</span><span class="sxs-lookup"><span data-stu-id="5457e-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="5457e-112">Copiando cada tabela de hierarquia em uma tabela de hierarquia integrada.</span><span class="sxs-lookup"><span data-stu-id="5457e-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="5457e-113">É a tabela de hierarquia integrada exposta ao cliente.</span><span class="sxs-lookup"><span data-stu-id="5457e-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="5457e-114">O MAPI impõe poucos requisitos para os autores de provedores de agendas.</span><span class="sxs-lookup"><span data-stu-id="5457e-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="5457e-115">A variedade de recursos possíveis que você pode implementar como um autor de livro de endereços é variada e flexível.</span><span class="sxs-lookup"><span data-stu-id="5457e-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="5457e-116">Por exemplo, seu provedor pode estar limitado a fornecer uma exibição somente leitura de um determinado tipo de informação de destinatário ou implementar um conjunto completo de recursos, talvez permitindo que clientes ou provedores façam adições ou modificações nos dados do destinatário e imponham critérios de pesquisa para definir exibições personalizadas.</span><span class="sxs-lookup"><span data-stu-id="5457e-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="5457e-117">Os dados do provedor podem residir localmente em um arquivo ou banco de dados ou em um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="5457e-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="5457e-118">Alguns provedores de agendamento de endereço devem trabalhar com um sistema de mensagens específico, fortemente unido a um provedor de transporte, enquanto outros podem operar com qualquer sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5457e-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="5457e-119">O MAPI define um tipo especial de provedor de livro de endereços chamado de um livro de endereços pessoal, ou PAB, que implementa um único contêiner modificável e pode manter informações de destinatário copiadas de outros contêineres, bem como informações criadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="5457e-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="5457e-120">Embora qualquer provedor de agendas possa implementar um PAB e vários PABs possam ser adicionados a um perfil, apenas um desses provedores pode ser designado para operar como PAB durante qualquer sessão.</span><span class="sxs-lookup"><span data-stu-id="5457e-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

