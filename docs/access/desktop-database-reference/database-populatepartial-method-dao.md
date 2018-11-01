---
title: Método Database.PopulatePartial (DAO)
TOCTitle: PopulatePartial Method
ms:assetid: fa3227a2-c961-6a98-32b3-5b6e5329a21d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837034(v=office.15)
ms:contentKeyID: 48548834
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101186
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ed8125d89691045a24ecc438d490146a8a3942b5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883012"
---
# <a name="databasepopulatepartial-method-dao"></a><span data-ttu-id="82dec-102">Método Database.PopulatePartial (DAO)</span><span class="sxs-lookup"><span data-stu-id="82dec-102">Database.PopulatePartial Method (DAO)</span></span>


<span data-ttu-id="82dec-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="82dec-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="82dec-p101">Sincroniza as alterações em uma réplica parcial com a réplica completa, limpa todos os registros na réplica parcial e preenche novamente a réplica parcial com base nos filtros da réplica atual. (Apenas bancos de dados do mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="82dec-p101">Synchronizes any changes in a partial replica with the full replica, clears all records in the partial replica, and then repopulates the partial replica based on the current replica filters. (Microsoft Access database engine databases only.).</span></span>

## <a name="syntax"></a><span data-ttu-id="82dec-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82dec-106">Syntax</span></span>

<span data-ttu-id="82dec-107">*expressão* . PopulatePartial (***DbPathName***)</span><span class="sxs-lookup"><span data-stu-id="82dec-107">*expression* .PopulatePartial(***DbPathName***)</span></span>

<span data-ttu-id="82dec-108">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="82dec-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="82dec-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82dec-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82dec-110">Nome</span><span class="sxs-lookup"><span data-stu-id="82dec-110">Name</span></span></p></th>
<th><p><span data-ttu-id="82dec-111">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="82dec-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="82dec-112">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="82dec-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="82dec-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="82dec-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82dec-114">DbPathName</span><span class="sxs-lookup"><span data-stu-id="82dec-114">DbPathName</span></span></p></td>
<td><p><span data-ttu-id="82dec-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="82dec-115">Required</span></span></p></td>
<td><p><span data-ttu-id="82dec-116"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="82dec-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="82dec-117">O caminho e o nome da réplica completa a partir da qual os registros serão preenchidos.</span><span class="sxs-lookup"><span data-stu-id="82dec-117">The path and name of the full replica from which to populate records.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="82dec-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="82dec-118">Remarks</span></span>

<span data-ttu-id="82dec-119">Quando você sincroniza uma réplica parcial com uma réplica completa, é possível criar registros "órfãos" na réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="82dec-119">When you synchronize a partial replica with a full replica, it is possible to create "orphaned" records in the partial replica.</span></span> <span data-ttu-id="82dec-120">Por exemplo, suponha que você tem uma tabela Customers com seu **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** definido como "região = 'CA'".</span><span class="sxs-lookup"><span data-stu-id="82dec-120">For example, suppose you have a Customers table with its **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** set to "Region = 'CA'".</span></span> <span data-ttu-id="82dec-121">Se um usuário alterar uma região de Customers de CA para NY na réplica parcial e, em seguida, ocorrer uma sincronização por meio do método **[Synchronize](database-synchronize-method-dao.md)**, a alteração será propagada para a réplica completa mas o registro que contém NY na réplica parcial é órfão porque agora ele não satisfaz aos critérios do filtro da réplica.</span><span class="sxs-lookup"><span data-stu-id="82dec-121">If a user changes a customer's region from CA to NY in the partial replica, and then a synchronization occurs via the **[Synchronize](database-synchronize-method-dao.md)** method, the change is propagated to the full replica but the record containing NY in the partial replica is orphaned because it now doesn't meet the replica filter criteria.</span></span>

<span data-ttu-id="82dec-p103">Para solucionar o problema dos registros órfãos, você pode usar o método **PopulatePartial**. O método **PopulatePartial** é semelhante ao método **Synchronize**, mas ele sincroniza quaisquer alterações com a réplica completa, remove todos os registros na réplica parcial e, em seguida, preenche novamente a réplica parcial com base nos atuais filtros da réplica. Mesmo que os filtros da réplica não tiverem sido alterados, **PopulatePartial** sempre limpará os registros na réplica parcial e os preencherá novamente com base nos filtros atuais.</span><span class="sxs-lookup"><span data-stu-id="82dec-p103">To solve the problem of orphaned records, you can use the **PopulatePartial** method. The **PopulatePartial** method is similar to the **Synchronize** method, but it synchronizes any changes with the full replica, removes all records in the partial replica, and then repopulates the partial replica based on the current replica filters. Even if your replica filters have not changed, **PopulatePartial** will always clear all records in the partial replica and repopulate it based on the current filters.</span></span>

<span data-ttu-id="82dec-p104">Geralmente, você deve usar o método **PopulatePartial** ao criar uma réplica parcial e sempre que alterar os filtros da réplica. Se seu aplicativo alterar os filtros da réplica, você deve executar os seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="82dec-p104">Generally, you should use the **PopulatePartial** method when you create a partial replica and whenever you change your replica filters. If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="82dec-127">Sincronize sua réplica completa com a réplica parcial nas quais os filtros estão sendo alterados.</span><span class="sxs-lookup"><span data-stu-id="82dec-127">Synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="82dec-128">Use as propriedades **ReplicaFilter** e **[PartialReplica](relation-partialreplica-property-dao.md)** para fazer as alterações desejadas no filtro da réplica.</span><span class="sxs-lookup"><span data-stu-id="82dec-128">Use the **ReplicaFilter** and **[PartialReplica](relation-partialreplica-property-dao.md)** properties to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="82dec-129">Chame o método **PopulatePartial** para remover todos os registros da réplica parcial e transferir todos os registros da réplica completa que satisfazem os novos critérios do filtro da réplica.</span><span class="sxs-lookup"><span data-stu-id="82dec-129">Call the **PopulatePartial** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="82dec-130">Se um filtro de réplica tiver sido alterado e o método **Synchronize** for invocado sem que seja invocado primeiramente **PopulatePartial**, ocorrerá um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="82dec-130">If a replica filter has changed, and the **Synchronize** method is invoked without first invoking **PopulatePartial**, a trappable error occurs.</span></span>

<span data-ttu-id="82dec-p105">O método **PopulatePartial** pode ser invocado apenas em uma réplica parcial que tiver sido aberta para acesso exclusivo. Além disso, não é possível chamar o método **PopulatePartial** a partir do código em execução dentro da própria réplica parcial. Em vez disso, abra a réplica parcial exclusivamente a partir da réplica completa ou de outro banco de dados e, em seguida, chame **PopulatePartial**.</span><span class="sxs-lookup"><span data-stu-id="82dec-p105">The **PopulatePartial** method can only be invoked on a partial replica that has been opened for exclusive access. Furthermore, you can't call the **PopulatePartial** method from code running within the partial replica itself. Instead, open the partial replica exclusively from the full replica or another database, then call **PopulatePartial**.</span></span>


> [!NOTE]
> <span data-ttu-id="82dec-p106">[!OBSERVAçãO] Embora **PopulatePartial** execute uma sincronização de mão única antes de limpar e preencher novamente a réplica parcial, ainda é uma boa ideia chamar **Synchronize** antes de chamar **PopulatePartial**. Isso ocorre porque se a chamada de **Synchronize** falhar, ocorrerá um erro interceptável. Você pode usar esse erro para decidir prosseguir ou não com o método **PopulatePartial** (o que remove todos os registros da réplica parcial). Se **PopulatePartial** for chamado por si mesmo e ocorrer um erro enquanto os registros estiverem sendo sincronizados, os registros da réplica parcial ainda serão limpos, o que pode não ser o resultado desejado.</span><span class="sxs-lookup"><span data-stu-id="82dec-p106">Although **PopulatePartial** performs a one-way synchronization before clearing and repopulating the partial replica, it is still a good idea to call **Synchronize** before calling **PopulatePartial**. This is because if the call to **Synchronize** fails, a trappable error occurs. You can use this error to decide whether or not to proceed with the **PopulatePartial** method (which removes all records in the partial replica). If **PopulatePartial** is called by itself and an error occurs while records are being synchronized, records in the partial replica will still be cleared, which may not be the desired result.</span></span>



## <a name="example"></a><span data-ttu-id="82dec-138">Exemplo</span><span class="sxs-lookup"><span data-stu-id="82dec-138">Example</span></span>

<span data-ttu-id="82dec-139">O exemplo a seguir usa o método **PopulatePartial** depois de alterar um filtro de réplica.</span><span class="sxs-lookup"><span data-stu-id="82dec-139">The following example uses the **PopulatePartial** method after changing a replica filter.</span></span>

```vb 
Sub PopulatePartialX() 
 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 ' Open the partial replica in exclusive mode. 
 Set dbsTemp = OpenDatabase("F:\SALES\FY96CA.MDB", True) 
 
 With dbsTemp 
 Set tdfCustomers = .TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 .Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 
 ' Populate records from the full replica. 
 .PopulatePartial "C:\SALES\FY96.MDB" 
 
 .Close 
 End With 
 
End Sub 
 
```

