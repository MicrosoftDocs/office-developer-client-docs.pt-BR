---
title: Método Delete (Coleção Parameters do ADO)
TOCTitle: Delete Method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 43d193a78be10ec5cedc2fe1a4001e677878dfb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464203"
---
# <a name="delete-method-ado-parameters-collection"></a>Método Delete (Coleção Parameters do ADO)


**Aplica-se a**: Access 2013 | Office 2013


Exclui um objeto da coleção [Parameters](parameters-collection-ado.md).

## <a name="syntax"></a>Sintaxe

*Parâmetros*. Excluir *índice*

## <a name="parameters"></a>Parâmetros

  - *Index*

  - Um valor **String** que contém o nome do objeto que você deseja excluir ou a posição ordinal do objeto (índice) na coleção.

## <a name="remarks"></a>Comentários

A utilização do método **Delete** em uma coleção permite remover um dos objetos da coleção. Esse método está disponível apenas na coleção **Parameters** de um objeto [Command](command-object-ado.md). Você deve utilizar a propriedade [Name](parameter-object-ado.md) do objeto [Parameter](name-property-ado.md) ou seu índice de coleção ao chamar o método **Delete**  uma variável de objeto não é um argumento válido.

