---
title: Manipular um catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b685244a-fe1b-4416-85d3-4bd86ccbc3aa
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 464549732562a4a02d081dc5a4c5e573e38cbbce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413917"
---
# <a name="handling-the-address-book"></a><span data-ttu-id="7bcab-103">Manipular um catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="7bcab-103">Handling the address book</span></span>
  
<span data-ttu-id="7bcab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bcab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bcab-105">A manipulação do livro de endereços MAPI pode incluir a extração de entradas a serem usadas como destinatários de mensagens, a modificação de propriedades de destinatários, a adição de usuários de mensagens ou listas de distribuição, a criação de one-offs e a exibição de uma ou mais caixas de diálogo de endereço comuns para permitir que os usuários naveguem por informações de endereço e façam alterações.</span><span class="sxs-lookup"><span data-stu-id="7bcab-105">Handling the MAPI address book can include extracting entries to be used as message recipients, modifying recipient properties, adding messaging users or distribution lists, creating one-offs, and displaying one or more of the common address dialog boxes to allow users to browse address information and make changes.</span></span>

- <span data-ttu-id="7bcab-106">[Abrir o Address Book](opening-the-address-book.md): descreve como usar MAPI para abrir um livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="7bcab-106">[Opening the Address Book](opening-the-address-book.md): Describes how to use MAPI to open an address book.</span></span>
    
- <span data-ttu-id="7bcab-107">[Exibindo a caixa de diálogo Endereço Comum:](displaying-the-common-address-dialog-box.md)descreve como exibir diferentes contêineres do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="7bcab-107">[Displaying the Common Address Dialog Box](displaying-the-common-address-dialog-box.md): Describes how to display different address book containers.</span></span>
    
- <span data-ttu-id="7bcab-108">[Abrir um contêiner do Address Book:](opening-an-address-book-container.md)descreve como abrir diferentes contêineres do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="7bcab-108">[Opening an Address Book Container](opening-an-address-book-container.md): Describes how to open different address book containers.</span></span>
    
- <span data-ttu-id="7bcab-109">[Definindo opções de agenda:](setting-address-book-options.md)descreve como definir as propriedades que descrevem as opções para usar o livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="7bcab-109">[Setting Address Book Options](setting-address-book-options.md): Describes how to set the properties that describe options for using the address book.</span></span>
    
- <span data-ttu-id="7bcab-110">[Criando um destinatário](creating-a-recipient.md): descreve como criar destinatários ao endereçamento de mensagens e adicionar entradas a contêineres de agendamento modificáveis.</span><span class="sxs-lookup"><span data-stu-id="7bcab-110">[Creating a Recipient](creating-a-recipient.md): Describes how to create recipients when addressing messages and adding entries to modifiable address book containers.</span></span>
    
- <span data-ttu-id="7bcab-111">[Criando uma lista de distribuição](creating-a-distribution-list.md): descreve como criar uma lista de distribuição em um contêiner modificável.</span><span class="sxs-lookup"><span data-stu-id="7bcab-111">[Creating a Distribution List](creating-a-distribution-list.md): Describes how to create a distribution list into a modifiable container.</span></span>
    
- <span data-ttu-id="7bcab-112">[Copiar um destinatário:](copying-a-recipient.md)descreve como copiar destinatários de um contêiner para outro ou o mesmo contêiner.</span><span class="sxs-lookup"><span data-stu-id="7bcab-112">[Copying a Recipient](copying-a-recipient.md): Describes how to copy recipients from one container into another or the same container.</span></span>
    
- <span data-ttu-id="7bcab-113">[Excluir um destinatário](deleting-a-recipient.md): descreve como remover uma ou mais entradas do livro de endereços de um contêiner modificável.</span><span class="sxs-lookup"><span data-stu-id="7bcab-113">[Deleting a Recipient](deleting-a-recipient.md): Describes how to remove one or more address book entries from a modifiable container.</span></span>
    
- <span data-ttu-id="7bcab-114">Preparando um destinatário [:](preparing-a-recipient.md)descreve como preparar destinatários convertendo seus identificadores de entrada de curto prazo em identificadores de entrada de longo prazo e possivelmente adicionando, alterando ou reordenando propriedades.</span><span class="sxs-lookup"><span data-stu-id="7bcab-114">[Preparing a Recipient](preparing-a-recipient.md): Describes how to prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span>
    
- <span data-ttu-id="7bcab-115">[Acessar os membros de uma lista de distribuição:](accessing-the-members-of-a-distribution-list.md)descreve como acessar os membros de uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="7bcab-115">[Accessing the Members of a Distribution List](accessing-the-members-of-a-distribution-list.md): Describes how to access the members of a distribution list.</span></span>
    
- <span data-ttu-id="7bcab-116">[Recuperando propriedades de destinatário:](retrieving-recipient-properties.md)descreve como acessar uma ou mais propriedades de uma entrada do livro de endereços de destinatário.</span><span class="sxs-lookup"><span data-stu-id="7bcab-116">[Retrieving Recipient Properties](retrieving-recipient-properties.md): Describes how to access one or more properties of a recipient address book entry.</span></span>
    
- <span data-ttu-id="7bcab-117">[Pesquisar o Address Book](searching-the-address-book.md): descreve os dois níveis de funcionalidade de pesquisa MAPI.</span><span class="sxs-lookup"><span data-stu-id="7bcab-117">[Searching the Address Book](searching-the-address-book.md): Describes the two levels of MAPI search functionality.</span></span> 
    
- <span data-ttu-id="7bcab-118">[Usando uma Caixa de Diálogo de Pesquisa](using-an-advanced-search-dialog-box.md)Avançada: descreve como executar uma funcionalidade de pesquisa avançada em um contêiner de um livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="7bcab-118">[Using an Advanced Search Dialog Box](using-an-advanced-search-dialog-box.md): Describes how to run an advanced search functionality in an address book container.</span></span>
    
- <span data-ttu-id="7bcab-119">[Resolvendo um nome de destinatário:](resolving-a-recipient-name.md)descreve como resolver um nome em um livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="7bcab-119">[Resolving a Recipient Name](resolving-a-recipient-name.md): Describes how to resolve a name in an address book.</span></span>
    
- <span data-ttu-id="7bcab-120">[Expandindo listas de](expanding-distribution-lists.md)distribuição : descreve como solicitar o MAPI para expandir uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="7bcab-120">[Expanding Distribution Lists](expanding-distribution-lists.md): Describes how to prompt MAPI to expand a distribution list.</span></span>
    

