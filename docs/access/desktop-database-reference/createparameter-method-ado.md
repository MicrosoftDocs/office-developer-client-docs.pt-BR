---
title: Método createParameter (ADO)
TOCTitle: CreateParameter method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fa060811f60379e720e06be9f94e9403477c7869
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295384"
---
# <a name="createparameter-method-ado"></a>Método createParameter (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Cria um novo objeto [Parameter](parameter-object-ado.md) com as propriedades especificadas.

## <a name="syntax"></a>Sintaxe

**Definir** *parâmetro*  =  *comando*. CreateParameter (*nome*, *tipo*, *direção*, *tamanho*, *valor*)

## <a name="return-value"></a>Valor de retorno

Retorna um objeto **Parameter**.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Name* |Opcional. Um valor **String** que contém o nome do objeto **Parameter**.|
|*Type* |Opcional. Um valor [DataTypeEnum](datatypeenum.md) que especifica o tipo de dados do objeto **Parameter**.|
|*Direction* |Opcional. Um valor [ParameterDirectionEnum](parameterdirectionenum.md) que especifica o tipo do objeto **Parameter**.|
|*Size* |Opcional. Um valor **Long** que especifica o comprimento máximo do valor do parâmetro em caracteres ou bytes.|
|*Value* |Opcional. Uma **Variant** que especifica o valor do objeto **Parameter**.|

## <a name="remarks"></a>Comentários

Utilize o método **CreateParameter** para criar um novo objeto **Parameter** com um nome, tipo, direção, tamanho e valor especificados. Quaisquer valores passados nos argumentos são gravados nas propriedades correspondentes de **Parameter**.

Esse método não acrescenta automaticamente o objeto **Parameter** na coleção **Parameters** de um objeto [Command](command-object-ado.md). Isso permite definir propriedades adicionais cujos valores o ADO validará quando você acrescentar o objeto **Parameter** na coleção.

Se você especificar um tipo de dados de comprimento variável no argumento *Type*, deverá passar um argumento *Size* ou definir a propriedade [Size](size-property-ado.md) do objeto **Parameter** antes de acrescentá-lo na coleção **Parameters**; caso contrário, ocorrerá um erro.

Se você especificar um tipo de dados numérico (**adNumeric** ou **adDecimal**) no argumento *Type*, também deverá definir as propriedades [NumericScale](numericscale-property-ado.md) e [Precision](precision-property-ado.md).

