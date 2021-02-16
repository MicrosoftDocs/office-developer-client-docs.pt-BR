---
title: Definindo uma posição de tabela com um filtro
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425467"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="a8c68-103">Definindo uma posição de tabela com um filtro</span><span class="sxs-lookup"><span data-stu-id="a8c68-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="a8c68-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8c68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8c68-105">Os usuários da tabela podem mover o cursor para uma linha que corresponde a um conjunto de critérios de filtro.</span><span class="sxs-lookup"><span data-stu-id="a8c68-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="a8c68-106">Os filtros podem ser baseados em uma variedade de diretrizes, como valores de propriedade de coluna, bitmasks ou subobjetos.</span><span class="sxs-lookup"><span data-stu-id="a8c68-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="a8c68-107">Os filtros são especificados em MAPI usando [uma estrutura SRestriction.](srestriction.md)</span><span class="sxs-lookup"><span data-stu-id="a8c68-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="a8c68-108">**Para posicionar uma tabela na primeira linha que corresponde aos critérios estabelecidos em uma restrição**</span><span class="sxs-lookup"><span data-stu-id="a8c68-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="a8c68-109">Chame o [método IMAPITable::FindRow.](imapitable-findrow.md)</span><span class="sxs-lookup"><span data-stu-id="a8c68-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="a8c68-110">Começando com a linha representada por um indicador específico, **FindRow** pesquisa em uma direção para frente ou para trás para localizar uma linha que corresponde aos critérios especificados na restrição.</span><span class="sxs-lookup"><span data-stu-id="a8c68-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="a8c68-111">**FindRow** pode ser útil para implementar uma barra de rolagem baseada em cadeias de caracteres, em vez de valores fracionais.</span><span class="sxs-lookup"><span data-stu-id="a8c68-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="a8c68-112">Por exemplo, um cliente pode chamar a implementação de **FindRow** de MAPI ao pesquisar o livro de endereços integrado para habilitar um usuário, inserindo um ou mais caracteres, para localizar o primeiro nome que começa com os caracteres especificados.</span><span class="sxs-lookup"><span data-stu-id="a8c68-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a8c68-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8c68-113">See also</span></span>



[<span data-ttu-id="a8c68-114">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c68-114">MAPI Tables</span></span>](mapi-tables.md)

