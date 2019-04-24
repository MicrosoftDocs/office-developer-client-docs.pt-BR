---
title: Propriedade Database. ReplicaId (DAO)
TOCTitle: ReplicaID Property
ms:assetid: cf2ca8a1-d13f-30e0-2ca1-dd32ac736c56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834672(v=office.15)
ms:contentKeyID: 48547805
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053375
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2ada9bf23a4b8fc34c5f9b4f24350fc6af91dc85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294712"
---
# <a name="databasereplicaid-property-dao"></a><span data-ttu-id="3ca52-102">Propriedade Database. ReplicaId (DAO)</span><span class="sxs-lookup"><span data-stu-id="3ca52-102">Database.ReplicaID property (DAO)</span></span>


<span data-ttu-id="3ca52-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ca52-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="3ca52-104">Retorna um valor de 16 bytes que identifica exclusivamente uma réplica de um banco dados (somente nos espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ca52-104">Returns a 16-byte value that uniquely identifies a database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca52-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ca52-105">Syntax</span></span>

<span data-ttu-id="3ca52-106">*expressão* . ReplicaID</span><span class="sxs-lookup"><span data-stu-id="3ca52-106">*expression* .ReplicaID</span></span>

<span data-ttu-id="3ca52-107">*expressão* Uma variável que representa um objeto **Database** .</span><span class="sxs-lookup"><span data-stu-id="3ca52-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ca52-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ca52-108">Remarks</span></span>

<span data-ttu-id="3ca52-109">O valor de retorno é um valor **GUID** que identifica exclusivamente a réplica ou a Design Mestre.</span><span class="sxs-lookup"><span data-stu-id="3ca52-109">The return value is a **GUID** value that uniquely identifies the replica or Design Master.</span></span>

<span data-ttu-id="3ca52-110">O mecanismo do banco de dados do Microsoft Access gerará automaticamente esse valor, quando você criar uma nova réplica.</span><span class="sxs-lookup"><span data-stu-id="3ca52-110">The Microsoft Access database engine automatically generates this value when you create a new replica.</span></span>

<span data-ttu-id="3ca52-111">A propriedade **ReplicaID** de cada réplica (e o Design Mestre) é armazenada em uma tabela do sistema MSysReplicas.</span><span class="sxs-lookup"><span data-stu-id="3ca52-111">The **ReplicaID** property of each replica (and the Design Master) is stored in the MSysReplicas system table.</span></span>

## <a name="example"></a><span data-ttu-id="3ca52-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3ca52-112">Example</span></span>

<span data-ttu-id="3ca52-p101">Este exemplo faz uma réplica do Design Mestre do Northwind.mdb e depois retorna a **ReplicaID** da replica, criada automaticamente pelo mecanismo do banco de dados do Microsoft Access. (Se você ainda não criou um Design Mestre do Northwind, consulte a propriedade **Replicable** ou altere o nome do banco de dados no código para um Design Mestre existente).</span><span class="sxs-lookup"><span data-stu-id="3ca52-p101">This example makes a replica from the Design Master of Northwind.mdb, and then returns the replica's **ReplicaID**, which is automatically created by the Microsoft Access database engine. (If you have not yet created a Design Master of Northwind, refer to the **Replicable** property, or change the name of the database in the code to an existing Design Master.)</span></span>

```vb 
Sub MakeReplicaReplicaIDX() 
 
 Dim dbsNorthwind As Database 
 Dim prpReplicaID As Property 
 Dim dbsReplica As Database 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Makes a new replica. 
 dbsNorthwind.MakeReplica "Nwreplica2.mdb", _ 
 "second replica" 
 dbsNorthwind.Close 
 
 ' Opens the new replica to read its ReplicaID. 
 Set dbsReplica = OpenDatabase("Nwreplica2.mdb") 
 
 Debug.Print dbsReplica.ReplicaID 
 dbsReplica.Close 
 
End Sub 
 
```

