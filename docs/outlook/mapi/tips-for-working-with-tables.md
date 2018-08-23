---
title: Dicas para trabalhar com tabelas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d9b4d6a469904058b0484428dbf20a90119e96bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586134"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="07789-103">Dicas para trabalhar com tabelas</span><span class="sxs-lookup"><span data-stu-id="07789-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="07789-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07789-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07789-105">Trabalhando com um MAPI tabela é um pouco semelhante a trabalhar com uma tabela de banco de dados relacional.</span><span class="sxs-lookup"><span data-stu-id="07789-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="07789-106">Um usuário pode limitar o número de linhas e colunas no modo de exibição e especifique sua ordem.</span><span class="sxs-lookup"><span data-stu-id="07789-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="07789-107">Linhas podem ser recuperados de um por vez ou em grupos.</span><span class="sxs-lookup"><span data-stu-id="07789-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="07789-108">Um cursor que controla a posição atual pode ser movido para um local específico na tabela.</span><span class="sxs-lookup"><span data-stu-id="07789-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="07789-109">Para trabalhar com tabelas, os clientes usam a interface de somente leitura, [IMAPITable: IUnknown](imapitableiunknown.md), enquanto os provedores de serviço, dependendo se eles possuem os dados que a tabela for baseada em, podem usar qualquer um dos **IMAPITable** ou [ITableData: IUnknown](itabledataiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="07789-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="07789-110">As operações definidas nessas interfaces podem ser categorizadas como operações que todos os usuários das tabelas tenham ou podem chamar e operações que não são usadas como amplamente porque eles são mais avançados.</span><span class="sxs-lookup"><span data-stu-id="07789-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="07789-111">Algumas das operações avançadas são mais complexas de implementar; outras pessoas não mais complexas, mas são de interesse para uma pequena minoria dos componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="07789-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="07789-112">Operações mais comuns são:</span><span class="sxs-lookup"><span data-stu-id="07789-112">The more common operations are:</span></span>
  
- <span data-ttu-id="07789-113">Operações de coluna, que afetam o única colunas.</span><span class="sxs-lookup"><span data-stu-id="07789-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="07789-114">Eles incluem especificando as propriedades a serem incluídos no conjunto de colunas e a ordem em que eles devem ser incluídos.</span><span class="sxs-lookup"><span data-stu-id="07789-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="07789-115">Operações de linha, que afetam o única linhas.</span><span class="sxs-lookup"><span data-stu-id="07789-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="07789-116">Eles incluem as operações de manutenção e recuperação de dados: adição, exclusão e modificação de uma única linha ou linhas.</span><span class="sxs-lookup"><span data-stu-id="07789-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="07789-117">Operações globais, que afetam a tabela inteira.</span><span class="sxs-lookup"><span data-stu-id="07789-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="07789-118">Isso inclui a notificação de evento, pesquisa e classificação.</span><span class="sxs-lookup"><span data-stu-id="07789-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07789-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="07789-119">See also</span></span>



[<span data-ttu-id="07789-120">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="07789-120">MAPI Tables</span></span>](mapi-tables.md)

