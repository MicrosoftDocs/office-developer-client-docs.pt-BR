---
title: Propriedades Recordset, SourceRecordset (RDS)
TOCTitle: Recordset, SourceRecordset Properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 08fe0f569b36fe0b3403cb564dc53eadf2edff8c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887177"
---
# <a name="recordset-sourcerecordset-properties-rds"></a>Propriedades Recordset, SourceRecordset (RDS)


**Aplica-se a**: Access 2013, o Office 2013

Indica o objeto **Recordset** retornado de um objeto corporativo personalizado.

## <a name="syntax"></a>Sintaxe

*DataControl*. SourceRecordset = *Recordset*

*Recordset* = *DataControl*. Conjunto de registros

## <a name="parameters"></a>Parâmetros

  - *DataControl*

  - Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).

  - *Recordset*

  - Uma variável de objeto que representa um objeto **Recordset**.

## <a name="remarks"></a>Comentários

Você pode definir a propriedade **SourceRecordset** para um [Recordset](recordset-object-ado.md) retornado por um objeto comercial personalizado.

Essas propriedades permitem que um aplicativo trate do processo de ligação por um processo personalizado. Elas recebem um conjunto de linhas disposto em um **Recordset**, de forma que você possa interagir diretamente com o **Recordset**, executando ações como a definição de propriedades ou interagindo por meio do **Recordset**.

Você pode definir a propriedade **SourceRecordset** ou ler a propriedade **Recordset** em tempo de execução no código de script.

**SourceRecordset** é uma propriedade somente gravação, ao contrário da propriedade **Recordset**, que é somente leitura.

