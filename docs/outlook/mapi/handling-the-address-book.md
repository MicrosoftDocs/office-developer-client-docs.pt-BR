---
title: Manipulação de catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b685244a-fe1b-4416-85d3-4bd86ccbc3aa
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6ef441b4315ef21f8b16dc062596bc7f1e526e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766689"
---
# <a name="handling-the-address-book"></a><span data-ttu-id="a2db3-103">Manipulação de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="a2db3-103">Handling the address book</span></span>
  
<span data-ttu-id="a2db3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a2db3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a2db3-105">Manipulação de catálogo de endereços MAPI pode incluir extraindo entradas que será usado como destinatários da mensagem, modificando propriedades de destinatário, adicionando usuários mensagens ou listas de distribuição, criação de algo isolado e exibindo uma ou mais das caixas de diálogo comuns do endereço para permitir que usuários a procurar informações de endereço e fazer alterações.</span><span class="sxs-lookup"><span data-stu-id="a2db3-105">Handling the MAPI address book can include extracting entries to be used as message recipients, modifying recipient properties, adding messaging users or distribution lists, creating one-offs, and displaying one or more of the common address dialog boxes to allow users to browse address information and make changes.</span></span>

- <span data-ttu-id="a2db3-106">[Abrir o catálogo de endereços](opening-the-address-book.md): descreve como usar o MAPI para abrir um catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="a2db3-106">[Opening the Address Book](opening-the-address-book.md): Describes how to use MAPI to open an address book.</span></span>
    
- <span data-ttu-id="a2db3-107">[Exibir a caixa de diálogo endereço comuns](displaying-the-common-address-dialog-box.md): descreve como exibir contêineres do catálogo de endereço diferente.</span><span class="sxs-lookup"><span data-stu-id="a2db3-107">[Displaying the Common Address Dialog Box](displaying-the-common-address-dialog-box.md): Describes how to display different address book containers.</span></span>
    
- <span data-ttu-id="a2db3-108">[Abrindo um contêiner de catálogo de endereços](opening-an-address-book-container.md): descreve como abrir contêineres do catálogo de endereço diferente.</span><span class="sxs-lookup"><span data-stu-id="a2db3-108">[Opening an Address Book Container](opening-an-address-book-container.md): Describes how to open different address book containers.</span></span>
    
- <span data-ttu-id="a2db3-109">[Definindo opções de catálogo de endereços](setting-address-book-options.md): descreve como definir as propriedades que descrevem as opções para usar o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="a2db3-109">[Setting Address Book Options](setting-address-book-options.md): Describes how to set the properties that describe options for using the address book.</span></span>
    
- <span data-ttu-id="a2db3-110">[Criando um destinatário](creating-a-recipient.md): descreve como criar destinatários quando lidando com mensagens e adicionando entradas em contêineres de catálogo de endereços modificável.</span><span class="sxs-lookup"><span data-stu-id="a2db3-110">[Creating a Recipient](creating-a-recipient.md): Describes how to create recipients when addressing messages and adding entries to modifiable address book containers.</span></span>
    
- <span data-ttu-id="a2db3-111">[Criar uma lista de distribuição](creating-a-distribution-list.md): descreve como criar uma lista de distribuição para um contêiner pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="a2db3-111">[Creating a Distribution List](creating-a-distribution-list.md): Describes how to create a distribution list into a modifiable container.</span></span>
    
- <span data-ttu-id="a2db3-112">[Copiando um destinatário](copying-a-recipient.md): descreve como copiar os destinatários de um contêiner para outra ou mesmo contêiner.</span><span class="sxs-lookup"><span data-stu-id="a2db3-112">[Copying a Recipient](copying-a-recipient.md): Describes how to copy recipients from one container into another or the same container.</span></span>
    
- <span data-ttu-id="a2db3-113">[Excluindo um destinatário](deleting-a-recipient.md): descreve como remover um ou mais entradas do catálogo de endereços de um contêiner pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="a2db3-113">[Deleting a Recipient](deleting-a-recipient.md): Describes how to remove one or more address book entries from a modifiable container.</span></span>
    
- <span data-ttu-id="a2db3-114">[Preparando um destinatário](preparing-a-recipient.md): descreve como prepara destinatários, convertendo seus identificadores de entrada de curto prazo aos identificadores de entrada de longo prazo e, possivelmente, adicionar, alterar ou reordenar propriedades.</span><span class="sxs-lookup"><span data-stu-id="a2db3-114">[Preparing a Recipient](preparing-a-recipient.md): Describes how to prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span>
    
- <span data-ttu-id="a2db3-115">[Acessando os membros de uma lista de distribuição](accessing-the-members-of-a-distribution-list.md): descreve como acessar os membros de uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="a2db3-115">[Accessing the Members of a Distribution List](accessing-the-members-of-a-distribution-list.md): Describes how to access the members of a distribution list.</span></span>
    
- <span data-ttu-id="a2db3-116">[Recuperando propriedades de destinatário](retrieving-recipient-properties.md): descreve como acessar uma ou mais propriedades de uma entrada de catálogo de endereço do destinatário.</span><span class="sxs-lookup"><span data-stu-id="a2db3-116">[Retrieving Recipient Properties](retrieving-recipient-properties.md): Describes how to access one or more properties of a recipient address book entry.</span></span>
    
- <span data-ttu-id="a2db3-117">[Pesquisar o catálogo de endereços](searching-the-address-book.md): descreve os dois níveis de funcionalidade de pesquisa MAPI.</span><span class="sxs-lookup"><span data-stu-id="a2db3-117">[Searching the Address Book](searching-the-address-book.md): Describes the two levels of MAPI search functionality.</span></span> 
    
- <span data-ttu-id="a2db3-118">[Usando uma caixa de diálogo de pesquisa avançada](using-an-advanced-search-dialog-box.md): descreve como executar uma funcionalidade de pesquisa avançada em um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="a2db3-118">[Using an Advanced Search Dialog Box](using-an-advanced-search-dialog-box.md): Describes how to run an advanced search functionality in an address book container.</span></span>
    
- <span data-ttu-id="a2db3-119">[Resolução de um nome de destinatário](resolving-a-recipient-name.md): descreve como resolver um nome de um catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="a2db3-119">[Resolving a Recipient Name](resolving-a-recipient-name.md): Describes how to resolve a name in an address book.</span></span>
    
- <span data-ttu-id="a2db3-120">[Expandir listas de distribuição](expanding-distribution-lists.md): descreve como solicitar MAPI para expandir uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="a2db3-120">[Expanding Distribution Lists](expanding-distribution-lists.md): Describes how to prompt MAPI to expand a distribution list.</span></span>
    

