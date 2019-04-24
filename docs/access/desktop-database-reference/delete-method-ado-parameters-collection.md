---
title: Método Delete (coleção paraMeters do ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e075e176f1c007a258f6277147442223ae108b47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294089"
---
# <a name="delete-method-ado-parameters-collection"></a>Método Delete (coleção paraMeters do ADO)

**Aplica-se ao:** Access 2013, Office 2013

Exclui um objeto da coleção [Parameters](parameters-collection-ado.md).

## <a name="syntax"></a>Sintaxe

*Parâmetros*. Excluir *índice*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Índice* |Um valor **String** que contém o nome do objeto que você deseja excluir ou a posição ordinal do objeto (índice) na coleção.|

## <a name="remarks"></a>Comentários

A utilização do método **Delete** em uma coleção permite remover um dos objetos da coleção. Esse método está disponível apenas na coleção **Parameters** de um objeto [Command](command-object-ado.md). Você deve utilizar a propriedade [Name](name-property-ado.md) do objeto [Parameter](parameter-object-ado.md) ou seu índice de coleção ao chamar o método **Delete** — uma variável de objeto não é um argumento válido.

