---
title: Trabalhar com colunas grandes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9ca3c5e7a0d1b4a6ac09dcfcc7db10ec76ecb224
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325778"
---
# <a name="working-with-large-columns"></a><span data-ttu-id="cada6-103">Trabalhar com colunas grandes</span><span class="sxs-lookup"><span data-stu-id="cada6-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="cada6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cada6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cada6-105">Colunas com dados de propriedades binárias ou cadeias de caracteres podem ser grandes, possivelmente muitos milhares de bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="cada6-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="cada6-106">Como a inclusão de uma ou mais colunas com centenas de bytes em um modo de exibição é geralmente impraticável, a MAPI permite que os implementadores de tabela truncar o valor, com mais frequência de 255 bytes e menos vezes para 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="cada6-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="cada6-107">Sempre que possível, os implementadores de tabela devem incluir o valor total de uma propriedade em uma coluna de tabela.</span><span class="sxs-lookup"><span data-stu-id="cada6-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="cada6-108">A alternativa recomendada é incluir somente os primeiros 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="cada6-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="cada6-109">Os clientes não podem saber com antecedência se uma tabela que está usando trunca colunas grandes.</span><span class="sxs-lookup"><span data-stu-id="cada6-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="cada6-110">Eles devem assumir que uma coluna representa uma propriedade truncada se o comprimento da coluna for 255 ou 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="cada6-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="cada6-111">Se necessário, os clientes podem recuperar diretamente o valor completo de uma coluna truncada do objeto chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps do objeto.</span><span class="sxs-lookup"><span data-stu-id="cada6-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="cada6-112">Os clientes que têm restrições de criação com propriedades grandes devem estar cientes de que ele está no implementador de tabelas e como essas restrições operam.</span><span class="sxs-lookup"><span data-stu-id="cada6-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="cada6-113">Alguns implementadores de tabela permitem que as restrições criadas com uma coluna truncada sejam baseadas no tamanho truncado enquanto outras a baseiam em todo o valor.</span><span class="sxs-lookup"><span data-stu-id="cada6-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cada6-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="cada6-114">See also</span></span>



[<span data-ttu-id="cada6-115">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="cada6-115">MAPI Tables</span></span>](mapi-tables.md)

