---
title: Propriedade Database.ReplicaID (DAO)
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
ms.openlocfilehash: ca879a3c56d23a67987d86b7fbc21421cd8db843
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461991"
---
# <a name="databasereplicaid-property-dao"></a>Propriedade Database.ReplicaID (DAO)


**Aplica-se a**: Access 2013 | Office 2013


Retorna um valor de 16 bytes que identifica exclusivamente uma réplica de um banco dados (somente nos espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . ReplicaID

*expressão* Uma variável que representa um objeto de **banco de dados** .

## <a name="remarks"></a>Comentários

O valor de retorno é um valor **GUID** que identifica exclusivamente a réplica ou a Design Mestre.

O mecanismo do banco de dados do Microsoft Access gerará automaticamente esse valor, quando você criar uma nova réplica.

A propriedade **ReplicaID** de cada réplica (e o Design Mestre) é armazenada em uma tabela do sistema MSysReplicas.

## <a name="example"></a>Exemplo

Este exemplo faz uma réplica do Design Mestre do Northwind.mdb e depois retorna a **ReplicaID** da replica, criada automaticamente pelo mecanismo do banco de dados do Microsoft Access. (Se você ainda não criou um Design Mestre do Northwind, consulte a propriedade **Replicable** ou altere o nome do banco de dados no código para um Design Mestre existente).

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

