---
title: Propriedade Connect (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42e7dd643985cee9aef8887099eb90dcdb381f4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295979"
---
# <a name="connect-property-rds"></a>Propriedade Connect (RDS)

**Aplica-se ao:** Access 2013, Office 2013

Indica o nome do banco de dados a partir do qual são executadas as operações de consulta e atualização.

É possível definir a propriedade **Connect** em tempo de design nas marcas OBJECT do objeto [RDS.DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script (por exemplo, VBScript).

## <a name="syntax"></a>Sintaxe

Tempo de design \<: parâmetro Name = "Connect" value = "ConnectionString"\>

Tempo de execução: dataControl. Connect = "ConnectionString"

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*ConnectionString* |Uma sequência de conexão válida. Para obter mais informações gerais sobre sequências de conexão, consulte a propriedade [ConnectionString](connectionstring-property-ado.md) ou a documentação de seu provedor.<br/><br/>**Observação**: ESPECIFICANDO o MS Remote como o provedor para o **RDS. DataControl** criaria um cenário de quatro camadas. Cenários com mais de três camadas não foram testados e não devem ser necessários.|
|*DataControl* |Uma variável de objeto que representa um objeto **RDS.DataControl**.|

