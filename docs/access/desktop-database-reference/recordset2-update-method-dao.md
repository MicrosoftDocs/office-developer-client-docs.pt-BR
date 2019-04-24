---
title: Método Recordset2. Update (DAO)
TOCTitle: Update Method
ms:assetid: 1b47606a-e79c-23f1-b120-46d1429bc167
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845700(v=office.15)
ms:contentKeyID: 48543537
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052882
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4259da0eb48e7ff13e246b326cc6e96d7a916ea7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307165"
---
# <a name="recordset2update-method-dao"></a>Método Recordset2. Update (DAO)

**Aplica-se ao:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . Atualização (****** UpdateType, ***Force***)

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
<td><p><em>UpdateType</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Uma constante <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> indicando o tipo de atualização, como especificado em Configurações (somente espaços de trabalho ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><em>Force</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p>Um valor <strong>Boolean</strong> indicando se é preciso impor ou não as alterações ao banco de dados, independentemente de os dados subjacentes terem sido alterados por outro usuário desde a chamada <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> ou <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong>. Se for <strong>True</strong>, as alterações serão impostas e as alterações feitas por outros usuários serão simplesmente substituídas. Se for <strong>False</strong> (padrão), as alterações feitas por outro usuário enquanto a atualização estiver pendente causarão uma falha na atualização para as alterações que estiverem em conflito. Nenhum erro ocorre, mas as propriedades <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> e <strong>BatchCollisions</strong> indicarão o número de conflitos e as linhas afetadas por conflitos, respectivamente (apenas espaços de trabalho ODBCDirect).</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Use **Update** para salvar o registro atual e todas as alterações feitas nele.

> [!IMPORTANT]
> [!IMPORTANTE] As alterações do registro atual serão perdidas se:
> - Você utilizar os métodos **Edit** ou **AddNew** e mover para outro registro sem primeiro usar **Update**.
> - Você utilizar **Edit** ou **AddNew** e, em seguida, usar **Edit** ou **AddNew** novamente sem primeiro usar **Update**.
> - Você definir a propriedade **[Bookmark](recordset2-bookmark-property-dao.md)** para outro registro.
> - Você fechar o **Recordset** sem usar primeiro **Update**.
> - Você cancelar a operação **Edit** utilizando **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.

Para editar um registro, use o método **Edit** para copiar o conteúdo do registro atual para um buffer de cópia. Se você não usar **Edit** primeiro, ocorrerá um erro ao usar **Update** ou tentar alterar um valor de campo.

Em um espaço de trabalho ODBCDirect, você pode fazer atualizações em lote, desde que a biblioteca de cursores aceite atualizações em lote, e o **Recordset** tenha sido aberto com a opção de bloqueio de lote otimista.

Em um espaço de trabalho do Microsoft Access, quando a configuração da propriedade **LockEdits** do objeto **Recordset** é **True** (bloqueado de forma pessimista) em um ambiente de vários usuários, o registro permanece bloqueado desde o momento em que **Edit** é usado até que o método **Update** seja executado ou a edição seja cancelada. Se a configuração da propriedade **LockEdits** é **False** (bloqueado de forma otimista), o registro é bloqueado e comparado ao registro pré-editado antes de ser atualizado no banco de dados. Se o registro foi alterado desde o uso do método **Edit**, a operação **Update** falhará. Os bancos de dados ODBC e ISAM instalável conectados ao mecanismo de banco de dados do Microsoft Access sempre utilizam bloqueio otimista. Para continuar a operação **Update** com suas alterações, use o método **Update** novamente. Para reverter para o registro para como ele foi alterado por outro usuário, atualize o registro atual usando Move 0.

> [!NOTE]
> [!OBSERVAçãO] Para adicionar, editar ou excluir um registro, deve haver um índice exclusivo no registro, na fonte de dados de base. Se não houver, um erro "Permissão negada" ocorrerá na chamada do método **AddNew**, **Delete** ou **Edit** em um espaço de trabalho do Microsoft Access, ou um erro "Argumento inválido" ocorrerá na chamada **Update** em um espaço de trabalho ODBCDirect.


