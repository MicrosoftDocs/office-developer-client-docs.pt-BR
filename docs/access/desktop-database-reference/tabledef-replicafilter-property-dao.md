---
title: Propriedade TableDef.ReplicaFilter (DAO)
TOCTitle: ReplicaFilter Property
ms:assetid: f44273de-2b6a-750f-cb7c-12c3ac2da503
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836681(v=office.15)
ms:contentKeyID: 48548683
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055548
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a5cc7394b01dcd79d17e3fcc7568bb8081ee12ce
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872638"
---
# <a name="tabledefreplicafilter-property-dao"></a><span data-ttu-id="bf141-102">Propriedade TableDef.ReplicaFilter (DAO)</span><span class="sxs-lookup"><span data-stu-id="bf141-102">TableDef.ReplicaFilter Property (DAO)</span></span>


<span data-ttu-id="bf141-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf141-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf141-p101">Define ou retorna um valor em um objeto **[TableDef](tabledef-object-dao.md)** em uma réplica parcial que indica qual subconjunto de registros foi replicado nessa tabela a partir de uma réplica completa. (Somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bf141-p101">Sets or returns a value on a **[TableDef](tabledef-object-dao.md)** object within a partial replica that indicates which subset of records is replicated to that table from a full replica. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf141-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf141-106">Syntax</span></span>

<span data-ttu-id="bf141-107">*expressão* . ReplicaFilter</span><span class="sxs-lookup"><span data-stu-id="bf141-107">*expression* .ReplicaFilter</span></span>

<span data-ttu-id="bf141-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="bf141-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf141-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf141-109">Remarks</span></span>

<span data-ttu-id="bf141-110">A configuração ou o valor de retorno é um **String** ou **Boolean** que indica qual subconjunto de registros foi replicado, conforme especificado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="bf141-110">The setting or return value is a **String** or **Boolean** that indicates which subset of records is replicated, as specified in the following table:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf141-111">Valor</span><span class="sxs-lookup"><span data-stu-id="bf141-111">Value</span></span></p></th>
<th><p><span data-ttu-id="bf141-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf141-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf141-113">String</span><span class="sxs-lookup"><span data-stu-id="bf141-113">A string</span></span></p></td>
<td><p><span data-ttu-id="bf141-114">Os critérios aos quais um registro em uma tabela de réplicas parciais deve atender para ser replicado a partir de uma réplica completa.</span><span class="sxs-lookup"><span data-stu-id="bf141-114">A criteria that a record in the partial replica table must satisfy in order to be replicated from the full replica.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf141-115"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="bf141-115"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="bf141-116">Replica todos os registros.</span><span class="sxs-lookup"><span data-stu-id="bf141-116">Replicates all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf141-117"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="bf141-117"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="bf141-118">(Padrão) Não replica registros.</span><span class="sxs-lookup"><span data-stu-id="bf141-118">(Default) Doesn't replicate any records.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf141-119">Essa propriedade é semelhante à cláusula SQL WHERE (sem a palavra WHERE), mas não será possível especificar subconsultas, funções agregadas (como **Count**) ou funções definidas pelo usuário dentro dos critérios.</span><span class="sxs-lookup"><span data-stu-id="bf141-119">This property is similar to an SQL WHERE clause (without the word WHERE), but you cannot specify subqueries, aggregate functions (such as **Count**), or user-defined functions within the criteria.</span></span>

<span data-ttu-id="bf141-p102">Você pode sincronizar os dados apenas entre uma réplica completa e uma réplica parcial. Não é possível sincronizar dados entre duas réplicas parciais. Além disso, com uma replicação parcial, você pode definir as restrições nos registros que serão replicados, mas não pode indicar quais campos serão replicados.</span><span class="sxs-lookup"><span data-stu-id="bf141-p102">You can only synchronize data between a full replica and a partial replica. You can't synchronize data between two partial replicas. Also, with partial replication you can set restrictions on which records are replicated, but you can't indicate which fields are replicated.</span></span>

<span data-ttu-id="bf141-p103">Geralmente, você redefinirá um filtro para réplica quando quiser replicar um conjunto de registros diferentes. Por exemplo, quando um representante de vendas assumir temporariamente o controle da região de outros representantes de vendas, o aplicativo do banco de dados poderá replicar temporariamente os dados de ambas as regiões e mais tarde retornar para o filtro anterior. Neste cenário, o aplicativo redefinirá a propriedade **ReplicaFilter** e depois preencherá novamente a réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="bf141-p103">Usually, you reset a replica filter when you want to replicate a different set of records. For example, when a sales representative temporarily takes over another sales representative's region, the database application can temporarily replicate data for both regions and then return to the previous filter. In this scenario, the application resets the **ReplicaFilter** property and then repopulates the partial replica.</span></span>

<span data-ttu-id="bf141-126">Se o aplicativo alterar os filtros das réplicas, você deverá seguir estas etapas:</span><span class="sxs-lookup"><span data-stu-id="bf141-126">If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="bf141-127">Use o método **[Synchronize](database-synchronize-method-dao.md)** para sincronizar a réplica completa com a réplica parcial a partir da qual os filtros estão sendo alterados.</span><span class="sxs-lookup"><span data-stu-id="bf141-127">Use the **[Synchronize](database-synchronize-method-dao.md)** method to synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="bf141-128">Use a propriedade **ReplicaFilter** para fazer as alterações desejadas no filtro para réplica.</span><span class="sxs-lookup"><span data-stu-id="bf141-128">Use the **ReplicaFilter** property to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="bf141-129">Use o método **[PopulatePartial](database-populatepartial-method-dao.md)** para remover todos os registros da réplica parcial e transferir todos os registros da réplica completa que correspondem aos novos critérios do filtro para réplica.</span><span class="sxs-lookup"><span data-stu-id="bf141-129">Use the **[PopulatePartial](database-populatepartial-method-dao.md)** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="bf141-p104">Para remover um filtro, defina a propriedade **ReplicaFilter** como **False**. Se você remover todos os filtros e chamar o método **PopulatePartial**, nenhum registro aparecerá nas tabelas replicadas da réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="bf141-p104">To remove a filter, set the **ReplicaFilter** property to **False**. If you remove all filters and invoke the **PopulatePartial** method, no records will appear in any replicated tables in the partial replica.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bf141-132">[!OBSERVAçãO] Se um filtro para réplica foi alterado e o método <STRONG>Synchronize</STRONG> for chamado antes do método <STRONG>PopulatePartial</STRONG>, ocorrerá um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="bf141-132">If a replica filter has changed, and the <STRONG>Synchronize</STRONG> method is invoked without first invoking <STRONG>PopulatePartial</STRONG>, a trappable error occurs.</span></span></P>



## <a name="example"></a><span data-ttu-id="bf141-133">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bf141-133">Example</span></span>

<span data-ttu-id="bf141-134">O exemplo a seguir usa a propriedade **ReplicaFilter** para replicar somente os registros dos clientes da região da Califórnia.</span><span class="sxs-lookup"><span data-stu-id="bf141-134">The following example uses the **ReplicaFilter** property to replicate only customer records from the California region.</span></span>

```vb 
Sub ReplicaFilterX() 
 
 ' This example assumes the current open database 
 ' is the replica. 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 Set dbsTemp = OpenDatabase("Northwind.mdb") 
 Set tdfCustomers = dbsTemp.TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 dbsTemp.Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 dbsTemp.PopulatePartial "C:\SALES\FY96.MDB" 
 
 ' Now remove the replica filter (for example purposes 
 ' only). 
 tdfCustomers.ReplicaFilter = False 
 ' Repopulate the database. 
 dbsTemp.PopulatePartial "C:\SALES\DATA96.MDB" 
 
End Sub 
 
```

