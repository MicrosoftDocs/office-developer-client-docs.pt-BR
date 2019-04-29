---
title: Exibir uma tabela de conteúdo da pasta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 56847283afaf41c1d45cdb875ddf49eaa5881175
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412391"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="90104-103">Exibir uma tabela de conteúdo da pasta</span><span class="sxs-lookup"><span data-stu-id="90104-103">Displaying a folder contents table</span></span>

<span data-ttu-id="90104-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90104-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90104-105">A tabela de conteúdo de uma pasta contém informações resumidas sobre todas as suas mensagens.</span><span class="sxs-lookup"><span data-stu-id="90104-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="90104-106">Informações de resumo sobre novas mensagens de entrada são exibidas na tabela de conteúdo da pasta de recebimento da classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="90104-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="90104-107">Para disponibilizar essas informações aos usuários, recupere a tabela e exiba as colunas e linhas conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="90104-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="90104-108">**Para exibir uma tabela de conteúdo da pasta**</span><span class="sxs-lookup"><span data-stu-id="90104-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="90104-109">Chame [IMsgStore:: OpenEntry](imsgstore-openentry.md), passando o identificador de entrada da pasta que contém a tabela.</span><span class="sxs-lookup"><span data-stu-id="90104-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="90104-110">Chame o método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable da pasta para abrir sua tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="90104-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="90104-111">Limite o modo de exibição da tabela de conteúdo se quiser chamar o método [IMAPITable::](imapitable-setcolumns.md) SetColumns para especificar colunas específicas.</span><span class="sxs-lookup"><span data-stu-id="90104-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="90104-112">Limite a exibição da tabela de conteúdo, se desejado, chamando o método [IMAPITable:: Restrict](imapitable-restrict.md) da tabela para filtrar linhas específicas.</span><span class="sxs-lookup"><span data-stu-id="90104-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="90104-113">Se, por exemplo, você quiser mostrar apenas as mensagens com uma classe de mensagem específica que ainda devem ser lidas:</span><span class="sxs-lookup"><span data-stu-id="90104-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="90104-114">Crie uma restrição de propriedade em uma estrutura [SPropertyRestriction](spropertyrestriction.md) que coincida com a propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) com a classe de mensagem desejada.</span><span class="sxs-lookup"><span data-stu-id="90104-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="90104-115">Crie uma restrição de bitmask em uma estrutura [SBitMaskRestriction](sbitmaskrestriction.md) que usa **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) como a marca de propriedade e o valor de MSGFLAG_UNREAD como máscara.</span><span class="sxs-lookup"><span data-stu-id="90104-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="90104-116">Criar uma restrição em uma estrutura [SAndRestriction](sandrestriction.md) que une as restrições de propriedade e bitmask.</span><span class="sxs-lookup"><span data-stu-id="90104-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="90104-117">Classifique a tabela de conteúdo se desejar chamando o método imApitable [:: SortTable](imapitable-sorttable.md) da tabela.</span><span class="sxs-lookup"><span data-stu-id="90104-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="90104-118">Call [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas as linhas da tabela de conteúdo para processamento.</span><span class="sxs-lookup"><span data-stu-id="90104-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

