---
title: Dicas para trabalhar com tabelas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439734"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="c1e83-103">Dicas para trabalhar com tabelas</span><span class="sxs-lookup"><span data-stu-id="c1e83-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="c1e83-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1e83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1e83-105">Trabalhar com uma tabela MAPI é um pouco como trabalhar com uma tabela de banco de dados relacional.</span><span class="sxs-lookup"><span data-stu-id="c1e83-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="c1e83-106">Um usuário pode limitar o número de linhas e colunas no modo de exibição e especificar sua ordem.</span><span class="sxs-lookup"><span data-stu-id="c1e83-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="c1e83-107">As linhas podem ser recuperadas uma por vez ou em grupos.</span><span class="sxs-lookup"><span data-stu-id="c1e83-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="c1e83-108">Um cursor que mantém o controle da posição atual pode ser movido para um local específico na tabela.</span><span class="sxs-lookup"><span data-stu-id="c1e83-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="c1e83-109">Para trabalhar com tabelas, os clientes usam a interface somente leitura, [IMAPITable: IUnknown](imapitableiunknown.md), enquanto os provedores de serviços, dependendo se eles possuem os dados nos quais a tabela se baseia, podem \*\*\*\* usar IMAPITable ou [ITableData: IUnknown](itabledataiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c1e83-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="c1e83-110">As operações definidas nessas interfaces podem ser categorizadas como operações que todos os usuários das tabelas fazem ou podem invocar e operações que não são tão amplamente usadas porque são mais avançadas.</span><span class="sxs-lookup"><span data-stu-id="c1e83-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="c1e83-111">Algumas das operações avançadas são mais complexas de implementar; outras não são mais complexas, mas são de interesse de uma pequena minoria dos componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1e83-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="c1e83-112">As operações mais comuns são:</span><span class="sxs-lookup"><span data-stu-id="c1e83-112">The more common operations are:</span></span>
  
- <span data-ttu-id="c1e83-113">Operações de coluna, que afetam colunas únicas.</span><span class="sxs-lookup"><span data-stu-id="c1e83-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="c1e83-114">Eles incluem a especificação das propriedades a serem incluídas no conjunto de colunas e a ordem em que devem ser incluídas.</span><span class="sxs-lookup"><span data-stu-id="c1e83-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="c1e83-115">Operações de linha, que afetam linhas únicas.</span><span class="sxs-lookup"><span data-stu-id="c1e83-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="c1e83-116">Isso inclui a recuperação de dados e as operações de manutenção: adição, exclusão e modificação de uma única linha ou linhas.</span><span class="sxs-lookup"><span data-stu-id="c1e83-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="c1e83-117">Operações globais, que afetam a tabela inteira.</span><span class="sxs-lookup"><span data-stu-id="c1e83-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="c1e83-118">Isso inclui notificação de evento, pesquisa e classificação.</span><span class="sxs-lookup"><span data-stu-id="c1e83-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1e83-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1e83-119">See also</span></span>



[<span data-ttu-id="c1e83-120">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="c1e83-120">MAPI Tables</span></span>](mapi-tables.md)

