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
ms.openlocfilehash: da9619102a955c9a7945d05e89a1e132371d2461
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868403"
---
# <a name="databasedesignmasterid-property-dao"></a>Propriedade Database.DesignMasterID (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor de 16 bytes que identifica exclusivamente a Design Mestre em um conjunto de réplicas (apenas espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . DesignMasterID

*expressão* Uma variável que representa um objeto de **banco de dados** .

## <a name="remarks"></a>Comentários

Você deve definir a propriedade **DesignMasterID** somente se precisar mover o Design Mestre atual. Definir essa propriedade torna uma réplica específica no conjunto de réplicas a Design Mestre.

> [!NOTE]
> [!OBSERVAçãO] Nunca cria uma segundo Design Mestre em um conjunto de réplicas. A existência de um segundo Design Mestre pode resultar em perda de dados.

Sob circunstâncias extremas  por exemplo, se o Design Mestre for apagada ou estiver corrompida  você poderá definir essa propriedade na réplica atual. Entretanto, a definição dessa propriedade em uma réplica, quando já houver outro Design Mestre no conjunto, poderá dividir o conjunto de réplicas em dois conjuntos irreconciliáveis e impedir qualquer sincronização de dados posterior.

Se você decidir tornar uma réplica o novo Design Mestre para o conjunto, sincronize-a com todas as réplicas no conjunto de réplicas antes de definir a propriedade **DesignMasterID** na réplica. A réplica deve ser aberta no modo exclusivo para torná-la o Design Mestre.

Se você tornar uma réplica, que é somente leitura, o Design Mestre, a réplica de destino se tornará de leitura/gravação; o Design Mestre antigo também permanecerá de leitura/gravação.

A configuração da propriedade **DesignMasterID** é armazenada na tabela de sistema MSysRepInfo.

## <a name="example"></a>Exemplo

Este exemplo define a propriedade **DesignMasterID** para a configuração da propriedade **ReplicaID** de outro banco de dados, tornando esse banco de dados o Design Mestre no conjunto de réplicas. As Estruturas-mestre nova e antiga são sincronizadas para atualizar as alterações de design. Para que esse código funcione, você deve criar uma Estrutura-mestre, incluir seus nomes e caminhos como apropriado e executar esse código a partir de um banco de dados diferente do Design Mestre novo ou antigo.

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

