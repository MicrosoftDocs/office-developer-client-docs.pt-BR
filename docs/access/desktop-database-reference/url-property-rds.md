---
title: Propriedade URL (RDS – referência do banco de dados da área de trabalho do Access)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aafc8cc10410cafed21e38ad7fec269c391c1fa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313395"
---
# <a name="url-property-rds"></a>Propriedade URL (RDS)

**Aplica-se ao:** Access 2013, Office 2013

Indica um cadeia de caracteres que contém uma URL relativa ou absoluta.

Você pode definir a propriedade **URL** no tempo de design na marca OBJECT do objeto [DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script.

## <a name="syntax"></a>Sintaxe

Tempo de design: \< PARAM NAME="URL" VALUE="Server"\>

Tempo de executar: DataControl.URL="Server"

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Server* |Um valor **String** que contém uma URL válida.|
|*DataControl* |Uma variável de objeto que representa um objeto **DataControl**.|

## <a name="remarks"></a>Comentários

Normalmente, a URL identifica um arquivo Active Server Page (.asp) que pode gerar e retornar um [Recordset](recordset-object-ado.md). Portanto, o usuário pode obter um **Recordset** sem ter que invocar o objeto [DataFactory](datafactory-object-rdsserver.md) do servidor ou programar um objeto comercial personalizado.

Se a propriedade **URL** tiver sido definida, [SubmitChanges](submitchanges-method-rds.md) enviará as alterações para o local especificado pela URL.

