---
title: Método CreateParameter (ADO)
TOCTitle: CreateParameter Method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 39916e8ef9cf240aba25f813d0cb7bf765a95cbe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464595"
---
# <a name="createparameter-method-ado"></a>Método CreateParameter (ADO)


**Aplica-se a**: Access 2013 | Office 2013


Cria um novo objeto [Parameter](parameter-object-ado.md) com as propriedades especificadas.

## <a name="syntax"></a>Sintaxe

**Definir** *parâmetro*  =  *comando*. CreateParameter (*nome*, *tipo*, *direção*, *tamanho*, *valor*)

## <a name="return-value"></a>Valor de Retorno

Retorna um objeto **Parameter**.

## <a name="parameters"></a>Parâmetros

  - *Name*

  - Opcional. Um valor **String** que contém o nome do objeto **Parameter**.

  - *Type*

  - Opcional. Um valor [DataTypeEnum](datatypeenum.md) que especifica o tipo de dados do objeto **Parameter**.

  - *Direction*

  - Opcional. Um valor [ParameterDirectionEnum](parameterdirectionenum.md) que especifica o tipo do objeto **Parameter**.

  - *Size*

  - Opcional. Um valor **Long** que especifica o comprimento máximo do valor do parâmetro em caracteres ou bytes.

  - *Value*

  - Opcional. Uma **Variant** que especifica o valor do objeto **Parameter**.

## <a name="remarks"></a>Comentários

Utilize o método **CreateParameter** para criar um novo objeto **Parameter** com um nome, tipo, direção, tamanho e valor especificados. Quaisquer valores passados nos argumentos são gravados nas propriedades correspondentes de **Parameter**.

Esse método não acrescenta automaticamente o objeto **Parameter** na coleção **Parameters** de um objeto [Command](command-object-ado.md). Isso permite definir propriedades adicionais cujos valores o ADO validará quando você acrescentar o objeto **Parameter** na coleção.

Se você especificar um tipo de dados de comprimento variável no argumento de *tipo* , você deve passar um argumento de *tamanho* ou definir a propriedade [Size](size-property-ado.md) do objeto **Parameter** antes de acrescentá-lo à coleção **Parameters** ; Caso contrário, ocorrerá um erro.

Se você especificar um tipo de dados numérico (**adNumeric** ou **adDecimal**) no argumento *Type*, também deverá definir as propriedades [NumericScale](numericscale-property-ado.md) e [Precision](precision-property-ado.md).

