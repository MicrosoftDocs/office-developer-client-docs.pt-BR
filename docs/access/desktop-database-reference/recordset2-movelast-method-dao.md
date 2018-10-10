---
title: Método Recordset2.MoveLast (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c66adcadcf07ab18db60ba39ae6bc66d58d5e5db
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465434"
---
# <a name="recordset2movelast-method-dao"></a>Método Recordset2.MoveLast (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Move o último registro em um objeto **Recordset** especificado e torna esse registro o atual.

## <a name="syntax"></a>Sintaxe

*expressão* . MoveLast (***Opções***)

*expressão* Uma variável que representa um objeto **Recordset2** .

### <a name="parameters"></a>Parâmetros

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
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Opções</p></td>
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
> <P>[!OBSERVAçãO] Você pode usar o método <STRONG>MoveLast</STRONG> para preencher totalmente um <STRONG>Recordset</STRONG> do tipo dynaset ou instantâneo para fornecer o número atual de registros no <STRONG>Recordset</STRONG>. Contudo, se você utilizar <STRONG>MoveLast</STRONG> dessa forma, poderá reduzir o desempenho do aplicativo. Utilize <STRONG>MoveLast</STRONG> somente se for absolutamente necessário para obter uma conta de registro precisa em um <STRONG>Recordset</STRONG> recém aberto. Se você usa a constante <STRONG>dbRunAsync</STRONG> com <STRONG>MoveLast</STRONG>, a chamada do método é assíncrona. É possível usar a propriedade <STRONG>StillExecuting</STRONG> para determinar quando o <STRONG>Recordset</STRONG> é totalmente preenchido, e o método <STRONG>Cancel</STRONG> para determinar a execução da chamada assíncrona do método <STRONG>MoveLast</STRONG>.</P>



Você não pode usar os métodos **MoveFirst**, **MoveLast**e **MovePrevious** em um objeto **Recordset** do tipo somente encaminhamento.

Para mover a posição do registro atual em um número específico de registros do objeto **Recordset** para frente ou para trás, use o método **Move**.

