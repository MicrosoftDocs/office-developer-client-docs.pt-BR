---
title: Excluir método (coleção Fields do ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718256"
---
# <a name="delete-method-ado-fields-collection"></a>Excluir método (coleção Fields do ADO)

**Aplica-se a**: Access 2013, o Office 2013


Exclui um objeto da coleção [Fields](fields-collection-ado.md).

## <a name="syntax"></a>Sintaxe

*Campos*. Excluir um*campo*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Field* |Um **Variant** que designa o objeto [Field](field-object-ado.md) a ser excluído. Este parâmetro pode ser o nome do objeto **Field** ou a posição ordinal do próprio objeto **Field**.|

## <a name="remarks"></a>Comentários

Chamar o método **Fields.Delete** em um [Recordset](recordset-object-ado.md) aberto causa um erro em tempo de execução.

