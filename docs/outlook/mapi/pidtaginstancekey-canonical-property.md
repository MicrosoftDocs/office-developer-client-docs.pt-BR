---
title: Propriedade canônica PidTagInstanceKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358508"
---
# <a name="pidtaginstancekey-canonical-property"></a><span data-ttu-id="32de4-103">Propriedade canônica PidTagInstanceKey</span><span class="sxs-lookup"><span data-stu-id="32de4-103">PidTagInstanceKey Canonical Property</span></span>

  
  
<span data-ttu-id="32de4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32de4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32de4-105">Contém um valor que identifica exclusivamente uma linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="32de4-105">Contains a value that uniquely identifies a row in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32de4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="32de4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="32de4-107">PR_INSTANCE_KEY</span><span class="sxs-lookup"><span data-stu-id="32de4-107">PR_INSTANCE_KEY</span></span>  <br/> |
|<span data-ttu-id="32de4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="32de4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="32de4-109">0x0FF6</span><span class="sxs-lookup"><span data-stu-id="32de4-109">0x0FF6</span></span>  <br/> |
|<span data-ttu-id="32de4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="32de4-110">Data type:</span></span>  <br/> |<span data-ttu-id="32de4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="32de4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="32de4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="32de4-112">Area:</span></span>  <br/> |<span data-ttu-id="32de4-113">Tabela</span><span class="sxs-lookup"><span data-stu-id="32de4-113">Table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32de4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="32de4-114">Remarks</span></span>

<span data-ttu-id="32de4-115">Esta propriedade é um valor binário que identifica exclusivamente uma linha em um modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="32de4-115">This property is a binary value that uniquely identifies a row in a table view.</span></span> <span data-ttu-id="32de4-116">É uma coluna obrigatória na maioria das tabelas.</span><span class="sxs-lookup"><span data-stu-id="32de4-116">It is a required column in most tables.</span></span> <span data-ttu-id="32de4-117">Se uma linha estiver incluída em dois modos de exibição, haverá duas chaves de instância diferentes.</span><span class="sxs-lookup"><span data-stu-id="32de4-117">If a row is included in two views, there are two different instance keys.</span></span> <span data-ttu-id="32de4-118">A chave de instância de uma linha pode ser diferente cada vez que a tabela é aberta, mas permanece constante enquanto a tabela está aberta.</span><span class="sxs-lookup"><span data-stu-id="32de4-118">The instance key of a row may differ each time the table is opened, but remains constant while the table is open.</span></span> <span data-ttu-id="32de4-119">Linhas adicionadas enquanto uma tabela está em uso não reutiliza uma chave de instância que foi usada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="32de4-119">Rows added while a table is in use do not reuse an instance key that was previously used.</span></span> 
  
<span data-ttu-id="32de4-120">Use as propriedades **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para correlacionar todas as linhas de uma expansão.</span><span class="sxs-lookup"><span data-stu-id="32de4-120">Use the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) properties to correlate all the rows of an expansion.</span></span> <span data-ttu-id="32de4-121">Use **PR_INSTANCE_KEY** para localizar uma instância específica dentro da expansão.</span><span class="sxs-lookup"><span data-stu-id="32de4-121">Use **PR_INSTANCE_KEY** to locate a particular instance within the expansion.</span></span> 
  
<span data-ttu-id="32de4-122">Quando uma propriedade de vários valores é expandida em uma tabela, uma linha é criada para cada instância da expansão, ou seja, para cada valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="32de4-122">When a multivalued property is expanded in a table, a row is created for each instance of the expansion, that is, for each value of that property.</span></span> <span data-ttu-id="32de4-123">Cada linha tem um valor exclusivo para a propriedade **PR_INSTANCE_KEY** , enquanto todas as outras colunas retêm seus valores originais por toda a expansão.</span><span class="sxs-lookup"><span data-stu-id="32de4-123">Each row has a unique value for the **PR_INSTANCE_KEY** property, while all the other columns retain their original values throughout the expansion.</span></span> 
  
<span data-ttu-id="32de4-124">Em uma classificação categorizada de uma tabela, as linhas não correspondentes aos dados reais podem ser adicionadas ao resultado da classificação.</span><span class="sxs-lookup"><span data-stu-id="32de4-124">In a categorized sort of a table, rows not corresponding to actual data can be added to the result of the sort.</span></span> <span data-ttu-id="32de4-125">Cada linha, como todas as linhas em todas as tabelas, tem sua própria chave de instância exclusiva.</span><span class="sxs-lookup"><span data-stu-id="32de4-125">Each such row, like all rows in all tables, has its own unique instance key.</span></span> 
  
 <span data-ttu-id="32de4-126">**PR_INSTANCE_KEY** também é usado em notificações de eventos de tabela.</span><span class="sxs-lookup"><span data-stu-id="32de4-126">**PR_INSTANCE_KEY** is also used in table event notifications.</span></span> <span data-ttu-id="32de4-127">Os membros **propIndex** e **PropPrior** da estrutura [TABLE_NOTIFICATION](table_notification.md) são [SPropValue](spropvalue.md) estruturas que contêm valores de **PR_INSTANCE_KEY** .</span><span class="sxs-lookup"><span data-stu-id="32de4-127">The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values.</span></span> <span data-ttu-id="32de4-128">O membro **propIndex** indica a linha que foi adicionada ou alterada.</span><span class="sxs-lookup"><span data-stu-id="32de4-128">The **propIndex** member indicates the row that was added or changed.</span></span> <span data-ttu-id="32de4-129">O membro **propPrior** indica a linha antes da linha adicionada ou alterada (**PR_NULL** indica uma alteração na primeira linha).</span><span class="sxs-lookup"><span data-stu-id="32de4-129">The **propPrior** member indicates the row before the added or changed row (**PR_NULL** indicates a change to the first row).</span></span> 
  
<span data-ttu-id="32de4-130">Esse valor não é copiado como parte da tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="32de4-130">This value is not copied as part of the display table.</span></span> 
  
 <span data-ttu-id="32de4-131">**PR_INSTANCE_KEY** é uma estrutura [MAPIUID](mapiuid.md) .</span><span class="sxs-lookup"><span data-stu-id="32de4-131">**PR_INSTANCE_KEY** is a [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="32de4-132">Todas as chaves de instância podem ser diretamente comparadas como valores binários.</span><span class="sxs-lookup"><span data-stu-id="32de4-132">All instance keys can be directly compared as binary values.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="32de4-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="32de4-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="32de4-134">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="32de4-134">Protocol specifications</span></span>

<span data-ttu-id="32de4-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32de4-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32de4-136">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="32de4-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="32de4-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32de4-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32de4-138">Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="32de4-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="32de4-139">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="32de4-139">Header files</span></span>

<span data-ttu-id="32de4-140">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="32de4-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="32de4-141">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="32de4-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="32de4-142">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="32de4-142">Mapitags.h</span></span>
  
> <span data-ttu-id="32de4-143">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="32de4-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32de4-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="32de4-144">See also</span></span>



[<span data-ttu-id="32de4-145">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="32de4-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="32de4-146">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="32de4-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="32de4-147">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="32de4-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="32de4-148">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="32de4-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

