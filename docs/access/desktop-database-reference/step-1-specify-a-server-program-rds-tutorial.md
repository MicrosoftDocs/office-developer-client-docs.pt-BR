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
# <a name="step-1-specify-a-server-program-rds-tutorial"></a><span data-ttu-id="eb605-102">Etapa 1: Especificar um programa do servidor (Tutorial do RDS)</span><span class="sxs-lookup"><span data-stu-id="eb605-102">Step 1: Specify a Server Program (RDS Tutorial)</span></span>


<span data-ttu-id="eb605-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb605-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eb605-p101">No caso mais geral, use o objeto [RDS.DataSpace](dataspace-object-rds.md) do método [CreateObject](createobject-method-rds.md) para especificar o programa do servidor padrão, [RDSServer.DataFactory](datafactory-object-rdsserver.md), ou seu próprio programa de servidor personalizado (objeto de negócios). Um programa de servidor é instanciado no servidor e uma referência ao programa do servidor, ou *proxy*, é retornada.</span><span class="sxs-lookup"><span data-stu-id="eb605-p101">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object). A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="eb605-106">Este tutorial usa o programa do servidor padrão:</span><span class="sxs-lookup"><span data-stu-id="eb605-106">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

