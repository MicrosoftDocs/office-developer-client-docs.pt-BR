---
title: Método SubmitChanges (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ea7f3e27a75b4483cb8cf46e27d4492f831cff33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314396"
---
# <a name="submitchanges-method-rds"></a>Método SubmitChanges (RDS)

**Aplica-se ao:** Access 2013, Office 2013

Submete as alterações pendentes do [Recordset](recordset-object-ado.md) atualizável e armazenado localmente em cache para a fonte de dados especificada na propriedade [Connect](connect-property-rds.md) ou na propriedade [URL](url-property-rds.md).

## <a name="syntax"></a>Sintaxe

*DataControl*. SubmitChanges

** Datafactory. *Conexão*SubmitChanges, *Recordset*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*DataControl* |Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*DataFactory* |Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).|
|*Connection* |Um valor **String** que representa a conexão criada com a propriedade **Connect** do objeto **RDS.DataControl**.|
|*Recordset* |Uma variável de objeto que representa um objeto **Recordset**.|

## <a name="remarks"></a>Comentários

As propriedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) e [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) devem ser definidas antes de utilizar o método **SubmitChanges** com o objeto **RDS.DataControl**.

Se você chamar o método [CancelUpdate](cancelupdate-method-rds.md) depois de chamar **SubmitChanges** para o mesmo objeto **Recordset**, a chamada a **CancelUpdate** falhará porque as alterações já foram confirmadas.

Apenas os registros alterados serão enviados para modificação e todas as alterações obterão êxito ou falharão ao mesmo tempo.

Você pode usar **SubmitChanges** somente com o objeto **RDSServer.** datafactory *padrão* . Objetos corporativos personalizados não podem utilizar esse método.

Se a propriedade **URL** foi definida, **SubmitChanges** submeterá as alterações para o local especificado pela URL.

