---
title: Sobre restrições
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 003655354ecac8e2910b3e6851da32c28ce31cfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586449"
---
# <a name="about-restrictions"></a><span data-ttu-id="0cc66-103">Sobre restrições</span><span class="sxs-lookup"><span data-stu-id="0cc66-103">About Restrictions</span></span>

  
  
<span data-ttu-id="0cc66-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0cc66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0cc66-105">Uma restrição é uma maneira para limitar o número de linhas em um modo de exibição somente as linhas com valores de colunas que correspondem a critérios específicos.</span><span class="sxs-lookup"><span data-stu-id="0cc66-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="0cc66-106">Há muitas oportunidades diferentes para o uso de restrições com tabelas.</span><span class="sxs-lookup"><span data-stu-id="0cc66-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="0cc66-107">Aplicativos cliente podem usar a restrições, por exemplo, para filtrar uma tabela de conteúdo para mensagens enviadas por uma pessoa específica, para pesquisar por linhas que não oferecem suporte a uma propriedade ou tem definido uma propriedade para um valor específico ou para procurar por destinatários duplicados dentro um Mensagem.</span><span class="sxs-lookup"><span data-stu-id="0cc66-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="0cc66-108">Os métodos [IMAPITable:: Restrict](imapitable-restrict.md) e [IMAPITable:: FindRow](imapitable-findrow.md) são usados para definir restrições em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="0cc66-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="0cc66-109">**Restrict** aplica a restrição à tabela sem recuperar qualquer linha.</span><span class="sxs-lookup"><span data-stu-id="0cc66-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="0cc66-110">Para recuperar apenas aquelas que atendam a restrição de linhas, uma chamada subsequente para [IMAPITable:: QueryRows](imapitable-queryrows.md) ou um método semelhante é necessária.</span><span class="sxs-lookup"><span data-stu-id="0cc66-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="0cc66-111">**FindRow** aplica a restrição e recupera a primeira linha da tabela que corresponde aos critérios.</span><span class="sxs-lookup"><span data-stu-id="0cc66-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="0cc66-112">**FindRow** aplica uma restrição temporária, que está no existência apenas para a duração da chamada, enquanto **Restrict** aplica uma restrição mais permanente.</span><span class="sxs-lookup"><span data-stu-id="0cc66-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="0cc66-113">Alguns clientes podem construir uma restrição usando colunas não na coluna atual definidas.</span><span class="sxs-lookup"><span data-stu-id="0cc66-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="0cc66-114">Suporte de tal uma restrição é opcional e implementadores de tabela que dão suporte ao agregam valor, particularmente para tabelas de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0cc66-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="0cc66-115">Implementadores de tabela que não têm suporte podem retornar o valor MAPI_E_TOO_COMPLEX de uma chamada **Restrict** ou o valor de E_NOT_FOUND de uma chamada **FindRow** .</span><span class="sxs-lookup"><span data-stu-id="0cc66-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="0cc66-116">Os clientes devem estar cientes de que, mesmo se o provedor oferece suporte a restrições em colunas não no conjunto coluna atual, elas receberão um melhor desempenho geral, especificando as colunas que pretendem usar em suas restrições com [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="0cc66-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0cc66-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cc66-117">See also</span></span>



[<span data-ttu-id="0cc66-118">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="0cc66-118">MAPI Tables</span></span>](mapi-tables.md)

