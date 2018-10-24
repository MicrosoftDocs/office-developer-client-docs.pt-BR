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
ms.openlocfilehash: 11007fa18a57e296472c28f86480cb71b780e568
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593029"
---
# <a name="working-with-large-columns"></a><span data-ttu-id="7607b-103">Trabalhar com colunas grandes</span><span class="sxs-lookup"><span data-stu-id="7607b-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="7607b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7607b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7607b-105">Colunas com dados de propriedade de cadeia de caracteres ou binário podem ser grandes, possivelmente muitos milhares de bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="7607b-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="7607b-106">Porque geralmente é impraticável incluindo uma ou mais colunas com centenas de bytes em um modo de exibição, MAPI permite implementadores de tabela truncar o valor com mais frequência para 255 bytes e com menos frequência 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="7607b-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="7607b-107">Sempre que possível, implementadores de tabela devem incluir o valor completo de uma propriedade em uma coluna de tabela.</span><span class="sxs-lookup"><span data-stu-id="7607b-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="7607b-108">A alternativa recomendada é incluir apenas os primeiros 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="7607b-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="7607b-109">Os clientes não podem souber com antecedência se uma tabela que estejam usando trunca colunas grandes.</span><span class="sxs-lookup"><span data-stu-id="7607b-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="7607b-110">Eles devem supõem que uma coluna representa uma propriedade truncada se o comprimento da coluna é 255 ou 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="7607b-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="7607b-111">Se necessário, os clientes podem diretamente recuperar o valor completo de uma coluna truncado do objeto chamando o método do objeto [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="7607b-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="7607b-112">Clientes criando restrições com propriedades de grandes devem estar cientes de que ele esteja o implementador tabela como para como essas restrições operar.</span><span class="sxs-lookup"><span data-stu-id="7607b-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="7607b-113">Alguns implementadores de tabela permitem que as restrições que são compiladas com uma coluna truncada se baseie no tamanho truncado, enquanto outros baseá-lo em todo o valor.</span><span class="sxs-lookup"><span data-stu-id="7607b-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7607b-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="7607b-114">See also</span></span>



[<span data-ttu-id="7607b-115">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="7607b-115">MAPI Tables</span></span>](mapi-tables.md)

