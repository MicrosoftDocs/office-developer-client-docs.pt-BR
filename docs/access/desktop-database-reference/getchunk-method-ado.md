---
title: Método getChunk (ADO)
TOCTitle: GetChunk method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44cd0cb5632e64811de14f9abd3c78aac9203705
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292282"
---
# <a name="getchunk-method-ado"></a>Método getChunk (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Retorna todo, ou uma porção de, o conteúdo de um grande objeto [Field](field-object-ado.md) de dados binários ou texto.

## <a name="syntax"></a>Sintaxe

** = *campo*Variable. GetChunk (*tamanho* )

## <a name="return-value"></a>Valor de retorno

Retorna uma **Variant**.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Size* |Uma expressão **Long** que é igual ao número de bytes ou caracteres que você deseja recuperar.|

## <a name="remarks"></a>Comentários

Utilize o método **GetChunk** em um objeto **Field** para recuperar parte ou todos os seus dados de caracteres ou binários longos. Em situações em que a memória do sistema seja limitada, é possível utilizar o método **GetChunk** para manipular valores longos em porções, em vez de em sua totalidade.

Os dados retornados por **GetChunk** são atribuídos a *variable*. Se *Size* for maior que os dados restantes, o método **GetChunk** retornará somente esses dados sem preencher *variable* com espaços vazios. Se o campo estiver vazio, o método **GetChunk** retornará um valor nulo.

Cada chamada subsequente a **GetChunk** recupera os dados a partir de onde a chamada anterior a **GetChunk** foi suspensa. No entanto, se estiver recuperando dados a partir de um campo e, em seguida, definir ou ler o valor de outro campo no registro atual, o ADO supõe que você concluiu a recuperação de dados do primeiro campo. Se você chamar o método **GetChunk** no primeiro campo novamente, o ADO interpreta a chamada como uma nova operação **GetChunk** e começara a ler a partir do início dos dados. O acesso a campos em outros objetos [Recordset](recordset-object-ado.md) que não sejam clones do primeiro objeto **Recordset** não interromperão as operações **GetChunk**.

Se o bit **adFldLong** na propriedade [Attributes](attributes-property-ado.md) de um objeto **Field** for definido como **True**, será possível utilizar o método **GetChunk** para esse campo.

Se não houver um registro atual ao utilizar o método **GetChunk** em um objeto **Field**, ocorrerá o erro 3021 (sem registro atual).


> [!NOTE]
> [!OBSERVAçãO] O método **GetChunk** não opera em objetos **Field** de um objeto [Record](record-object-ado.md). Ele não executa nenhuma operação e produzirá um erro em tempo de execução.


