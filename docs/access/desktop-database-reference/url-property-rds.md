---
title: Propriedade URL (RDS - referência de banco de dados da área de trabalho do Access)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f75e5e1a6d4df21970eea387ecd85ac8ef346a70
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943770"
---
# <a name="url-property-rds"></a>Propriedade URL (RDS)


**Aplica-se a**: Access 2013, o Office 2013



Indica um cadeia de caracteres que contém uma URL relativa ou absoluta.

Você pode definir a propriedade **URL** no tempo de design na marca OBJECT do objeto [DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script.

## <a name="syntax"></a>Sintaxe

Tempo de design: \<PARAM nome = valor "URL" = "Server"\>

Tempo de execução: DataControl.URL="Server"

## <a name="parameters"></a>Parâmetros

- *Server*

  - Um valor **String** que contém uma URL válida.

- *DataControl*

  - Uma variável de objeto que representa um objeto **DataControl**.

## <a name="remarks"></a>Comentários

Normalmente, a URL identifica um arquivo Active Server Page (.asp) que pode gerar e retornar um [Recordset](recordset-object-ado.md). Portanto, o usuário pode obter um **Recordset** sem ter que invocar o objeto [DataFactory](datafactory-object-rdsserver.md) do servidor ou programar um objeto comercial personalizado.

Se a propriedade **URL** tiver sido definida, [SubmitChanges](submitchanges-method-rds.md) enviará as alterações para o local especificado pela URL.

