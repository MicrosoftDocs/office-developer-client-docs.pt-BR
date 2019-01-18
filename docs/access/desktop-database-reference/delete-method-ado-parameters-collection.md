---
title: Excluir método (coleção Parameters do ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e075e176f1c007a258f6277147442223ae108b47
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704571"
---
# <a name="delete-method-ado-parameters-collection"></a>Excluir método (coleção Parameters do ADO)

**Aplica-se a**: Access 2013, o Office 2013

Exclui um objeto da coleção [Parameters](parameters-collection-ado.md).

## <a name="syntax"></a>Sintaxe

*Parâmetros*. Excluir *índice*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Índice* |Um valor **String** que contém o nome do objeto que você deseja excluir ou a posição ordinal do objeto (índice) na coleção.|

## <a name="remarks"></a>Comentários

A utilização do método **Delete** em uma coleção permite remover um dos objetos da coleção. Esse método está disponível apenas na coleção **Parameters** de um objeto [Command](command-object-ado.md). Você deve utilizar a propriedade [Name](parameter-object-ado.md) do objeto [Parameter](name-property-ado.md) ou seu índice de coleção ao chamar o método **Delete**  uma variável de objeto não é um argumento válido.

