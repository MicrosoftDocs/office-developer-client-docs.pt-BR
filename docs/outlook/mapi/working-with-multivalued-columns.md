---
title: Trabalhar com colunas com vários valores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 34f19e279c86e0c0856d242cf2aa13d744d46f13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325799"
---
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="f334d-103">Trabalhar com colunas com vários valores</span><span class="sxs-lookup"><span data-stu-id="f334d-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="f334d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f334d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f334d-105">Uma coluna com vários valores contém os dados de uma propriedade com vários valores, que é uma propriedade que tem uma matriz de valores do tipo base em vez de um único valor.</span><span class="sxs-lookup"><span data-stu-id="f334d-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="f334d-106">Como nenhuma das tabelas inclui propriedades com vários valores em seus conjuntos de colunas padrão, as propriedades com vários valores serão incluídas em uma tabela somente se o usuário da tabela a solicitar.</span><span class="sxs-lookup"><span data-stu-id="f334d-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="f334d-107">Colunas com vários valores podem ser exibidas em tabelas:</span><span class="sxs-lookup"><span data-stu-id="f334d-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="f334d-108">Em uma única linha, com todos os valores de propriedade que aparecem na instância de coluna única.</span><span class="sxs-lookup"><span data-stu-id="f334d-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="f334d-109">Este é o padrão.</span><span class="sxs-lookup"><span data-stu-id="f334d-109">This is the default.</span></span>
    
    - <span data-ttu-id="f334d-110">Ou</span><span class="sxs-lookup"><span data-stu-id="f334d-110">Or -</span></span>
    
- <span data-ttu-id="f334d-111">Em uma série de linhas, com uma linha para cada valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f334d-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="f334d-112">Cada valor exclusivo é exibido na coluna em sua própria linha, com o mesmo número de linhas que há valores na propriedade multivalued.</span><span class="sxs-lookup"><span data-stu-id="f334d-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="f334d-113">Cada linha tem um valor exclusivo para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), mas os mesmos valores para as outras colunas.</span><span class="sxs-lookup"><span data-stu-id="f334d-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="f334d-114">Se uma linha contiver mais de uma coluna com vários valores, por exemplo, duas colunas com valores _M_ e _N_ respectivamente, _M\*N_ instâncias da linha aparecerão na tabela.</span><span class="sxs-lookup"><span data-stu-id="f334d-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="f334d-115">Um usuário de tabela solicita o tipo de exibição não padrão chamando o método imApitable [::](imapitable-setcolumns.md) SetColumns com o sinalizador MVI_FLAG definido no tipo de propriedade da coluna de vários valores.</span><span class="sxs-lookup"><span data-stu-id="f334d-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="f334d-116">O sinalizador MVI_FLAG é uma constante definida como resultado da combinação dos sinalizadores MV_FLAG e MV_INSTANCE com uma operação **ou** lógica.</span><span class="sxs-lookup"><span data-stu-id="f334d-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="f334d-117">Além de ser usado em setColumns, MVI_FLAG também pode ser passado para imApitable [:: SortTable](imapitable-sorttable.md) no _parâmetro LpSortCriteria_ e [IMAPITable:](imapitable-restrict.md) : Restrict no membro **ulPropTag** do _lpRestriction_ \*\*\*\* Construtor.</span><span class="sxs-lookup"><span data-stu-id="f334d-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="f334d-118">Quando passamos o MVI_FLAG \*\*\*\* , SortTable é executado de forma semelhante a SetColumns, adicionando uma linha para cada valor na coluna de vários valores e classificando os valores únicos nas instâncias. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f334d-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="f334d-119">Uma linha é adicionada para cada valor.</span><span class="sxs-lookup"><span data-stu-id="f334d-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="f334d-120">No entanto, a **restrição**não expande a coluna de vários valores em linhas computadas adicionais.</span><span class="sxs-lookup"><span data-stu-id="f334d-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="f334d-121">Uma coluna com vários valores com o conjunto MVI_FLAG instrui o provedor de serviços a usar essa coluna ao restringir a tabela.</span><span class="sxs-lookup"><span data-stu-id="f334d-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="f334d-122">Se houver um valor de propriedade na restrição, ele deve ser uma marca de propriedade de valor único idêntica à que seria retornada por imApitable [:: QueryRows](imapitable-queryrows.md) para a coluna.</span><span class="sxs-lookup"><span data-stu-id="f334d-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="f334d-123">Os implementadores de tabela são necessários apenas para suportar o tipo de exibição padrão e podem retornar o valor MAPI_E_TOO_COMPLEX quando um chamador solicita a outra alternativa.</span><span class="sxs-lookup"><span data-stu-id="f334d-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="f334d-124">A capacidade de suportar ambos os tipos de exibição é mais importante para os provedores de repositório de mensagens que estão implementando tabelas de conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="f334d-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f334d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f334d-125">See also</span></span>



[<span data-ttu-id="f334d-126">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="f334d-126">MAPI Tables</span></span>](mapi-tables.md)

