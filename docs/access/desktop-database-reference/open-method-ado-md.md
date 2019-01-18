---
title: Método Open (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54f7ce4d5d588e644707cd7b466c29f619850824
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703829"
---
# <a name="open-method-ado-md"></a>Método Open (ADO MD)

**Aplica-se a**: Access 2013, o Office 2013

Recupera os resultados de uma consulta multidimensional e retorna os resultados para um conjunto de células.

## <a name="syntax"></a>Sintaxe

*Conjunto de células*. Abrir*fonte*, *ActiveConnection*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Source* |Opcional. Um objeto **Variant** que resulta em uma consulta multidimensional válida, como uma consulta MDX (Expressão Multidimensional). O argumento *Source* corresponde à propriedade [Source](source-property-ado-md.md) . Para obter mais informações sobre MDX, consulte a documentação do OLE DB para OLAP no Microsoft Data Access Components SDK.|
|*ActiveConnection* |Opcional. Um objeto **Variant** que resulta em uma sequência de caracteres que especifica um nome de variável de objeto [Connection](connection-object-ado.md) válido do ADO ou em uma definição de conexão. O argumento *ActiveConnection* Especifica a conexão para abrir o objeto de [conjunto de células](cellset-object-ado-md.md) . Se você passar uma definição de conexão para esse argumento, o ADO abrirá uma nova conexão utilizando os parâmetros especificados. O argumento *ActiveConnection* corresponde à propriedade [ActiveConnection](activeconnection-property-ado-md.md) .|

## <a name="remarks"></a>Comentários

O método **Open** gerará um erro se um desses parâmetros for omitido e o valor de sua propriedade correspondente não tiver sido definido antes da tentativa de abrir o **Cellset**.

