---
title: Exibindo uma tabela de conteúdo de pasta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 30099e9fe645f810e08ba331717cff975f69b313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766436"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="dfe9c-103">Exibindo uma tabela de conteúdo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfe9c-103">Displaying a folder contents table</span></span>

<span data-ttu-id="dfe9c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dfe9c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dfe9c-105">A tabela de conteúdo de uma pasta contém informações de resumo sobre todas as suas mensagens.</span><span class="sxs-lookup"><span data-stu-id="dfe9c-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="dfe9c-106">Informações de resumo sobre novas mensagens de entrada é exibida na tabela de conteúdo da pasta de recebimento para a classe da mensagem.</span><span class="sxs-lookup"><span data-stu-id="dfe9c-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="dfe9c-107">Para disponibilizar essas informações para usuários, recuperar a tabela e exibir as colunas e linhas conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="dfe9c-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="dfe9c-108">**Para exibir uma tabela de conteúdo de pasta**</span><span class="sxs-lookup"><span data-stu-id="dfe9c-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="dfe9c-109">Chame [IMsgStore::OpenEntry](imsgstore-openentry.md), passando o identificador de entrada da pasta que contém a tabela.</span><span class="sxs-lookup"><span data-stu-id="dfe9c-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="dfe9c-110">Chame o método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da pasta para abrir a tabela de seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="dfe9c-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="dfe9c-111">Limite de sua exibição da tabela conteúdo se desejado, chamando o método da tabela [IMAPITable::SetColumns](imapitable-setcolumns.md) para especificar colunas específicas.</span><span class="sxs-lookup"><span data-stu-id="dfe9c-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="dfe9c-112">Limite sua exibição da tabela de conteúdo, se desejado, chamando o método da tabela [IMAPITable:: Restrict](imapitable-restrict.md) para filtrar linhas específicas.</span><span class="sxs-lookup"><span data-stu-id="dfe9c-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="dfe9c-113">Se, por exemplo, você deseja mostrar somente as mensagens com uma classe de mensagem específica que ainda precisam ser lido:</span><span class="sxs-lookup"><span data-stu-id="dfe9c-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="dfe9c-114">Crie uma restrição de propriedade em uma estrutura de [SPropertyRestriction](spropertyrestriction.md) que corresponda a propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) com a classe de mensagem desejado.</span><span class="sxs-lookup"><span data-stu-id="dfe9c-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="dfe9c-115">Crie uma restrição de bitmask em uma estrutura de [SBitMaskRestriction](sbitmaskrestriction.md) que usa **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) como a marca de propriedade e o valor MSGFLAG_UNREAD como a máscara.</span><span class="sxs-lookup"><span data-stu-id="dfe9c-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="dfe9c-116">Crie uma restrição em uma estrutura de [SAndRestriction](sandrestriction.md) que une as restrições de propriedade e bitmask.</span><span class="sxs-lookup"><span data-stu-id="dfe9c-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="dfe9c-117">Classificar a tabela de conteúdo, se desejado, chamando o método da tabela [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="dfe9c-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="dfe9c-118">Chame [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas as linhas da tabela de conteúdo para processamento.</span><span class="sxs-lookup"><span data-stu-id="dfe9c-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

