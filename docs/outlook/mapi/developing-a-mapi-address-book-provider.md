---
title: Desenvolver um provedor de catálogo de endereços MAPI
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
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="fef49-103">Desenvolver um provedor de catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="fef49-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="fef49-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fef49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fef49-105">Um provedor de catálogo de endereços fornece informações de destinatários para aplicativos clientes, para provedores de transporte e armazenamento de mensagens e para MAPI.</span><span class="sxs-lookup"><span data-stu-id="fef49-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="fef49-106">As informações do destinatário são organizadas hierarquicamente em compartimentos de armazenamento conhecidos como contêineres.</span><span class="sxs-lookup"><span data-stu-id="fef49-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="fef49-107">Cada catálogo de endereços no perfil contribui para um ou mais recipientes de nível superior ou pai para o catálogo de endereços MAPI, uma visão integrada das informações de destinatário de todos os provedores de catálogo de endereços em uma sessão.</span><span class="sxs-lookup"><span data-stu-id="fef49-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="fef49-108">É através do catálogo de endereços MAPI que os clientes e outros provedores de serviços obtêm acesso aos dados de um provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="fef49-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="fef49-109">MAPI cria o catálogo de endereços integrados por:</span><span class="sxs-lookup"><span data-stu-id="fef49-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="fef49-110">Recuperar os contêineres de nível superior de cada provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="fef49-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="fef49-111">Recuperar a tabela de hierarquia de cada contêiner.</span><span class="sxs-lookup"><span data-stu-id="fef49-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="fef49-112">Copiando cada tabela de hierarquia em uma tabela de hierarquia integrada.</span><span class="sxs-lookup"><span data-stu-id="fef49-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="fef49-113">É a tabela de hierarquia integrada que é exposta ao cliente.</span><span class="sxs-lookup"><span data-stu-id="fef49-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="fef49-114">O MAPI impõe alguns requisitos nos escritores do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="fef49-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="fef49-115">O intervalo de possíveis recursos que você pode implementar como gravador de catálogo de endereços é variado e flexível.</span><span class="sxs-lookup"><span data-stu-id="fef49-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="fef49-116">Por exemplo, o provedor pode ser limitado ao fornecimento de um modo de exibição somente leitura de um tipo específico de informações do destinatário ou implementar um conjunto completo de recursos, talvez permitindo que clientes ou provedores façam inclusões ou modificações nos dados do destinatário e imponham critérios de pesquisa para definição de modos de exibição personalizados.</span><span class="sxs-lookup"><span data-stu-id="fef49-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="fef49-117">Os dados do provedor podem residir localmente em um arquivo ou banco de dados ou em um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="fef49-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="fef49-118">Alguns provedores de catálogos de endereços servem para trabalhar com um sistema de mensagens específico, intimamente acoplado a um provedor de transporte, enquanto outros podem operar com qualquer sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fef49-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="fef49-119">O MAPI define um tipo especial de provedor de catálogo de endereços chamado de catálogo de endereços pessoal, ou PAB, que implementa um único contêiner modificável e pode conter informações de destinatário copiadas de outros contêineres, bem como informações criadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="fef49-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="fef49-120">Embora qualquer provedor de catálogo de endereços possa implementar um PAB e vários PABs possam ser adicionados a um perfil, somente um desses provedores pode ser designado para operar como o PAB durante uma única sessão.</span><span class="sxs-lookup"><span data-stu-id="fef49-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

