---
title: Trabalhando com colunas de múltiplos valores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 34f19e279c86e0c0856d242cf2aa13d744d46f13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420182"
---
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="d8096-103">Trabalhando com colunas de múltiplos valores</span><span class="sxs-lookup"><span data-stu-id="d8096-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="d8096-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8096-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8096-105">Uma coluna de múltiplos valores contém os dados de uma propriedade de múltiplos valores, que é uma propriedade que tem uma matriz de valores do tipo base em vez de um único valor.</span><span class="sxs-lookup"><span data-stu-id="d8096-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="d8096-106">Como nenhuma das tabelas inclui propriedades de múltiplos valores em seus conjuntos de colunas padrão, as propriedades de valores múltiplos são incluídas em uma tabela somente se o usuário da tabela solicitar.</span><span class="sxs-lookup"><span data-stu-id="d8096-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="d8096-107">Colunas de múltiplos valores podem ser exibidas em tabelas:</span><span class="sxs-lookup"><span data-stu-id="d8096-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="d8096-108">Em uma única linha, com todos os valores de propriedade aparecendo na instância de coluna única.</span><span class="sxs-lookup"><span data-stu-id="d8096-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="d8096-109">É o padrão.</span><span class="sxs-lookup"><span data-stu-id="d8096-109">This is the default.</span></span>
    
    - <span data-ttu-id="d8096-110">Ou -</span><span class="sxs-lookup"><span data-stu-id="d8096-110">Or -</span></span>
    
- <span data-ttu-id="d8096-111">Em uma série de linhas, com uma linha para cada um dos valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d8096-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="d8096-112">Cada valor exclusivo aparece na coluna em sua própria linha, com tantas linhas quanto valores na propriedade de múltiplos valores.</span><span class="sxs-lookup"><span data-stu-id="d8096-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="d8096-113">Cada linha tem um valor exclusivo para a **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), mas os mesmos valores para as outras colunas.</span><span class="sxs-lookup"><span data-stu-id="d8096-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="d8096-114">Se uma linha contiver mais de uma coluna com vários valores, por exemplo, duas colunas com valores  _M_ e  _N_ respectivamente, as instâncias  _M \* N_ da linha aparecerão na tabela.</span><span class="sxs-lookup"><span data-stu-id="d8096-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="d8096-115">Um usuário de tabela solicita o tipo não padrão de exibição chamando o método [IMAPITable::SetColumns](imapitable-setcolumns.md) com o sinalizador MVI_FLAG definido no tipo de propriedade da coluna de vários valores.</span><span class="sxs-lookup"><span data-stu-id="d8096-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="d8096-116">O MVI_FLAG sinalizador é uma constante definida como resultado da combinação dos sinalizadores MV_FLAG e MV_INSTANCE com uma operação **OR** lógica.</span><span class="sxs-lookup"><span data-stu-id="d8096-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="d8096-117">Além de ser usado em **SetColumns**, MVI_FLAG também pode ser passado para [IMAPITable::SortTable](imapitable-sorttable.md) no parâmetro _lpSortCriteria_ e [IMAPITable::Restrict](imapitable-restrict.md) no **membro ulPropTag** do parâmetro _lpRestriction._</span><span class="sxs-lookup"><span data-stu-id="d8096-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="d8096-118">Quando passada a MVI_FLAG, **SortTable** tem um desempenho semelhante a **SetColumns**, adicionando uma linha para cada valor na coluna de vários valores e classificação nos valores individuais nas instâncias.</span><span class="sxs-lookup"><span data-stu-id="d8096-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="d8096-119">Uma linha é adicionada para cada valor.</span><span class="sxs-lookup"><span data-stu-id="d8096-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="d8096-120">**Restringir**, no entanto, não expande a coluna de múltiplos valores em linhas computadas adicionais.</span><span class="sxs-lookup"><span data-stu-id="d8096-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="d8096-121">Uma coluna de vários valores com o conjunto MVI_FLAG instrui o provedor de serviços a usar essa coluna para restringir a tabela.</span><span class="sxs-lookup"><span data-stu-id="d8096-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="d8096-122">Se houver um valor de propriedade na restrição, deverá ser uma marca de propriedade de valor único idêntica à que seria retornada por [IMAPITable::QueryRows](imapitable-queryrows.md) para a coluna.</span><span class="sxs-lookup"><span data-stu-id="d8096-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="d8096-123">Implementadores de tabela só são necessários para dar suporte ao tipo padrão de exibição e podem retornar o valor MAPI_E_TOO_COMPLEX quando um chamador solicita a outra alternativa.</span><span class="sxs-lookup"><span data-stu-id="d8096-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="d8096-124">A capacidade de dar suporte a ambos os tipos de exibição é mais importante para provedores de armazenamento de mensagens que implementam tabelas de conteúdo de pastas.</span><span class="sxs-lookup"><span data-stu-id="d8096-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8096-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8096-125">See also</span></span>



[<span data-ttu-id="d8096-126">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="d8096-126">MAPI Tables</span></span>](mapi-tables.md)

