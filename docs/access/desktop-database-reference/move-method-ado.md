---
title: Mover o método - ActiveX Data Objects (ADO)
TOCTitle: Move Method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c968a53dffbb5463d186c97f4fa36ba5f4dfc29f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883670"
---
# <a name="move-method-ado"></a>Método Move (ADO)


**Aplica-se a**: Access 2013, o Office 2013



Move a posição do registro atual em um objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxe

*conjunto de registros*. Mover *NumRecords*, *Iniciar*

## <a name="parameters"></a>Parâmetros

  - *NumRecords*

  - Uma expressão **Long** com sinal que especifica o número de registros que a posição do registro atual é movida.

  - *Start*

  - Opcional. Um valor **String** ou **Variant** que é avaliado para um indicador. Também é possível utilizar um valor [BookmarkEnum](bookmarkenum.md).

## <a name="remarks"></a>Comentários

O método **Move** é suportado em todos os objetos **Recordset**.

Se o argumento *NumRecords* for maior que zero, a posição de registro atual é movida para frente (em direção ao final do **Recordset**). Se *NumRecords* for menor que zero, a posição de registro atual será movida para trás (em direção ao início do **Recordset**).

Se a chamada **Mover** seria mover a posição do registro atual em um ponto antes do primeiro registro, o ADO define o registro atual para a posição antes do primeiro registro no recordset ([BOF](bof-eof-properties-ado.md) é **verdadeira**). Uma tentativa em mover para trás quando a propriedade **BOF** já é **True** gera um erro.

Se a chamada **Mover** seria mover a posição do registro atual para um ponto após o último registro, o ADO define o registro atual para a posição após o último registro no recordset ([EOF](bof-eof-properties-ado.md) é **True**). Uma tentativa em mover para frente quando a propriedade **EOF** já é **True** gera um erro.

Chamar o método **Move** a partir de um objeto **Recordset** vazio gera um erro.

Se você passar o argumento *Start* , a movimentação é relativo record com este indicador, supondo que o objeto **Recordset** suporta indicadores. Se não for especificado, o movimento será relativo ao registro atual.

Força o ADO para recuperar um novo grupo de registros, se você estiver usando a propriedade [CacheSize](cachesize-property-ado.md) para registros no cache localmente do provedor, passando um argumento *NumRecords* que move a posição do registro atual fora do grupo atual de registros armazenados em cache Iniciando o registro de destino. A propriedade **CacheSize** determina o tamanho do grupo recém-recuperado e o registro de destino é o primeiro registro recuperado.

Se o objeto **Recordset** for encaminhar apenas, um usuário ainda poderá passar um argumento *NumRecords* menor do que zero, desde que o destino é dentro do conjunto atual de registros armazenados em cache. Se a chamada a **Move** moveria a posição do registro atual para um registro antes do primeiro registro em cache, um erro ocorrerá. Dessa forma, é possível utilizar um cache de registro que suporte rolagem total em um provedor que suporte apenas rolagem para frente. Como os registros em cache são carregados em memória, você deve evitar o armazenamento em cache de mais registros que o necessário. Mesmo se um objeto **Recordset** apenas de avanço suportar movimentos para trás dessa forma, chamar o método [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) em qualquer objeto **Recordset** apenas de avanço ainda gerará um erro.


> [!NOTE]
> [!OBSERVAçãO] O suporte para movimentos para trás em um **Recordset** apenas de avanço não é previsível, dependendo do provedor. Se o registro atual foi posicionado após o último registro no **Recordset**, **Move** para trás pode não resultar na posição atual correta.


