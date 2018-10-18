---
title: 'Etapa 5: O DataControl torna-se utilizável (Tutorial RDS)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d5b0dfef4d14594c2b2a9b8b57b866e032a07a5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605650"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a>Etapa 5: O DataControl torna-se utilizável (Tutorial RDS)


**Aplica-se a**: Access 2013 | Office 2013

O objeto **Recordset** retornado está disponível para uso. Você pode examinar, navegar ou editá-lo como faria com qualquer outro **Recordset**. As possibilidades de uso do **Recordset** dependem do seu ambiente. O Visual Basic e o Visual C++ possuem controles visuais que podem utilizar um **Recordset** diretamente ou indiretamente com a ajuda de um controle de dados de ativação.

<<<<<<< Cabeça por exemplo, se você estiver exibindo uma página da Web no Microsoft Internet Explorer, você talvez queira exibir os dados do objeto **Recordset** em um controle visual. Os controles visuais em uma página da Web não podem acessar um objeto **Recordset** diretamente. No entanto, podem acessar o objeto **Recordset** através do [RDS.DataControl](datacontrol-object-rds.md). O **RDS.DataControl** torna-se utilizável por um controle visual quando sua propriedade [SourceRecordset](recordset-sourcerecordset-properties-rds.md) for definida como o objeto **Recordset**.
=== Por exemplo, se você está exibindo uma página da Web no Microsoft Internet Explorer, você deseja exibir os dados do objeto **Recordset** em um controle visual. Controles visuais em uma página da Web não podem acessar um objeto **Recordset** diretamente. No entanto, podem acessar o objeto **Recordset** através do [RDS.DataControl](datacontrol-object-rds.md). O **RDS.DataControl** torna-se utilizável por um controle visual quando sua propriedade [SourceRecordset](recordset-sourcerecordset-properties-rds.md) for definida como o objeto **Recordset**.
>>>>>>> mestre

O objeto de controle visual deve ter seu parâmetro **DATASRC** definido como **RDS.DataControl** e sua propriedade **DATAFLD** definida como um campo de objeto **Recordset** (coluna).

Nesse tutorial, defina a propriedade **SourceRecordset**:

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

