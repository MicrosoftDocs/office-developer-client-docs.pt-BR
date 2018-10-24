---
title: Definir uma posição de tabela com um filtro
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6c4db9c67fc712143657fe66b86ea33ef2b9c272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565589"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="08977-103">Definir uma posição de tabela com um filtro</span><span class="sxs-lookup"><span data-stu-id="08977-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="08977-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08977-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08977-105">Os usuários da tabela podem mover o cursor para uma linha que corresponde a um conjunto de critérios de filtro.</span><span class="sxs-lookup"><span data-stu-id="08977-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="08977-106">Filtros podem ser baseados em uma variedade de diretrizes como valores de propriedade de coluna, bitmasks ou subobjetos.</span><span class="sxs-lookup"><span data-stu-id="08977-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="08977-107">Filtros são especificados em MAPI usando uma estrutura [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="08977-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="08977-108">**Para posicionar uma tabela à primeira linha que corresponde aos critérios estabelecidos em uma restrição**</span><span class="sxs-lookup"><span data-stu-id="08977-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="08977-109">Chame o método [IMAPITable:: FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="08977-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="08977-110">Começando com a linha representada por um determinado indicador, **FindRow** procura em uma direção frente ou para trás para localizar uma linha que corresponde aos critérios especificados na restrição.</span><span class="sxs-lookup"><span data-stu-id="08977-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="08977-111">**FindRow** pode ser útil para implementar uma barra de rolagem que se baseia em cadeias de caracteres, em vez de valores fracionários.</span><span class="sxs-lookup"><span data-stu-id="08977-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="08977-112">Por exemplo, um cliente pode chamar a implementação do MAPI do **FindRow** ao pesquisar o catálogo de endereços integrado para habilitar um usuário, inserindo um ou mais caracteres, para localizar o primeiro nome que começa com os caracteres especificados.</span><span class="sxs-lookup"><span data-stu-id="08977-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="08977-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="08977-113">See also</span></span>



[<span data-ttu-id="08977-114">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="08977-114">MAPI Tables</span></span>](mapi-tables.md)

