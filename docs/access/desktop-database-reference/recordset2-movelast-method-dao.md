---
title: Método Recordset2. moVelast (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 829c4dd759bce86388cc65aa5b63276eec438ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307256"
---
# <a name="recordset2movelast-method-dao"></a>Método Recordset2. moVelast (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Move o último registro em um objeto **Recordset** especificado e torna esse registro o atual.

## <a name="syntax"></a>Sintaxe

*expressão* . MoVelast (***Opções***)

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Defina para <strong>dbRunAsync</strong> para executar a chamada de <strong>MoveLast</strong> de forma assíncrona.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Use os métodos **Move** para mover de um registro para outro sem aplicar nenhuma condição.

Se você editar o registro atual, certifique-se de usar o método **Update** para salvar as alterações antes de mover para outro registro. Se você mover para outro registro sem realizar a atualização, as alterações serão perdidas sem nenhum aviso.

Quando você abre um **Recordset**, o primeiro registro é o atual, e a propriedade **BOF** é **False**. Se o **Recordset** não contiver nenhum registro, a propriedade **BOF** será **True**, e não haverá nenhum registro atual.

Se o primeiro ou o último registro já for o atual quando você usar **MoveFirst** ou **MoveLast**, o registro atual não será alterado.

Se Recordset se refere a um **Recordset** do tipo tabela (somente espaços de trabalho do Microsoft Access), o movimento segue o índice atual. Você pode definir o índice atual utilizando a propriedade **Index**. Se você não definir o índice atual, a ordem dos registros retornados será indefinida.

> [!NOTE]
> [!OBSERVAçãO] Você pode usar o método **MoveLast** para preencher totalmente um **Recordset** do tipo dynaset ou instantâneo para fornecer o número atual de registros no **Recordset**. Contudo, se você utilizar **MoveLast** dessa forma, poderá reduzir o desempenho do aplicativo. Utilize **MoveLast** somente se for absolutamente necessário para obter uma conta de registro precisa em um **Recordset** recém aberto. 
>
> Se você usa a constante **dbRunAsync** com **MoveLast**, a chamada do método é assíncrona. É possível usar a propriedade **StillExecuting** para determinar quando o **Recordset** é totalmente preenchido, e o método **Cancel** para determinar a execução da chamada assíncrona do método **MoveLast**.

Você não pode usar os métodos **MoveFirst**, MoveLast e **MovePrevious** em um objeto **Recordset** do tipo somente encaminhamento. ****

Para mover a posição do registro atual em um número específico de registros do objeto **Recordset** para frente ou para trás, use o método **Move**.

