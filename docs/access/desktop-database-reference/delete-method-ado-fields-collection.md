---
title: Método Delete (Coleção Fields do ADO)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3dc4d3553113a35fba875c3eb23ec544ea3d6b7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463935"
---
# <a name="delete-method-ado-fields-collection"></a>Método Delete (Coleção Fields do ADO)


**Aplica-se a**: Access 2013 | Office 2013



Exclui um objeto da coleção [Fields](fields-collection-ado.md).

## <a name="syntax"></a>Sintaxe

*Campos*. Excluir um*campo*

## <a name="parameters"></a>Parâmetros

  - *Field*

  - Um **Variant** que designa o objeto [Field](field-object-ado.md) a ser excluído. Este parâmetro pode ser o nome do objeto **Field** ou a posição ordinal do próprio objeto **Field**.

## <a name="remarks"></a>Comentários

Chamar o método **Fields.Delete** em um [Recordset](recordset-object-ado.md) aberto causa um erro em tempo de execução.

