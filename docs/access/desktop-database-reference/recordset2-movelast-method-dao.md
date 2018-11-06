---
title: Método Recordset2.MoveLast (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 83db6ae8da804237222fc1f58e03058951d7ce41
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998984"
---
# <a name="recordset2movelast-method-dao"></a>Método Recordset2.MoveLast (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Move o último registro em um objeto **Recordset** especificado e torna esse registro o atual.

## <a name="syntax"></a>Sintaxe

*expressão* . MoveLast (***Opções***)

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

Se o recordset se refere a um tipo tabela **Recordset** (somente espaços de trabalho do Microsoft Access), o movimento segue o índice atual. Você pode definir o índice atual utilizando a propriedade **Index**. Se você não definir o índice atual, a ordem dos registros retornados será indefinida.

> [!NOTE]
> [!OBSERVAçãO] Você pode usar o método **MoveLast** para preencher totalmente um **Recordset** do tipo dynaset ou instantâneo para fornecer o número atual de registros no **Recordset**. Contudo, se você utilizar **MoveLast** dessa forma, poderá reduzir o desempenho do aplicativo. Utilize **MoveLast** somente se for absolutamente necessário para obter uma conta de registro precisa em um **Recordset** recém aberto. 
>
> Se você usa a constante **dbRunAsync** com **MoveLast**, a chamada do método é assíncrona. É possível usar a propriedade **StillExecuting** para determinar quando o **Recordset** é totalmente preenchido, e o método **Cancel** para determinar a execução da chamada assíncrona do método **MoveLast**.

Você não pode usar os métodos **MoveFirst**, **MoveLast**e **MovePrevious** em um objeto **Recordset** do tipo somente encaminhamento.

Para mover a posição do registro atual em um número específico de registros do objeto **Recordset** para frente ou para trás, use o método **Move**.

