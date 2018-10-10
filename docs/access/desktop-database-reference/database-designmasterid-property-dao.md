---
title: Propriedade Database.DesignMasterID (DAO)
TOCTitle: DesignMasterID Property
ms:assetid: c0545561-d44f-5479-8ae0-e3955db91761
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822824(v=office.15)
ms:contentKeyID: 48547508
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053417
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0bb2e369f886ba60fb425b9f1f2d10fdea0c1463
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463696"
---
# <a name="databasedesignmasterid-property-dao"></a><span data-ttu-id="75450-102">Propriedade Database.DesignMasterID (DAO)</span><span class="sxs-lookup"><span data-stu-id="75450-102">Database.DesignMasterID Property (DAO)</span></span>

<span data-ttu-id="75450-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="75450-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="75450-104">Define ou retorna um valor de 16 bytes que identifica exclusivamente a Design Mestre em um conjunto de réplicas (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="75450-104">Sets or returns a 16-byte value that uniquely identifies the Design Master in a replica set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="75450-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75450-105">Syntax</span></span>

<span data-ttu-id="75450-106">*expressão* . DesignMasterID</span><span class="sxs-lookup"><span data-stu-id="75450-106">*expression* .DesignMasterID</span></span>

<span data-ttu-id="75450-107">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="75450-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="75450-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="75450-108">Remarks</span></span>

<span data-ttu-id="75450-p101">Você deve definir a propriedade **DesignMasterID** somente se precisar mover o Design Mestre atual. Definir essa propriedade torna uma réplica específica no conjunto de réplicas a Design Mestre.</span><span class="sxs-lookup"><span data-stu-id="75450-p101">You should set the **DesignMasterID** property only if you need to move the current Design Master. Setting this property makes a specific replica in the replica set the Design Master.</span></span>

> [!NOTE]
> <span data-ttu-id="75450-p102">[!OBSERVAçãO] Nunca cria uma segundo Design Mestre em um conjunto de réplicas. A existência de um segundo Design Mestre pode resultar em perda de dados.</span><span class="sxs-lookup"><span data-stu-id="75450-p102">Never create a second Design Master in a replica set. The existence of a second Design Master can result in the loss of data.</span></span>

<span data-ttu-id="75450-p103">Sob circunstâncias extremas  por exemplo, se o Design Mestre for apagada ou estiver corrompida  você poderá definir essa propriedade na réplica atual. Entretanto, a definição dessa propriedade em uma réplica, quando já houver outro Design Mestre no conjunto, poderá dividir o conjunto de réplicas em dois conjuntos irreconciliáveis e impedir qualquer sincronização de dados posterior.</span><span class="sxs-lookup"><span data-stu-id="75450-p103">Under extreme circumstances— for example, if the Design Master is erased or corrupted— you can set this property at the current replica. However, setting this property at a replica when there is already another Design Master in the set might partition your replica set into two irreconcilable sets and prevent any further synchronization of data.</span></span>

<span data-ttu-id="75450-p104">Se você decidir tornar uma réplica o novo Design Mestre para o conjunto, sincronize-a com todas as réplicas no conjunto de réplicas antes de definir a propriedade **DesignMasterID** na réplica. A réplica deve ser aberta no modo exclusivo para torná-la o Design Mestre.</span><span class="sxs-lookup"><span data-stu-id="75450-p104">If you decide to make a replica the new Design Master for the set, synchronize it with all the replicas in the replica set before setting the **DesignMasterID** property in the replica. The replica must be open in exclusive mode in order to make it the Design Master.</span></span>

<span data-ttu-id="75450-117">Se você tornar uma réplica, que é somente leitura, o Design Mestre, a réplica de destino se tornará de leitura/gravação; o Design Mestre antigo também permanecerá de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="75450-117">If you make a replica that is designated read-only into the Design Master, the target replica is made read/write; the old Design Master also remains read/write.</span></span>

<span data-ttu-id="75450-118">A configuração da propriedade **DesignMasterID** é armazenada na tabela de sistema MSysRepInfo.</span><span class="sxs-lookup"><span data-stu-id="75450-118">The **DesignMasterID** property setting is stored in the MSysRepInfo system table.</span></span>

## <a name="example"></a><span data-ttu-id="75450-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="75450-119">Example</span></span>

<span data-ttu-id="75450-p105">Este exemplo define a propriedade **DesignMasterID** para a configuração da propriedade **ReplicaID** de outro banco de dados, tornando esse banco de dados o Design Mestre no conjunto de réplicas. As Estruturas-mestre nova e antiga são sincronizadas para atualizar as alterações de design. Para que esse código funcione, você deve criar uma Estrutura-mestre, incluir seus nomes e caminhos como apropriado e executar esse código a partir de um banco de dados diferente do Design Mestre novo ou antigo.</span><span class="sxs-lookup"><span data-stu-id="75450-p105">This example sets the **DesignMasterID** property to the **ReplicaID** property setting of another database, making that database the Design Master in the replica set. The old and new Design Masters are synchronized to update the design change. For this code to work, you must create a Design Master and replica, include their names and paths as appropriate, and run this code from a database other than the old or new Design Master.</span></span>

```vb 
 Sub SetNewDesignMaster(strOldDM as String, _ 
    strNewDM as String) 
    
    Dim dbsOld As Database 
    Dim dbsNew As Database 
    
    ' Open the current Design Master in exclusive mode. 
    Set dbsOld = OpenDatabase(strOldDM, True) 
    
    ' Open the database that will become the new 
    ' Design Master. 
    Set dbsNew = OpenDatabase(strNewDM) 
    
    ' Make the new database the Design Master. 
    dbsOld.DesignMasterID = dbsNew.ReplicaID 
    
    ' Synchronize the old Design Master with the new 
    ' Design Master, and allow two-way exchanges. 
    dbsOld.Synchronize strNewDM, dbRepImpExpChanges 
    dbsOld.Close 
    dbsNew.Close 
 
 End Sub 
 
```

