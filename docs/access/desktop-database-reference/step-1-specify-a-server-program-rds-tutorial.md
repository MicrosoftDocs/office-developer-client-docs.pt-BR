---
title: 'Etapa 1: Especificar um programa servidor (Tutorial RDS)'
TOCTitle: 'Step 1: Specify a Server Program (RDS Tutorial)'
ms:assetid: e6c2c624-d9bc-c899-60bc-e80a67ce8596
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250172(v=office.15)
ms:contentKeyID: 48548389
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fe85853b013caf8610e7706f3d836551ce8801c7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871875"
---
# <a name="step-1-specify-a-server-program-rds-tutorial"></a>Etapa 1: Especificar um programa do servidor (Tutorial do RDS)


**Aplica-se a**: Access 2013, o Office 2013

No caso mais geral, use o objeto [RDS.DataSpace](dataspace-object-rds.md) do método [CreateObject](createobject-method-rds.md) para especificar o programa do servidor padrão, [RDSServer.DataFactory](datafactory-object-rdsserver.md), ou seu próprio programa de servidor personalizado (objeto de negócios). Um programa de servidor é instanciado no servidor e uma referência ao programa do servidor, ou *proxy*, é retornada.

Este tutorial usa o programa do servidor padrão:

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

