---
title: Trabalhar com colunas com vários valores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ee3307836e8b167efbc2cdc870e698257526ef97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770735"
---
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="f49c6-103">Trabalhar com colunas com vários valores</span><span class="sxs-lookup"><span data-stu-id="f49c6-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="f49c6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f49c6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f49c6-105">Uma coluna de valores múltiplos contém os dados de uma propriedade de vários valores, que é uma propriedade que tem uma matriz de valores do tipo base, em vez de um único valor.</span><span class="sxs-lookup"><span data-stu-id="f49c6-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="f49c6-106">Porque nenhuma das tabelas inclui vários valores de propriedades em seus conjuntos de coluna padrão, vários valores de propriedades são incluídas em uma tabela somente se solicitado pelo usuário da tabela.</span><span class="sxs-lookup"><span data-stu-id="f49c6-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="f49c6-107">Colunas de valores múltiplos podem ser exibidas nas tabelas:</span><span class="sxs-lookup"><span data-stu-id="f49c6-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="f49c6-108">Em uma única linha, com todos os valores de propriedade que aparecem na instância única coluna.</span><span class="sxs-lookup"><span data-stu-id="f49c6-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="f49c6-109">Este é o padrão.</span><span class="sxs-lookup"><span data-stu-id="f49c6-109">This is the default.</span></span>
    
    - <span data-ttu-id="f49c6-110">Ou -</span><span class="sxs-lookup"><span data-stu-id="f49c6-110">Or -</span></span>
    
- <span data-ttu-id="f49c6-111">Em uma série de linhas, com uma linha para cada um dos valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f49c6-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="f49c6-112">Cada valor exclusivo aparece na coluna na sua própria linha com daí sendo conforme o número de linhas daí é valores na propriedade multivalorado.</span><span class="sxs-lookup"><span data-stu-id="f49c6-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="f49c6-113">Cada linha tem um valor exclusivo para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), mas os mesmos valores para as outras colunas.</span><span class="sxs-lookup"><span data-stu-id="f49c6-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="f49c6-114">Se uma linha contiver mais de uma coluna com vários valores, por exemplo, duas colunas com _M_ e _N_ valores respectivamente, em seguida, _M\*N_ instâncias da linha aparecem na tabela.</span><span class="sxs-lookup"><span data-stu-id="f49c6-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="f49c6-115">Um usuário de tabela solicita o tipo de fora do padrão de exibição chamando o método [IMAPITable::SetColumns](imapitable-setcolumns.md) com o sinalizador MVI_FLAG definido no tipo de propriedade da coluna de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="f49c6-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="f49c6-116">O sinalizador MVI_FLAG é uma constante definida como resultado de combinar os sinalizadores MV_FLAG e MV_INSTANCE com uma operação **OR** lógica.</span><span class="sxs-lookup"><span data-stu-id="f49c6-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="f49c6-117">Além do que está sendo usado em **SetColumns**, MVI_FLAG pode também ser passado para [IMAPITable:: SortTable](imapitable-sorttable.md) no parâmetro _lpSortCriteria_ and [IMAPITable:: Restrict](imapitable-restrict.md) no membro **ulPropTag** a _lpRestriction_ Use o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f49c6-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="f49c6-118">Quando passado a MVI_FLAG, **SortTable** da mesma forma realiza a **SetColumns**, adicionando uma linha para cada valor na coluna multivalorada e classificação nos valores único nas instâncias.</span><span class="sxs-lookup"><span data-stu-id="f49c6-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="f49c6-119">Uma linha é adicionada para cada valor.</span><span class="sxs-lookup"><span data-stu-id="f49c6-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="f49c6-120">**Restrict**, no entanto, não expandir a coluna de valores múltiplos em linhas computadas adicionais.</span><span class="sxs-lookup"><span data-stu-id="f49c6-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="f49c6-121">Uma coluna de valores múltiplos com o conjunto de MVI_FLAG instrui o provedor de serviços para usar essa coluna na restringindo a tabela.</span><span class="sxs-lookup"><span data-stu-id="f49c6-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="f49c6-122">Se houver um valor de propriedade na restrição, ele deve ser uma marca de propriedade de valor único idêntica ao que seria retornada pela [IMAPITable:: QueryRows](imapitable-queryrows.md) da coluna.</span><span class="sxs-lookup"><span data-stu-id="f49c6-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="f49c6-123">Implementadores de tabela apenas requeridos para suportar o tipo de padrão de exibição e podem retornar o valor MAPI_E_TOO_COMPLEX quando um chamador solicita a outra alternativa.</span><span class="sxs-lookup"><span data-stu-id="f49c6-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="f49c6-124">A capacidade de suportar os dois tipos de exibição é mais importante para a implementação de tabelas de conteúdo de pasta de provedores de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f49c6-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f49c6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f49c6-125">See also</span></span>



[<span data-ttu-id="f49c6-126">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="f49c6-126">MAPI Tables</span></span>](mapi-tables.md)

