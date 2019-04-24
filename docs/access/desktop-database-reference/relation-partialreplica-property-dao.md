---
title: Propriedade relation. PartialReplica (DAO)
TOCTitle: PartialReplica Property
ms:assetid: 3cb15639-371e-06e3-e2ba-30466ce09a72
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192692(v=office.15)
ms:contentKeyID: 48544324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053557
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fef48902b806f13947ae4b81728af4c5704c2b8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307011"
---
# <a name="relationpartialreplica-property-dao"></a><span data-ttu-id="34fa7-102">Propriedade relation. PartialReplica (DAO)</span><span class="sxs-lookup"><span data-stu-id="34fa7-102">Relation.PartialReplica property (DAO)</span></span>

<span data-ttu-id="34fa7-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34fa7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34fa7-p101">Define ou retorna um valor em um objeto **Relation**, indicando se essa relação deverá ser considerada durante o preenchimento de uma réplica parcial a partir de uma réplica completa. (somente em banco de dados do mecanismo de banco de dados do Microsoft Access). **Boolean** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="34fa7-p101">Sets or returns a value on a **Relation** object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="34fa7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34fa7-107">Syntax</span></span>

<span data-ttu-id="34fa7-108">*expressão* . PartialReplica</span><span class="sxs-lookup"><span data-stu-id="34fa7-108">*expression* .PartialReplica</span></span>

<span data-ttu-id="34fa7-109">*expressão* Uma expressão que retorna um objeto **relation** .</span><span class="sxs-lookup"><span data-stu-id="34fa7-109">*expression* An expression that returns a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="34fa7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="34fa7-110">Remarks</span></span>

<span data-ttu-id="34fa7-111">A configuração ou o valor de retorno é um tipo de dados Boolean que será **True** quando a relação for imposta durante a sincronização.</span><span class="sxs-lookup"><span data-stu-id="34fa7-111">The setting or return value is a Boolean data type that is **True** when the relation should be enforced during synchronization.</span></span>

<span data-ttu-id="34fa7-112">Essa propriedade permite replicar os dados da réplica completa para a réplica parcial com base nas relações entre as tabelas.</span><span class="sxs-lookup"><span data-stu-id="34fa7-112">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables.</span></span> <span data-ttu-id="34fa7-113">Use a propriedade **PartialReplica** quando apenas a definição da propriedade **ReplicaFilter** não especificar de forma adequada quais dados deverão ser replicados para a réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="34fa7-113">You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial.</span></span> <span data-ttu-id="34fa7-114">Por exemplo, suponha que você tenha um banco de dados no qual a tabela Clientes possui uma relação um-para-muitos com a tabela Pedidos e que você queira configurar uma réplica parcial que replique apenas os pedidos dos clientes da região da Califórnia (em vez de todos os pedidos).</span><span class="sxs-lookup"><span data-stu-id="34fa7-114">For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders).</span></span> <span data-ttu-id="34fa7-115">Não é possível definir a propriedade **ReplicaFilter** na tabela Pedidos como Region = 'CA', porque o campo Região está na tabela Clientes e não na tabela Pedidos.</span><span class="sxs-lookup"><span data-stu-id="34fa7-115">It is not possible to set the **ReplicaFilter** property on the Orders table to Region = 'CA' because the Region field is in the Customers table, not the Orders table.</span></span>

<span data-ttu-id="34fa7-p103">Para replicar todos os pedidos da região da Califórnia, indique se a relação entre as tabelas Pedidos e Clientes estará ativa durante a replicação. Assim que você tiver criado uma réplica parcial, as próximas etapas serão preenchidas com todos os pedidos da região da Califórnia:</span><span class="sxs-lookup"><span data-stu-id="34fa7-p103">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication. Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span></span>

1.  <span data-ttu-id="34fa7-118">Defina a propriedade **ReplicaFilter** no objeto **TableDef** dos clientes como "Region =" AC "".</span><span class="sxs-lookup"><span data-stu-id="34fa7-118">Set the **ReplicaFilter** property on the Customers **TableDef** object to "Region = 'CA'".</span></span>

2.  <span data-ttu-id="34fa7-119">Defina o valor da propriedade **PartialReplica** como **True** no objeto **Relation**, que corresponde à relação entre Pedidos e Clientes.</span><span class="sxs-lookup"><span data-stu-id="34fa7-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span></span>

3.  <span data-ttu-id="34fa7-120">Chame o método **PopulatePartial**.</span><span class="sxs-lookup"><span data-stu-id="34fa7-120">Invoke the **PopulatePartial** method.</span></span>
    

> [!NOTE]
> <span data-ttu-id="34fa7-121">[!OBSERVAçãO] Quando você definir um filtro para réplica ou uma relação de réplicas, esteja ciente de que os registros da réplica parcial que não satisfizerem os critérios de restrição serão removidos da réplica parcial, mas não da réplica completa.</span><span class="sxs-lookup"><span data-stu-id="34fa7-121">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica.</span></span> <span data-ttu-id="34fa7-122">Por exemplo, suponha que você tenha definido a propriedade **ReplicaFilter** em **TableDef** de Clientes na réplica parcial como "Region = 'CA'" e depois tenha preenchido novamente o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="34fa7-122">For example, suppose you set the **ReplicaFilter** property on the Customers **TableDef** in the partial replica to "Region = 'CA'" and you then repopulate the database.</span></span> <span data-ttu-id="34fa7-123">Isso inserirá ou atualizará todos os registros dos clientes da Califórnia.</span><span class="sxs-lookup"><span data-stu-id="34fa7-123">This will insert or update all records for California-based customers.</span></span> 
> 
> <span data-ttu-id="34fa7-124">Se você redefinir depois a propriedade **ReplicaFilter** como "Region = 'FL'" e preencher novamente o banco de dados, todos os registros da região da Califórnia na réplica parcial serão removidos e todos os registros dos clientes da Flórida serão inseridos na réplica completa.</span><span class="sxs-lookup"><span data-stu-id="34fa7-124">If you then reset the **ReplicaFilter** property to "Region = 'FL'" and repopulate the database, all California region records in the partial replica will be removed, and all records from Florida-based customers will be inserted from the full replica.</span></span> <span data-ttu-id="34fa7-125">Nenhum registro será excluído da réplica completa.</span><span class="sxs-lookup"><span data-stu-id="34fa7-125">No records in the full replica will be deleted.</span></span> 
>
> <span data-ttu-id="34fa7-126">Antes de definir a propriedade **ReplicaFilter** ou a propriedade **PartialReplica**, é uma boa ideia sincronizar a réplica parcial na qual você está definindo essas propriedades na réplica completa.</span><span class="sxs-lookup"><span data-stu-id="34fa7-126">Before setting either the **ReplicaFilter** or **PartialReplica** property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica.</span></span> <span data-ttu-id="34fa7-127">Isso garantirá que as alterações pendentes na réplica parcial serão mescladas na réplica completa antes de quaisquer registros serem removidos da réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="34fa7-127">This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span></span>


