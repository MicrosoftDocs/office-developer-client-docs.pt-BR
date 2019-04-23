---
title: Método Move-ActiveX Data Objects (ADO)
TOCTitle: Move method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c7db661e590bc21605d9c289b1de6d4ae9f46e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288831"
---
# <a name="move-method-ado"></a>Método Move (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Move a posição do registro atual em um objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxe

*Recordset*. Mover *NumRecords*, *Iniciar*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*NumRecords* |Uma expressão **Long** com sinal que especifica o número de registros que a posição do registro atual é movida.|
|*Start* |Opcional. Um valor **String** ou **Variant** que é avaliado para um indicador. Também é possível utilizar um valor [BookmarkEnum](bookmarkenum.md).|

## <a name="remarks"></a>Comentários

O método **Move** é suportado em todos os objetos **Recordset**.

Se o argumento *NumRecords* for maior que zero, a posição de registro atual é movida para frente (em direção ao final do **Recordset**). Se *NumRecords* for menor que zero, a posição de registro atual será movida para trás (em direção ao início do **Recordset**).

Se a chamada de **movimentação** mover a posição do registro atual para um ponto antes do primeiro registro, o ADO define o registro atual como a posição antes do primeiro registro no Recordset ([BOF](bof-eof-properties-ado.md) é **true**). Uma tentativa em mover para trás quando a propriedade **BOF** já é **True** gera um erro.

Se a chamada a **Move** moveria a posição do registro atual para um ponto depois do último registro, o ADO define o registro atual para a posição depois do último registro no recordset ([EOF](bof-eof-properties-ado.md) é **True**). Uma tentativa em mover para frente quando a propriedade **EOF** já é **True** gera um erro.

Chamar o método **Move** a partir de um objeto **Recordset** vazio gera um erro.

Se você passar o argumento *Start*, o movimento será relativo ao registro com esse indicador, assumindo que o objeto **Recordset** suporte indicadores. Se não for especificado, o movimento será relativo ao registro atual.

Se estiver utilizando a propriedade [CacheSize](cachesize-property-ado.md) para armazenar localmente em cache os registros do provedor, passar um argumento *NumRecords* que mova a posição do registro atual para fora do grupo atual de registros em cache força o ADO a recuperar um novo grupo de registros, iniciando pelo registro de destino. A propriedade **CacheSize** determina o tamanho do grupo recém-recuperado e o registro de destino é o primeiro registro recuperado.

Se o objeto **Recordset** for apenas de avanço, um usuário ainda poderá passar um argumento *NumRecords* menor que zero, desde que o destino esteja dentro do conjunto atual de registros em cache. Se a chamada a **Move** moveria a posição do registro atual para um registro antes do primeiro registro em cache, um erro ocorrerá. Dessa forma, é possível utilizar um cache de registro que suporte rolagem total em um provedor que suporte apenas rolagem para frente. Como os registros em cache são carregados em memória, você deve evitar o armazenamento em cache de mais registros que o necessário. Mesmo se um objeto **Recordset** apenas de avanço suportar movimentos para trás dessa forma, chamar o método [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) em qualquer objeto **Recordset** apenas de avanço ainda gerará um erro.


> [!NOTE]
> [!OBSERVAçãO] O suporte para movimentos para trás em um **Recordset** apenas de avanço não é previsível, dependendo do provedor. Se o registro atual foi posicionado após o último registro no **Recordset**, **Move** para trás pode não resultar na posição atual correta.


