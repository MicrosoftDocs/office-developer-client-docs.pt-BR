---
title: Método DBEngine.Idle (DAO)
TOCTitle: Idle Method
ms:assetid: c90b565e-626e-139d-102a-0386601ce0c8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823202(v=office.15)
ms:contentKeyID: 48547666
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052978
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 50e445339251bb2d35f700c1fa3860c246ec70d4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882347"
---
# <a name="dbengineidle-method-dao"></a><span data-ttu-id="b47d5-102">Método DBEngine.Idle (DAO)</span><span class="sxs-lookup"><span data-stu-id="b47d5-102">DBEngine.Idle Method (DAO)</span></span>


<span data-ttu-id="b47d5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b47d5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="b47d5-104">Suspende o processamento de dados, habilitando o mecanismo de banco de dados do Microsoft Access a concluir tarefas pendentes, como otimização de memória ou tempo limite da página (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b47d5-104">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b47d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b47d5-105">Syntax</span></span>

<span data-ttu-id="b47d5-106">*expressão* . Ocioso (***ação***)</span><span class="sxs-lookup"><span data-stu-id="b47d5-106">*expression* .Idle(***Action***)</span></span>

<span data-ttu-id="b47d5-107">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="b47d5-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b47d5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b47d5-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b47d5-109">Nome</span><span class="sxs-lookup"><span data-stu-id="b47d5-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b47d5-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="b47d5-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b47d5-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b47d5-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b47d5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b47d5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b47d5-113">Ação</span><span class="sxs-lookup"><span data-stu-id="b47d5-113">Action</span></span></p></td>
<td><p><span data-ttu-id="b47d5-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="b47d5-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="b47d5-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b47d5-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b47d5-p101">Especifica a ação a ser tomada. Pode ser uma das constantes <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="b47d5-p101">Specifies the action to take. Can be one of the <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong> constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b47d5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b47d5-118">Remarks</span></span>

<span data-ttu-id="b47d5-p102">O método **Idle** permite que o mecanismo de banco de dados do Microsoft Access execute tarefas em segundo plano que podem não estar atualizadas por causa de intenso processamento de dados. Isso geralmente ocorre em ambientes multiusuários e multitarefas que não têm tempo suficiente de planejamento em segundo plano para manter todos os registros em um **[Recordset](recordset-object-dao.md)** atual.</span><span class="sxs-lookup"><span data-stu-id="b47d5-p102">The **Idle** method allows the Microsoft Access database engine to perform background tasks that may not be up-to-date because of intense data processing. This is often true in multiuser, multitasking environments that don't have enough background processing time to keep all records in a **[Recordset](recordset-object-dao.md)** current.</span></span>

<span data-ttu-id="b47d5-p103">Em geral, bloqueios de leitura são removidos e os dados em objetos **Recordset** do tipo dynaset locais são atualizados apenas quando nenhuma outra ação ocorrer (inclusive movimentos de mouse). Se você usa periodicamente o método **Idle**, o mecanismo de banco de dados do Microsoft Access pode realizar o processamento de tarefas em segundo plano, liberando bloqueios de leitura desnecessários.</span><span class="sxs-lookup"><span data-stu-id="b47d5-p103">Usually, read locks are removed and data in local dynaset-type **Recordset** objects are updated only when no other actions (including mouse movements) occur. If you periodically use the **Idle** method, the Microsoft Access database engine can catch up on background processing tasks by releasing unneeded read locks.</span></span>

<span data-ttu-id="b47d5-123">Especificar o argumento **dbRefreshCache** opcional atualiza a memória apenas com os dados mais recentes do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b47d5-123">Specifying the optional **dbRefreshCache** argument refreshes memory with only the most current data from the database.</span></span>

<span data-ttu-id="b47d5-p104">Você não precisa usar esse método em ambientes de um único usuário a menos que várias instâncias de um aplicativo estejam em execução. O método **Idle** pode aumentar o desempenho em um ambiente multiusuário porque força o mecanismo de banco de dados a gravar dados em disco, liberando bloqueios na memória.</span><span class="sxs-lookup"><span data-stu-id="b47d5-p104">You don't need to use this method in single-user environments unless multiple instances of an application are running. The **Idle** method may increase performance in a multiuser environment because it forces the database engine to write data to disk, releasing locks on memory.</span></span>


> [!NOTE]
> <span data-ttu-id="b47d5-126">[!OBSERVAçãO] Você também pode liberar bloqueios de leitura tornando as operações parte de uma transação.</span><span class="sxs-lookup"><span data-stu-id="b47d5-126">You can also release read locks by making operations part of a transaction.</span></span>

## <a name="example"></a><span data-ttu-id="b47d5-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b47d5-127">Example</span></span>

<span data-ttu-id="b47d5-p105">Este exemplo usa o método **Idle** para assegurar que um procedimento de saída está acessando os dados mais atuais disponíveis no banco de dados. O procedimento IdleOutput é exigido para a execução do procedimento.</span><span class="sxs-lookup"><span data-stu-id="b47d5-p105">This example uses the **Idle** method to ensure that an output procedure is accessing the most current data available from the database. The IdleOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub IdleX() 
 
 Dim dbsNorthwind As Database 
 Dim strCountry As String 
 Dim strSQL As String 
 Dim rstOrders As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Get name of country from user and build SQL statement 
 ' with it. 
 strCountry = Trim(InputBox("Enter country:")) 
 strSQL = "SELECT * FROM Orders WHERE ShipCountry = '" & _ 
 strCountry & "' ORDER BY OrderID" 
 
 ' Open Recordset object with SQL statement. 
 Set rstOrders = dbsNorthwind.OpenRecordset(strSQL) 
 
 ' Display contents of Recordset object. 
 IdleOutput rstOrders, strCountry 
 
 rstOrders.Close 
 dbsNorthwind.Close 
 
End Sub 
 
Sub IdleOutput(rstTemp As Recordset, strTemp As String) 
 
 ' Call the Idle method to release unneeded locks, force 
 ' pending writes, and refresh the memory with the current 
 ' data in the .mdb file. 
 DBEngine.Idle dbRefreshCache 
 
 ' Enumerate the Recordset object. 
 With rstTemp 
 Debug.Print "Orders from " & strTemp & ":" 
 Debug.Print , "OrderID", "CustomerID", "OrderDate" 
 Do While Not .EOF 
 Debug.Print , !OrderID, !CustomerID, !OrderDate 
 .MoveNext 
 Loop 
 End With 
 
End Sub 
 
```

