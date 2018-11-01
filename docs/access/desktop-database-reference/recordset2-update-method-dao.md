---
title: Método Recordset2.Update (DAO)
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
ms.openlocfilehash: 223846a50dd06cfe1b47f954e1dc55a40b9cc083
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869313"
---
# <a name="recordset2update-method-dao"></a><span data-ttu-id="fd3cb-102">Método Recordset2.Update (DAO)</span><span class="sxs-lookup"><span data-stu-id="fd3cb-102">Recordset2.Update Method (DAO)</span></span>


<span data-ttu-id="fd3cb-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd3cb-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="fd3cb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd3cb-104">Syntax</span></span>

<span data-ttu-id="fd3cb-105">*expressão* . Atualização (***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="fd3cb-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="fd3cb-106">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="fd3cb-106">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="fd3cb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd3cb-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd3cb-108">Nome</span><span class="sxs-lookup"><span data-stu-id="fd3cb-108">Name</span></span></p></th>
<th><p><span data-ttu-id="fd3cb-109">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="fd3cb-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="fd3cb-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fd3cb-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="fd3cb-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd3cb-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd3cb-112">UpdateType</span><span class="sxs-lookup"><span data-stu-id="fd3cb-112">UpdateType</span></span></p></td>
<td><p><span data-ttu-id="fd3cb-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="fd3cb-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="fd3cb-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="fd3cb-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="fd3cb-115">Uma constante <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> indicando o tipo de atualização, como especificado em Configurações (somente espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="fd3cb-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd3cb-116">Force</span><span class="sxs-lookup"><span data-stu-id="fd3cb-116">Force</span></span></p></td>
<td><p><span data-ttu-id="fd3cb-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="fd3cb-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="fd3cb-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="fd3cb-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="fd3cb-p101">Um valor <strong>Boolean</strong> indicando se é preciso impor ou não as alterações ao banco de dados, independentemente de os dados subjacentes terem sido alterados por outro usuário desde a chamada <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> ou <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong>. Se for <strong>True</strong>, as alterações serão impostas e as alterações feitas por outros usuários serão simplesmente substituídas. Se for <strong>False</strong> (padrão), as alterações feitas por outro usuário enquanto a atualização estiver pendente causarão uma falha na atualização para as alterações que estiverem em conflito. Nenhum erro ocorrerá, mas as propriedades <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> e <strong>BatchCollisions</strong> indicarão o número de conflitos e as linhas afetadas por conflitos, respectivamente (somente espaços de trabalho ODBCDirect).  </span><span class="sxs-lookup"><span data-stu-id="fd3cb-p101">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong> call. If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten. If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict. No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong>BatchCollisions</strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fd3cb-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd3cb-123">Remarks</span></span>

<span data-ttu-id="fd3cb-124">Use **Update** para salvar o registro atual e quaisquer alterações feitas nele.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-124">Use **Update** to save the current record and any changes you've made to it.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="fd3cb-125">[!IMPORTANTE] As alterações do registro atual serão perdidas se:</span><span class="sxs-lookup"><span data-stu-id="fd3cb-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="fd3cb-126">Você utilizar os métodos **Edit** ou **AddNew** e mover para outro registro sem primeiro usar **Update**.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="fd3cb-127">Você utilizar **Edit** ou **AddNew** e, em seguida, usar **Edit** ou **AddNew** novamente sem primeiro usar **Update**.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="fd3cb-128">Você definir a propriedade **[Bookmark](recordset2-bookmark-property-dao.md)** para outro registro.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-128">You set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="fd3cb-129">Você fechar o **Recordset** sem usar primeiro **Update**.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="fd3cb-130">Você cancelar a operação **Edit** utilizando **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="fd3cb-p102">Para editar um registro, use o método **Edit** para copiar o conteúdo do registro atual para um buffer de cópia. Se você não usar **Edit** primeiro, ocorrerá um erro ao usar **Update** ou tentar alterar um valor de campo.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-p102">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer. If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="fd3cb-133">Em um espaço de trabalho ODBCDirect, você pode fazer atualizações em lote, desde que a biblioteca de cursores aceite atualizações em lote, e o **Recordset** tenha sido aberto com a opção de bloqueio de lote otimista.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="fd3cb-134">Em um espaço de trabalho do Microsoft Access, quando a configuração da propriedade **LockEdits** do objeto **Recordset** é **True** (bloqueado de forma pessimista) em um ambiente de vários usuários, o registro permanece bloqueado desde o momento em que **Edit** é usado até que o método **Update** seja executado ou a edição seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="fd3cb-135">Se a configuração da propriedade **LockEdits** é **False** (bloqueado de forma otimista), o registro é bloqueado e comparado ao registro pré-editado antes de ser atualizado no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> <span data-ttu-id="fd3cb-136">Se o registro foi alterado desde o uso do método **Edit**, a operação **Update** falhará.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="fd3cb-137">Os bancos de dados ODBC e ISAM instalável conectados ao mecanismo de banco de dados do Microsoft Access sempre utilizam bloqueio otimista.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="fd3cb-138">Para continuar a operação **Update** com suas alterações, use o método **Update** novamente.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="fd3cb-139">Para reverter para o registro como o outro usuário alterou, atualize o registro atual por meio de movimentação 0.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>


> [!NOTE]
> <span data-ttu-id="fd3cb-p104">[!OBSERVAçãO] Para adicionar, editar ou excluir um registro, deve haver um índice exclusivo no registro, na fonte de dados de base. Se não houver, um erro "Permissão negada" ocorrerá na chamada do método **AddNew**, **Delete** ou **Edit** em um espaço de trabalho do Microsoft Access, ou um erro "Argumento inválido" ocorrerá na chamada **Update** em um espaço de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="fd3cb-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>


