---
title: Sobre restrições
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433105"
---
# <a name="about-restrictions"></a><span data-ttu-id="55ddd-103">Sobre restrições</span><span class="sxs-lookup"><span data-stu-id="55ddd-103">About Restrictions</span></span>

  
  
<span data-ttu-id="55ddd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55ddd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55ddd-105">Uma restrição é uma maneira de limitar o número de linhas em um modo de exibição apenas às linhas com valores para colunas que correspondem a critérios específicos.</span><span class="sxs-lookup"><span data-stu-id="55ddd-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="55ddd-106">Há várias oportunidades diferentes de usar restrições com tabelas.</span><span class="sxs-lookup"><span data-stu-id="55ddd-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="55ddd-107">Os aplicativos cliente podem usar restrições, por exemplo, para filtrar uma tabela de conteúdo para mensagens enviadas por uma determinada pessoa, procurar linhas que não dão suporte a uma propriedade ou definir uma propriedade para um valor específico ou procurar destinatários duplicados em um Mensagem.</span><span class="sxs-lookup"><span data-stu-id="55ddd-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="55ddd-108">Os métodos imApitable: [: Restrict](imapitable-restrict.md) e IMAPITable [:: FindRow](imapitable-findrow.md) são usados para definir restrições em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="55ddd-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="55ddd-109">**Restrict** aplica a restrição à tabela sem recuperar nenhuma linha.</span><span class="sxs-lookup"><span data-stu-id="55ddd-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="55ddd-110">Para recuperar apenas as linhas que atendem à restrição, uma chamada subsequente para imApitable [:: QueryRows](imapitable-queryrows.md) ou um método semelhante é necessária.</span><span class="sxs-lookup"><span data-stu-id="55ddd-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="55ddd-111">**FindRow** aplica a restrição e recupera a primeira linha na tabela que corresponde aos critérios.</span><span class="sxs-lookup"><span data-stu-id="55ddd-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="55ddd-112">**FindRow** aplica uma restrição temporária, que está em existência somente pela duração da chamada, enquanto restrict \*\*\*\* aplica uma restrição mais permanente.</span><span class="sxs-lookup"><span data-stu-id="55ddd-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="55ddd-113">Alguns clientes podem criar uma restrição usando colunas que não estão no conjunto de colunas atual.</span><span class="sxs-lookup"><span data-stu-id="55ddd-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="55ddd-114">O suporte a uma restrição é opcional e os implementadores de tabela que suportam o valor agregado, especialmente para tabelas de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="55ddd-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="55ddd-115">Os implementadores de tabela que não oferecem suporte a ele podem retornar o valor MAPI_E_TOO_COMPLEX de uma chamada **restrita** ou o valor de MAPI_E_NOT_FOUND de uma chamada **FindRow** .</span><span class="sxs-lookup"><span data-stu-id="55ddd-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="55ddd-116">Os clientes devem estar cientes de que, mesmo que o provedor não tenha restrições de suporte em colunas que não estejam no conjunto de colunas atual, eles terão um desempenho melhor, especificando as colunas que pretendem usar em suas restrições com imApitable [::](imapitable-setcolumns.md) SetColumns .</span><span class="sxs-lookup"><span data-stu-id="55ddd-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="55ddd-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="55ddd-117">See also</span></span>



[<span data-ttu-id="55ddd-118">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="55ddd-118">MAPI Tables</span></span>](mapi-tables.md)

