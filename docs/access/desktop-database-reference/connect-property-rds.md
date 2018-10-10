---
title: Propriedade Connect (RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb628356e4d93201c38cf84a9c3245b13e044ee3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464706"
---
# <a name="connect-property-rds"></a>Propriedade Connect (RDS)


**Aplica-se a**: Access 2013 | Office 2013

Indica o nome do banco de dados a partir do qual são executadas as operações de consulta e atualização.

É possível definir a propriedade **Connect** em tempo de design nas marcas OBJECT do objeto [RDS.DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script (por exemplo, VBScript).

## <a name="syntax"></a>Sintaxe

Tempo de design: \<nome do parâmetro = "Conectar" valor = "ConnectionString"\>

Tempo de execução: DataControl.Connect = "ConnectionString"

## <a name="parameters"></a>Parâmetros

  - *ConnectionString*

  - Uma sequência de conexão válida. Para obter mais informações gerais sobre sequências de conexão, consulte a propriedade [ConnectionString](connectionstring-property-ado.md) ou a documentação de seu provedor.
    

    > [!NOTE]
    > <P>[!OBSERVAçãO] A especificação do MS Remote como o provedor para o <STRONG>RDS.DataControl</STRONG> criaria um cenário de quatro camadas. Cenários com mais de três camadas não foram testados e não devem ser necessários.</P>



  - *DataControl*

  - Uma variável de objeto que representa um objeto **RDS.DataControl**.

